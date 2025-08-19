# AWS Access Key Rotation

Automated solution for AWS IAM access key rotation using AWS Lambda, AWS Config, SSM Document, and SNS, with secure S3 storage.

## Overview

This solution automates the rotation of AWS IAM user access keys to enhance security by enforcing regular key updates, utilizing AWS Systems Manager (SSM) for execution and AWS Config for compliance monitoring.

![alt text](<Screenshot 2025-08-19 203913.png>)

## Features

- Automated IAM access key rotation
- AWS Systems Manager automation via SSM documents
- AWS Config rules for compliance monitoring
- Secure S3 storage with server-side encryption
- Email notifications for key expiration
- Lambda function for key management
- CloudWatch monitoring and logging

## Prerequisites

1. AWS Account
2. IAM permissions to create:
    - Lambda functions
    - IAM roles and policies
    - SNS configuration
    - AWS Config rules
    - SSM documents
    - S3 buckets with encryption

## Manual Setup Required

1. AWS Config setup

## Deployment

The solution is deployed using CloudFormation template `access-key-rotation.yaml` which sets up:

- Lambda function for key rotation
- Required IAM roles and policies
- SNS email notification configuration
- SSM automation documents
- AWS Config rules
- S3 bucket with server-side encryption

## Security Considerations

- Access keys are rotated automatically
- New keys securely stored in S3 with server-side encryption
- SSM document for standardized execution
- AWS Config rules for compliance monitoring
- Old keys are deactivated after grace period
- Secure notification delivery via SNS
- Logging and monitoring via CloudWatch

## Contributing

Feel free to submit issues and pull requests.
