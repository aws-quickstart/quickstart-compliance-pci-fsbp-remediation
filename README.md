# quickstart-enterprise-accelerator-cis-benchmark

The CIS Enterprise Accelerator Quick Start deploys a standard environment for establishing CIS AWS 1.1 benchmark governance rules.
Refer the benchmark specification [here](https://d0.awsstatic.com/whitepapers/compliance/AWS_CIS_Foundations_Benchmark.pdf).

The ```main.template``` is an AWS CloudFormation template for establishing CIS AWS 1.1 benchmark governance rules.

The ```cis-benchmark-matrix.xlsx``` is a spreadsheet that maps the CIS Amazon Web Services Foundations benchmarks to the specific security controls provisioned in the CloudFormation template.

The AWS services used for these benchmarks are used in the following relationship:

![Architecture](https://github.com/aws-quickstart/quickstart-enterprise-accelerator-cis-benchmark/blob/develop/assets/CIS_Benchmark_Architecture.png)

The following preconditions must be met before the stack can be launched:

1. AWS Config must be running in the region where this template will be run. This is needed for Config Rules.
2. Amazon CloudTrail must be delivering logs to CloudWatch Logs. This is needed for CloudWatch metrics and alarms.
3. AWS Lambda must be supported in the region where this template will be launched. See [this](https://aws.amazon.com/about-aws/global-infrastructure/regional-product-services/) page for region support.

The controls are a combination of AWS Config Rules, Amazon CloudWatch rules, and Amazon CloudWatch alarms.
Please note that these resources will incur costs in your account; please refer to the pricing model for each service.

For example, an estimate in us-east-1:

* ```Config Rules```: 15 rules   @ $2.00/rule/month    = $30.00/month
* ```CloudWatch Alarms```:  5 alarms  @ $0.10/alarm/month   =  $0.50/month
* ```CloudWatch Metrics```: 5 metrics @ $0.30/metric/month  =  $1.50/month
* ```CloudWatch Logs```:  23 logs    @ $0.50/GB ingested   =  based on usage
* ```CloudWatch Event Rules```: 7 Rules - Variable - $1.00 per million custom events generated.
* ```AWS Lambda```:  Variable (first 1 million requests per month are free)
* ```S3 Storage```: Variable
