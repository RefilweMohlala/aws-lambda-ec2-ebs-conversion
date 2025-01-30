# AWS EBS Volume Automation with Lambda & EventBridge

## Overview
This project automates the conversion of newly created **EBS gp2 volumes** to **gp3** using AWS Lambda and EventBridge.

## AWS Services Used
- **EventBridge (CloudWatch Events)**
- **Lambda**
- **CloudWatch Logs**
- **IAM**

## How It Works
1. **EventBridge Rule** detects new EBS volume creation.
2. **Lambda Function** checks if the volume is `gp2` and converts it to `gp3`.
3. **CloudWatch Logs** store execution logs.

## Lambda Code
```python
import boto3
import json

ec2 = boto3.client('ec2')

def lambda_handler(event, context):
    volume_id = event['detail']['requestParameters']['volumeId']
    print(f"Processing volume: {volume_id}")

    ec2.modify_volume(VolumeId=volume_id, VolumeType='gp3')
    print(f"Volume {volume_id} successfully converted to gp3")

