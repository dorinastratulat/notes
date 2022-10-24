- use [[S3]] to host static websites
  - .html sites / [[Static Site Generator|SSG]]
- [[S3]] scales automatically to meet demand
- put static sites on [[S3]] when large demand is expected
- make a static site:
  1. uncheck block public access
  2. Bucket -> Properties -> Static website hosting -> Enable
  3. set index and error documents
  4. upload files to the bucket
  5. Permissions -> Bucket policy -> Allow * principal to read `BUCKET/*`

Review:
- static website = [[S3]]
- bucket policies act on bucket level
- static content only
- automated scaling