# EBS & EFS 03 - Protecting EBS Volumes with Encryption

- [[EBS]] [[encryption]]
  - encrypt vols with data key using [[AES]]-256
  - uses AWS [[KMS]] customer master keys (CMK) when creating encrypted vols or snapshots
  - data at rest is encrypted
  - data in flight between instance and volume is encrypted
  - all snapshots are encrypted
  - all vols created from snap will be encrypted
  - end-to-end [[encryption]]
  - handled transparently
  - minimal impact on latency
  - copying unencrypted snapshot allows [[encryption]]
  - snaps of encrypted vols are encrypted automatically
  - encrypt the root device volume (OS disk)
- steps to encrypt an unencrypted vol
  - create snap of unencrypted root device vol
  - create a copy of snap and select encrypt option
  - create [[AMI]] from encrypted snap
  - use [[AMI]] to launch new encrypted instance

Review
- encrypted vols
  - data at rest and in flight is encrypted
  - snaps are encrypted
  - all vols created from snap are encrypted
- how to encrypt
  - create snap of unencrypted
  - create copy of snap select encrypt option
  - create [[AMI]] from snap
  - launch new instance with [[AMI]]

