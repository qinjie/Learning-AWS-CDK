# Learning-AWS-CDK

## Bootstrapping Environment

**Opiton 1: CLI**

Bootstrapping can be conveniently done using [CDK CLI](https://docs.aws.amazon.com/cdk/latest/guide/cli.html).

**Option 2: CloudFormation**

For AWS environment where CLI is dis-allowed, bootstrapping can still be done through Cloud Formation template `bootstrap-template.yml`, which is downloaded from [aws-cdk in GitHub](https://github.com/aws/aws-cdk/blob/master/packages/aws-cdk/lib/api/bootstrap/bootstrap-template.yaml).

**With Permissions Boundary**

If the AWS environment is restricted by [Permissions Boundary](https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies_boundaries.html), modify existing `bootstrap-template.yml` file by adding PermissionsBoundary in role creation. The resulted template is `bootstrap-template-with-permissions-boundary.yml`.

* Find the Permissions Boundary policy ARN in your AWS environment.
* Fill the parameter on first step when you create a stack using `bootstrap-template-with-permissions-boundary.yml`.
