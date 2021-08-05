# aws-cdk-python-sample

The AWS Cloud Development Kit (CDK) lets you define your cloud infrastructure as code. Constructs (as well as stacks and apps) are represented as types in your programming language of choice.

Constructs come in three fundamental flavors:

* **AWS CloudFormation-only** or **L1** (short for "level 1"): These constructs correspond directly to resource types defined by AWS CloudFormation. In fact, these constructs are automatically generated from the AWS CloudFormation specification, so when a new AWS service is launched, the AWS CDK supports it as soon as AWS CloudFormation does.
AWS CloudFormation resources always have names that begin with Cfn. For example, in the Amazon S3 module, CfnBucket is the L1 module for an Amazon S3 bucket.

* **Curated** or **L2**: These constructs are carefully developed by the AWS CDK team to address specific use cases and simplify infrastructure development. For the most part, they encapsulate L1 modules, providing sensible defaults and best-practice security policies. For example, in the Amazon S3 module, Bucket is the L2 module for an Amazon S3 bucket.
L2 modules may also define supporting resources needed by the primary resource. Some services have more than one L2 module in the Construct Library for organizational purposes.

* **Patterns** or **L3**: Patterns declare multiple resources to create entire AWS architectures for particular use cases. All the plumbing is already hooked up, and configuration is boiled down to a few important parameters. In the AWS Construct Library, patterns are in separate modules from L1 and L2 constructs.


## Important Links
1. [AWS CDK API reference](https://docs.aws.amazon.com/cdk/api/latest/docs/aws-construct-library.html)
2. [Working with the AWS CDK in Python](https://docs.aws.amazon.com/cdk/latest/guide/work-with-cdk-python.html)
