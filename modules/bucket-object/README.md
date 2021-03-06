
# iam-bucket-object
Configure object upload for Amazon S3.

# Notes
For better code organization, `objects` files must be in the archive directory at the root of the module.

## Providers

| Name | Version |
|------|---------|
| aws | ~> 2.40 |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:-----:|
| bucket\_name | Name of bucket. | `string` | `""` | no |
| name | Bucket S3 name. | `string` | `""` | no |
| object\_key | The name of the object once it is in the bucket. | `string` | `""` | no |
| object\_source | Path to a file that will be read and uploaded as raw bytes for the object content. | `string` | `""` | no |
| tags | n/a | `map(string)` | `{}` | no |

## Outputs

| Name | Description |
|------|-------------|
| bucket\_object\_etag | ETag generated for the object (an MD5 sum of the object content). |
| bucket\_object\_id | Key of the resource supplied above. |