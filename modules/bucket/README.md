# iam-bucket
Create and configure access to the amazon S3 service.

## Providers

| Name | Version |
|------|---------|
| aws | ~> 2.40 |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:-----:|
| acl | Defines which type of bucket access acl S3 (public or privite). | `string` | `"private"` | no |
| create\_object | Enables bucket object creation (true or false). | `string` | `"false"` | no |
| force\_destroy | Indicates all objects (including any locked objects) should be deleted from the bucket so that the bucket can be destroyed without error | `string` | `"false"` | no |
| logging | Enable logging set this to [{target\_bucket = 'xxx' target\_prefix = 'logs/'}] | `map(string)` | `{}` | no |
| name | Bucket S3 name. | `string` | `""` | no |
| object\_key | The name of the object once it is in the bucket. | `string` | `""` | no |
| object\_source | Path to a file that will be read and uploaded as raw bytes for the object content. | `string` | `""` | no |
| tags | n/a | `map(string)` | `{}` | no |
| target\_bucket | n/a | `string` | `""` | no |
| target\_prefix | n/a | `string` | `""` | no |
| versioning | Versioning object into bucket (true or false). | `string` | `"false"` | no |

## Outputs

| Name | Description |
|------|-------------|
| bucket\_arn | ARN of the bucket. |
| bucket\_id | Name of the bucket. |

