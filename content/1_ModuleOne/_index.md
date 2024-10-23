---
title: "Getting Started"
chapter: true
weight: 1
---

# Getting Started

![ReadMe AWS System Overview](/images/system-overview.png)

## Solution Overview

This example implementation reacts to the changes to the API Gateway made manually or through a CI/CD pipeline. It will synchronize changes from the API Gateway to the developer portal in ReadMe. It does this by exporting the API Gateway OpenAPI definition and uploading changes to ReadMe. Optionally, it will delete the existing definition when you delete an API Gateway endpoint. Implementation uses the following resources:

1. **Amazon API Gateway** that gets changed manually or by an automated process
1. **Amazon EventBridge** that receives events whenever you deploy API Gateway stage
1. **AWS Lambda function** that is invoked by the EventBridge and synchronizes definition to ReadMe
1. **AWS Systems Manager Parameter Store** to store Lambda configuration parameters
1. **AWS Secrets Manager** to store ReadMe API key used for authentication
1. **Amazon CloudWatch** with alarms used for synchronization error notifications
1. **Amazon Simple Notification Service (SNS)** to deliver error notifications to the subscribed email recipients

## Prerequisites

This workshop requires:
1. An AWS account.  If you don't wish to use your own account, you can use the one that is generated for the workshop by clicking HERE (link will go here).
1. CLI tool for Serverless Application Models (SAM).  
1. ReadMe account and a project within that ReadMe account.  
1. [GitHub CLI](https://cli.github.com/)
