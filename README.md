# S3 file input plugin for Embulk

## Overview

* Plugin type: **file input**
* Resume supported: **yes**
* Cleanup supported: **yes**

## Configuration

- **bucket** S3 bucket name (string, required)
- **path_prefix** prefix of target keys (string, required)
- **endpoint** S3 endpoint login user name (string, optional)
- **access_key_id** AWS access key id (string, required)
- **secret_access_key** AWS secret key (string, required)

## Example

```yaml
in:
  type: s3
  bucket: my-s3-bucket
  path_prefix: logs/csv-
  endpoint: s3-us-west-1.amazonaws.com
  access_key_id: ABCXYZ123ABCXYZ123
  secret_access_key: AbCxYz123aBcXyZ123
```

For public S3 buckets such as `landsat-pds`:

```yaml
in:
  type: s3
  bucket: landsat-pds
  path_prefix: scene_list.gz
```

## Build

```
./gradlew gem
```

