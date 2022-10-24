- automates moving objects between different tiers
  - maximizes cost effectiveness
  - example:
    - \[0, 30) days    -> [[S3]] Standard
    - \[30, 90) days   -> [[S3]] IA
    - \[90, +inf) days -> Glacier
- combine lifecycle management with versioning
  - different versions in different storage tiers

Review:
- use in conjunction with versioning
- applied to current versions and previous versions