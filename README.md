# aws-cdk-python-sample

The AWS Cloud Development Kit (CDK) lets you define your cloud infrastructure as code. Constructs (as well as stacks and apps) are represented as types in your programming language of choice.

Constructs come in three fundamental flavors:

* **AWS CloudFormation-only** or **L1** (short for "level 1"): These constructs correspond directly to resource types defined by AWS CloudFormation. In fact, these constructs are automatically generated from the AWS CloudFormation specification, so when a new AWS service is launched, the AWS CDK supports it as soon as AWS CloudFormation does.
AWS CloudFormation resources always have names that begin with Cfn. For example, in the Amazon S3 module, CfnBucket is the L1 module for an Amazon S3 bucket.

* **Curated** or **L2**: These constructs are carefully developed by the AWS CDK team to address specific use cases and simplify infrastructure development. For the most part, they encapsulate L1 modules, providing sensible defaults and best-practice security policies. For example, in the Amazon S3 module, Bucket is the L2 module for an Amazon S3 bucket.
L2 modules may also define supporting resources needed by the primary resource. Some services have more than one L2 module in the Construct Library for organizational purposes.

* **Patterns** or **L3**: Patterns declare multiple resources to create entire AWS architectures for particular use cases. All the plumbing is already hooked up, and configuration is boiled down to a few important parameters. In the AWS Construct Library, patterns are in separate modules from L1 and L2 constructs.

# Prerequisites

1. [AWS account](https://aws.amazon.com/premiumsupport/knowledge-center/create-and-activate-aws-account/)
2. [Configured credentials](https://docs.aws.amazon.com/general/latest/gr/aws-sec-cred-types.html)
3. [NodeJS](https://nodejs.org/en/download/)
    * **Note:** 13.0.0 through 13.6.0 are not compatible.
4. [Python3.6 or later](https://www.python.org/)
5. [Pip](https://pip.pypa.io/en/stable/installation/)
6. [virtualenv](https://virtualenv.pypa.io/en/latest/installation.html)
5. [Setting your credentials in Node](https://docs.aws.amazon.com/sdk-for-javascript/v2/developer-guide/setting-credentials-node.html)

# Process
### 1. Install CDK

```bash
$ npm install -g aws-cdk
```

### 2. Init your project

```bash
$ mkdir cdk

$ cd cdk

$ cdk init app --language python
```

### 3. Start the virtual environment

If the venv folder hasn't been created

```bash
$ python3 -m venv .venv
```

If the virtual environment has been set up you can start it

```bash
$ source .venv/bin/activate
```

### 4. Install venv dependencies
```bash
$ pip install -r requirements.txt
```

### 5. Synthesize the CloudFormation template

```
$ cdk synth
```

To add additional dependencies, for example other CDK libraries, just add
them to your `setup.py` file and rerun the `pip install -r requirements.txt`
command.

## Useful commands

 * `cdk ls`          list all stacks in the app
 * `cdk synth`       emits the synthesized CloudFormation template
 * `cdk deploy`      deploy this stack to your default AWS account/region
 * `cdk diff`        compare deployed stack with current state
 * `cdk docs`        open CDK documentation


## Important Links
1. [AWS CDK API reference](https://docs.aws.amazon.com/cdk/api/latest/docs/aws-construct-library.html)
2. [Working with the AWS CDK in Python](https://docs.aws.amazon.com/cdk/latest/guide/work-with-cdk-python.html)
