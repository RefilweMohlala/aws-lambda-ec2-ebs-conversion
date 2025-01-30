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


