# Project 22 - S3 Log Archive with Lifecycle

## Goal

Lower storage costs using Amazon S3 Lifecycle Rules.

## Files

- server.log
- lifecycle.json

## Tasks Completed

- Created S3 bucket
- Uploaded log file
- Configured lifecycle expiration policy
- Verified lifecycle rule in AWS Console

## Bucket

```text
project22-logarchive-1795257277
```

## Uploaded Object

```text
server.log
```

## Lifecycle Rule

```text
ExpireLogsAfter30Days
```

## Lifecycle Configuration

```json
{
  "Rules": [
    {
      "ID": "ExpireLogsAfter30Days",
      "Status": "Enabled",
      "Filter": {
        "Prefix": ""
      },
      "Expiration": {
        "Days": 30
      }
    }
  ]
}
```

## Verification

Lifecycle rule successfully configured and verified through:

AWS Console → S3 → Bucket → Management → Lifecycle Rules

## Deliverables

- Lifecycle Rule Screenshot
- S3 Management Console Screenshot
