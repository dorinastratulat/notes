- 1 user = 1 person
- group users in groups by job function
- roles are for internal usage in AWS
  - ie. allow vms to access [[s3]] buckets
- best practice - user inherit permissions from groups
- principal of least privilege
  - assign minimum amount of privileges needed
  - no extra permissions
- only see auth information once, make sure to save it after creating a user
- [[IAM]] is universal, not apply to [[region]]s
- root acct is created on first setup and has complete admin access
  - don't use for day-to-day access
- creating a user comes with zero permissions
- access key id and secret key are used for programmatic access to AWS
- set up password rotation policy
- [[IAM]] federation -> Identity Federation -> [[Single Sign-on|SSO]] w/ [[SAML]]/[[OpenID]]