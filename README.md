# AWS Security Detection and Response Lab

## Overview

This project demonstrates how to build an automated cloud security monitoring and incident response workflow in AWS. The environment was designed to simulate how modern security teams detect suspicious activity, trigger automated remediation, and maintain audit visibility.

## Objectives

* Build AWS network environment
* Deploy compute resources securely
* Enable audit logging and network telemetry
* Detect suspicious activity with GuardDuty
* Trigger automated remediation with Lambda
* Send security alerts with SNS
* Document and version the project in GitHub


## Architecture

VPC → Public / Private Subnets → EC2 → CloudTrail / Flow Logs / GuardDuty → EventBridge → Lambda → SNS



## AWS Services Used

* Amazon VPC
* Amazon EC2
* AWS IAM
* AWS Systems Manager (SSM)
* AWS CloudTrail
* Amazon GuardDuty
* Amazon CloudWatch
* AWS Lambda
* Amazon EventBridge
* Amazon SNS
* Amazon S3



## Security Controls Implemented

* Network segmentation using public and private subnets
* IAM role-based access instead of static credentials
* EC2 administration via SSM (no SSH exposure)
* Threat detection with GuardDuty
* API activity logging with CloudTrail
* Network visibility with VPC Flow Logs
* Automated containment using Lambda
* Alert notifications through SNS



## Build Phases

### Phase 1 — Network Foundation

* Created custom VPC
* Configured public and private subnets
* Attached Internet Gateway
* Built route tables

### Phase 2 — Secure Compute

* Created EC2 IAM role
* Configured security group
* Deployed Amazon Linux EC2 instance
* Validated SSM access

### Phase 3 — Visibility & Detection

* Enabled CloudTrail
* Enabled GuardDuty
* Enabled VPC Flow Logs

### Phase 4 — Automated Response

* Created SNS alert topic
* Built Lambda remediation function
* Created EventBridge rule for GuardDuty findings
* Automated EC2 containment workflow

### Phase 5 — Validation

* Generated GuardDuty sample findings
* Confirmed automatic EC2 stop action
* Verified end-to-end detection pipeline



## Example Incident Workflow

1. GuardDuty generates a finding
2. EventBridge captures the event
3. Lambda function executes response logic
4. EC2 instance is stopped automatically
5. SNS sends security notification
6. Logs are retained for investigation



## Skills Demonstrated

* AWS Cloud Security
* Incident Response Automation
* IAM and Least Privilege Concepts
* Detection Engineering
* Security Monitoring
* Infrastructure Documentation
* Git / Version Control
* Cloud Operations


## Built as a hands-on cloud security engineering project for portfolio and interview readiness.
