---
page_title: "snowflake_system_get_aws_sns_iam_policy Data Source - terraform-provider-snowflake"
subcategory: "Preview"
description: |-
  
---

!> **Caution: Preview Feature** This feature is considered a preview feature in the provider, regardless of the state of the resource in Snowflake. We do not guarantee its stability. It will be reworked and marked as a stable feature in future releases. Breaking changes are expected, even without bumping the major version. To use this feature, add the relevant feature name to `preview_features_enabled` field in the [provider configuration](https://registry.terraform.io/providers/snowflakedb/snowflake/latest/docs#schema). Please always refer to the [Getting Help](https://github.com/snowflakedb/terraform-provider-snowflake?tab=readme-ov-file#getting-help) section in our Github repo to best determine how to get help for your questions.

# snowflake_system_get_aws_sns_iam_policy (Data Source)



For more details, visit the official Snowflake documentation: https://docs.snowflake.com/en/sql-reference/functions/system_get_aws_sns_iam_policy.
Read this guide to understand how to use the snowflake_system_get_aws_sns_iam_policy to integrate with AWS: https://docs.snowflake.com/en/user-guide/data-load-snowpipe-auto-s3#step-1-subscribe-the-snowflake-sqs-queue-to-the-sns-topic.
It's SQL-based, but after knowing what has to be done use corresponding resources and data-sources from the Snowflake and AWS Terraform provider.

## Example Usage

```terraform
data "snowflake_system_get_aws_sns_iam_policy" "snowflake_policy" {
  aws_sns_topic_arn = "<aws_sns_topic_arn>"
}
```

-> **Note** If a field has a default value, it is shown next to the type in the schema.

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `aws_sns_topic_arn` (String) Amazon Resource Name (ARN) of the SNS topic for your S3 bucket

### Read-Only

- `aws_sns_topic_policy_json` (String) IAM policy for Snowflake’s SQS queue to subscribe to this topic
- `id` (String) The ID of this resource.
