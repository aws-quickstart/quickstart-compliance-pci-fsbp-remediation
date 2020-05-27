<p align="center">
</p>

# Automated Remediations for AWS CIS Benchmarks using AWS Security Hub

The CIS Benchmarks for AWS are the only industry standard, objective, consensus-driven security guideline for AWS. They consist of security policies that serve as widely adopted security best practices when configuring AWS deployments and cover all aspects of an AWS deployment. AWS provides built-in automated detection of CIS violations via AWS Security Hub. 

The Quick Start for CIS provides CloudFormation templates that provide real time and automated remediations for each of the AWS CIS benchmarks in the AWS Security Hub service by providing a fully automated integration of AWS Security Hub Custom Actions and AWS Systems Manager automation documents.



## How it Works

1. Leverages AWS Security Hub directly to provide automated detection of CIS Benchmarks findings
2. Provides NEW AWS Systems Manager Automation Documents for automated remediation for AWS Security Hub CIS Benchmark findings. All documents are automatically provisioned via a AWS CloudFormation template.
3. Provides NEW integration of AWS Security Hub Custom Actions with AWS Systems Manager Automation Documents to provide real time remediations of AWS Security Hub CIS Benchmark findings. Provisions Event based (CloudWatch Events) processing of AWS Security Hub Findings based on the AWS Security Hub Finding Format (ASFF) and packages the finding as input parameters for the associated AWS Systems Manager Automation Document.

## Solution Design


![Solution Design](https://github.com/kmahajan11/quickstart-compliance-cis-benchmark/blob/master/assets/CIS_Benchmark_Architecture.png)

## How To Install

1. **Template 1 of 3:** aws-cis-systemsmanagerautomations.yml
* Provisions AWS Systems Manager automation documents. These documents are used to provide automated remediations within the provisioned AWS Security Hub Action.
* Provisions with fully built-in pre-reqs. No input parameters required. Simply install on the CloudFormation console (or CLI). Installs in approx 3-4 mins.

2. **Template 2 of 3:** aws-cis-securityhubactions.yml
* Provisions AWS CloudWatch Evemts and AWS Security Hub Custom Actions. No input parameters. Simply install on the CloudFormation console (or CLI). Installs in approx 3-4 mins.
* Leverages the output from the previous template specifically the AWS Systems Manager Automation documents

3. **Template 3 of 3:** aws-cis-cloudwatchlogmetricfilters.yml
* Provisions CloudWatch Log Metric Filters and corresponding CloudWatch Alarms for each of the required CIS Benchmarks. Installs independently of templates 1 and 2.  Provide email as input for SNS notification. Installs in approx 2-3 mins. 


## Author

Kanishk Mahajan; kanishk.mahajan@gmail.com

