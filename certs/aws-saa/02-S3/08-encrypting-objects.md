- types of [[encryption]]:
  - [[encryption]] in transit
    - [[Secure Sockets Layer|ssl]]/[[Transport Layer Security|tls]]
    - [[https]]
  - [[encryption]] at rest: server side
    - SSE-[[S3]]  - [[S3]]-managed keys, [[AES]] 256-bit
    - SSE-[[KMS]] - [[KMS|Key Management Service]]-managed keys
    - SSE-C   - Customer-provided keys
  - [[encryption]] at rest: client side
    - encrypt manually before upload to [[S3]]
- how to enforce?
  - enforce [[encryption]] in console
  - enforce [[encryption]] through bucket policy
- create policy that denies `PUT` that doesn't include the [[encryption]] header

```http
PUT
header:
x-amz-server-side-encryption: AES256  # s3  managed
x-amz-server-side-encryption: aws:kms # kms managed
```

Review:
- multiple [[encryption]] types
  - transit, rest SSE, rest CSE
- enforce with bucket policy
  - deny `PUT` requests without [[encryption]] header