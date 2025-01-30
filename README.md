# AWS EBS Volume Automation with Lambda & EventBridge

## Overview
This project automates the conversion of newly created **EBS gp2 volumes** to **gp3** using AWS Lambda and EventBridge.

## AWS Services Used
- **EventBridge (CloudWatch Events)**
- **Lambda**
- **Python**
- **CloudWatch Logs**
- **IAM**

## How It Works
1. **EventBridge Rule** detects new EBS volume creation.
2. **Lambda Function** checks if the volume is `gp2` and converts it to `gp3`.
3. **CloudWatch Logs** store execution logs.


## Screenshots
EventBridge rule
![eventbridge rule](https://github.com/user-attachments/assets/66ff0962-5cdf-4bd2-b311-63d1f28f2364)

Log Streams
![log streams](https://github.com/user-attachments/assets/10fff5d7-c60b-4c2b-a820-b89ae93f3e93)

Latest Log Event 
![latest log event](https://github.com/user-attachments/assets/4600ec86-2860-413c-90b5-67576ebe2089)

gp3 Volume 
![GP3 vol](https://github.com/user-attachments/assets/f41baf64-5b7b-48a3-b412-d71cb0a27c4e)
