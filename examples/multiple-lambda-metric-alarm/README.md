# Cloudwatch metric alarms for AWS Lambda example

Configuration in this directory creates Cloudwatch metric alarms for AWS Lambda. One metric alarm is based on `metric_name` defined by AWS Lambda service, another metric alarm is based on `metric_query` which monitors error rates (number of errors divided by the number of invocations).

## Usage

To run this example you need to execute:

```bash
$ terraform init
$ terraform plan
$ terraform apply
```

Note that this example may create resources which cost money. Run `terraform destroy` when you don't need these resources.

<!-- BEGINNING OF PRE-COMMIT-TERRAFORM DOCS HOOK -->
## Requirements

| Name | Version |
|------|---------|
| <a name="requirement_terraform"></a> [terraform](#requirement\_terraform) | >= 0.12.26 |
| <a name="requirement_aws"></a> [aws](#requirement\_aws) | >= 2.55 |

## Providers

No providers.

## Modules

| Name | Source | Version |
|------|--------|---------|
| <a name="module_alarms"></a> [alarms](#module\_alarms) | ../../modules/metric-alarms-by-multiple-dimensions |  |
| <a name="module_aws_lambda_function1"></a> [aws\_lambda\_function1](#module\_aws\_lambda\_function1) | ../fixtures/aws_lambda_function |  |
| <a name="module_aws_lambda_function2"></a> [aws\_lambda\_function2](#module\_aws\_lambda\_function2) | ../fixtures/aws_lambda_function |  |
| <a name="module_aws_sns_topic"></a> [aws\_sns\_topic](#module\_aws\_sns\_topic) | ../fixtures/aws_sns_topic |  |

## Resources

No resources.

## Inputs

No inputs.

## Outputs

| Name | Description |
|------|-------------|
| <a name="output_this_cloudwatch_metric_alarm_arns"></a> [this\_cloudwatch\_metric\_alarm\_arns](#output\_this\_cloudwatch\_metric\_alarm\_arns) | List of ARN of the Cloudwatch metric alarms |
| <a name="output_this_cloudwatch_metric_alarm_ids"></a> [this\_cloudwatch\_metric\_alarm\_ids](#output\_this\_cloudwatch\_metric\_alarm\_ids) | List of ID of the Cloudwatch metric alarms |
| <a name="output_this_lambda_function1_arn"></a> [this\_lambda\_function1\_arn](#output\_this\_lambda\_function1\_arn) | Lambda function ARN |
| <a name="output_this_lambda_function1_name"></a> [this\_lambda\_function1\_name](#output\_this\_lambda\_function1\_name) | Lambda function name |
<!-- END OF PRE-COMMIT-TERRAFORM DOCS HOOK -->
