---
sidebar_position: 4
---

# rclone

[rclone](https://rclone.org/) is a free tool for manging files and folders on cloud storage on Windows, macOS, linux and FreeBSD. This includes protocols including S3 compatible Object Storage.

Please follow the installation instruction like described on [rclone](https://rclone.org/downloads/). We generally recommend using the latest stable release from there and __not__ installing rclone via your distro's package manager. E.g. the download/upload speed can suffer from older rclone versions.

All you will need is:

* `access_key`
* `secret_key`
* Contabo's S3 URL

For `access_key`, `secret_key` and the S3 URL please check [here](/docs/products/Object-Storage/s3-connection-settings).

## Configuration for Contabo's S3 compatible Object Storage

### Example values

* `access_key` = 82046e8110804a43bf29c1ae426a724d
* `secret_key` = 82e69bd7a52076c527154297a76c2233
* S3 URL = https://eu2.contabostorage.com

### Steps

1. run `rclone config`
2. specify `n` for `n) New remote`
3. specify a name, e.g. `eu2`
4. specify `5` for `Amazon S3 Compliant Storage Providers including AWS, Alibaba, Ceph, Digital Ocean, Dreamhost, IBM COS, Minio, SeaweedFS, and Tencent COS`
5. specify `3` for `Ceph Object Storage`
6. speficy `1` for `Enter AWS credentials in the next step.`
7. specify your access_key, e.g. `82046e8110804a43bf29c1ae426a724d` for `access_key_id`
8. specify your secret_key, e.g. `82e69bd7a52076c527154297a76c2233` for `secret_access_key`
9. press `return` to skip `region`
10. specifiy the S3 URL, e.g. `https://eu2.contabostorage.com` for `endpoint`
11. press `return` to skip `location_constraint`
12. press `return` to skip `acl`
13. press `return` to skip `server_side_encryption`
14. press `return` to skip `sse_kms_key_id`
15. specify `n` for `Edit advanced config`
16. specify `y` for `Yes this is OK (default)`
17. optionally specify `q` to quit configuration mode

### rclone config

```conf
[eu2]
type = s3
provider = Ceph
access_key_id = 82046e8110804a43bf29c1ae426a724d
secret_access_key = 82e69bd7a52076c527154297a76c2233
endpoint = https://eu2.contabostorage.com/
```

### Usage

Please specify `--s3-no-head` when doing copies or synchronizations to avoid messages like `corrupted on transfer: sizes differ xxx vs 0`. Like the following:

```bash
rclone sync -P . eu2:bucketname/folder --s3-no-head
```
