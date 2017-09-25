# quickstart-enterprise-accelerator-cis-benchmark

The CIS Enterprise Accelerator Quick Start deploys a standard environment for establishing CIS AWS 1.1 benchmark governance rules.
Refer the benchmark specification [here](https://benchmarks.cisecurity.org/en-us/?route=downloads.form.awsfoundations.110)).

The ```main.template``` is an AWS CloudFormation template for establishing CIS AWS 1.1 benchmark governance rules.

The ```cis-benchmark-matrix.xlsx``` is a spreadsheet that maps the CIS Amazon Web Services Foundations benchmarks to the specific security controls provisioned in the CloudFormation template.

The AWS services used for these benchmarks are used in the following relationship:

![CIS Benchmark Architecture Diagram] TODO

The following preconditions must be met before the stack can be launched:

1. AWS Config must be running in the region where this template will be run. This is needed for Config Rules.
2. Amazon CloudTrail must be delivering logs to CloudWatch Logs. This is needed for CloudWatch metrics and alarms.
3. AWS Lambda must be supported in the region where this template will be launched. See [this](https://aws.amazon.com/about-aws/global-infrastructure/regional-product-services/) page for region support.

The controls are a combination of AWS Config Rules, Amazon CloudWatch rules, and Amazon CloudWatch alarms.
Please note that these resources will incur costs in your account; please refer to the pricing model for each service.

For example, an estimate in us-east-1:
