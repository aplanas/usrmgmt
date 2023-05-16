# usrmgmt
Basic user management for duplicati backups

# Installation
In the backup server create a new user without login password.  This
user should only have access via a SSH key.  Generate one with
`ssh-key`, and register the public key under the
`.ssh/authorized_keys` file.

We should have access via SSH using the private key: `ssh -i id_rsa
user@server`.  We need to clone this repository under this user, so we
can send commands:

  ssh -i keys/id_rsa user@server usrmgmt/um -h
