## Jellyfin Server on Acorn

[Jellyfin](https://jellyfin.org/) is the volunteer-built media solution that puts you in control of your media. Stream to any device from your own server, with no strings attached. Your media, your server, your way. This Acorn demonstrates using Jellyfin with Wasabi as your online media storage.

## Wasabi
[Wasabi](https://wasabi.com/hot-cloud-storage/) is one of the most affordable online storage options available. You can store all of your media on it with as little as $6.99 TB/Month, with no egress charges.

## Using Jellyfin Acorn
If you have all your media on Wasabi s3 and you want to sync it with jellyfin to stream it, you **must** configure the Wasabi bucket details for the below parameters.
| Param  | Description  | Default Value |
|---|---|---|
|bucket_name | Wasabi bucket Name | NA |
| region | Bucket Region | us-east-1 |
| endpoint_url | Bucket URL | s3.wasabisys.com |
| access_key | S3 Access Key for your account | NA |
| secret_key | S3 Secret Key for your account | NA |

Optionally you can also configure below parameters, as needed.
| Param  | Description  | Default Value |
|---|---|---|
| storage | Jellyfin Storage volume size | "2G" |
| rclone_schedule | Bucket sync cron job schedule | "0 */6 * * *" i.e. Every 6 hours |