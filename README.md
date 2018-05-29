# quickstart-compliance-cis-benchmark
## CIS AWS Foundations Benchmark in the AWS Cloud

This Quick Start deploys and configures a standardized architecture for the Center for Internet Security (CIS) AWS Foundations Benchmark.

CIS Benchmarks are consensus-based configuration guidelines developed by experts in US government, business, industry, and academia to help organizations assess and improve security.

This Quick Start implements the CIS AWS Foundations Benchmark, which is a set of security configuration best practices for hardening AWS accounts, and provides continuous monitoring capabilities for these security configurations.

The Quick Start supports the benchmark by creating AWS Config rules, Amazon CloudWatch alarms, and CloudWatch Events rules in your AWS account. The deployment is automated by customizable AWS CloudFormation templates and scripts that build and configure the environment in about 10 minutes. The Quick Start also includes a security controls matrix (Microsoft Excel spreadsheet), which shows how the Quick Start components and configuration map to CIS controls. For more information about the recommendations implemented by this Quick Start, see the [CIS AWS Foundations Benchmark specification](https://d0.awsstatic.com/whitepapers/compliance/AWS_CIS_Foundations_Benchmark.pdf) and the [security controls matrix](https://fwd.aws/K8NEq).

You can also use the AWS CloudFormation templates as a starting point for your own implementation.

This Quick Start was built by AWS solutions architects and compliance experts in collaboration with Accenture, an AWS Premier Consulting Partner.

![Quick Start architecture for CIS AWS Foundations Benchmark](https://d0.awsstatic.com/partner-network/QuickStart/datasheets/quickstart-architecture-for-cis-benchmark-on-aws.png)

For architectural details, step-by-step instructions, and customization options, see the [deployment guide](https://fwd.aws/wPK3M).

To post feedback, submit feature ideas, or report bugs, use the **Issues** section of this GitHub repo.
If you'd like to submit code for this Quick Start, please review the [AWS Quick Start Contributor's Kit](https://aws-quickstart.github.io/).
