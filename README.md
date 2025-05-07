# Automated_S3_Remediation
Automate detection and remediation of public S3 buckets with AWS Config &amp; Systems Manager

## Overview
This repository demonstrates how organizations can automatically detect and remediate Amazon S3 buckets with disabled Public Access Block settings. By leveraging AWS Config and AWS Systems Manager Automation, we enforce security policies without manual intervention, reducing risk, saving operational time, and ensuring continuous compliance. Publicly accessible S3 buckets can cause data breaches, regulatory fines, and reputational harm. If the setting is ever disabled by mistake or malicious action, AWS Config will detect the change and automatically trigger a remediation runbook to restore privacy.

## Prerequisites

- AWS CLI v2 installed and configured
- IAM permissions:  
  - `config:PutConfigurationRecorder`, `config:StartConfigurationRecorder`,    `config:PutConfigRule`,  `config:DescribeComplianceByConfigRule`, `config:DescribeConfigRemediationExecutions`  
  - `ssm:StartAutomationExecution`, `iam:PassRole`, `s3:PutPublicAccessBlock`  
- AWS Config enabled in your target region 


## 🔧 Implementation Steps
For the full project walkthrough and detailed steps, see  
➡️ [Read the full guide on Dev.to](https://dev.to/ola_a_da305c9d390ba68b3c5/automated-s3-remediation-with-aws-config-systems-manager-2h7h)

Block Public Access is re‑enabled within minutes of any change, with a full history of detection and remediation in AWS Config and CloudWatch, applying automatically to all existing and future S3 buckets.

## Conclusion
Using Automated S3 Remediation to Enforce Block Public Access is a proactive approach to maintaining the security of your Amazon S3 buckets. By automating the detection and remediation of non-compliant configurations, you can prevent data exposure and ensure compliance with security best practices. You can take advantage of AWS Config and Systems Manager Automation to help your cloud infrastructure security.
