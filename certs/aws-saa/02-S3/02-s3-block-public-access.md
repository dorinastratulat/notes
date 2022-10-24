- object [[Access Control Lists|ACLs]]
  - work on individual object level
- bucket policy
  - work on entire bucket level
- [[S3]] console is global namespace
  - name has to be globally unique
- AWS [[region]] is where to deploy the bucket
- Default is to block public access
- Make objects public:
  1. Bucket -> Permissions -> Edit -> uncheck Block Public Access
  2. Bucket -> Permissions -> Object Ownership -> Edit -> enable ACLs
  3. Bucket -> Object -> Actions -> Make public using object ACL

Review:
- buckets are private by default
- [[Access Control Lists|ACLs]] are object level
- Bucket policies are bucket level
- uploading objects return [[HTTP]] 200 on success