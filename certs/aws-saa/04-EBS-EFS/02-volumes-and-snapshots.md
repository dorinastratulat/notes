# EBS & EFS 02 - Volumes and Snapshots

- volumes
  - volumes exist on [[EBS]]
  - virtual hard disk
  - >= 1 vol per [[EC2]] instance 
  - root device on [[EC2]] instance
  - always in the same [[Availability Zone|AZ]] as the [[EC2]] instance
  - resize on the fly
    - will need to extend the filesystem in the OS (resize2fs, etc.)
  - switch volume types on the fly
- snapshots
  - snapshots exist on [[S3]]
  - image of the virtual disk/volume
  - point-in-time copy of a volume
  - incremental/differential
    - only changed data since last snapshot will be captured
  - first snapshot may take time to create
  - tips
    - consistent snapshot - stop instance and take snapshot
    - encrypt snapshots
    - share snapshots in the same [[region]] they were created

Review
- vols on [[EBS]], snapshot on [[S3]]
- snap is point-in-time, incremental
- first snap will take time
- stop instance before snapshot
- share snaps between accounts and [[region]]s but need to copy to target [[region]] first
- resize [[EBS]] on the fly and change volume types