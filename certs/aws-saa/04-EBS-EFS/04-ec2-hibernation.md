# EBS & EFS 04 - EC2 Hibernation

- data is kept on disk with [[EBS]] when [[EC2]] instance is stopped or terminated
- if instance is terminated the root device vol will also be terminated
- [[hibernation]]
  - OS is told to perform [[hibernation]]
  - save contents of [[RAM]] to disk
- start out of [[hibernation]]
  - [[EBS]] volume restored to previous state
  - [[RAM]] contents are reloaded
  - processes running are resumed
  - previously attached data volumes are reattached 
- instance boots faster
  - long running processes
  - services that take time to initialize
- [[RAM]] must be < 150 GB