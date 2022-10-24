- [[S3]] replication
  - replicate objects from one bucket to another
  - versioning enabled on src and dest
  - objects are not replicated automatically
    - subsequent updated objects will be replicated after enabling replication
  - create src and dest at the same time
  - delete markers aren't replicated by default
    - can turn this on
  
Review:
- you can replicate objects across buckets
- objects in existing bucket are not replicated automatically
- delete markers are not replicated by default