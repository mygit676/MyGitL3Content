# Connect to CodeCommit via SSH

1) Navigate to the .ssh folder on your work-station [ cd~/.ssh ] 
2) Generate a public and a private key using the below command

ssh-keygen: https://man.openbsd.org/ssh-keygen.1

```
ssh-keygen -t rsa -b 2048 -C "nameofthekey"

```

-t : Specifies the type of key to create. The possible values are “dsa”, “ecdsa”, “ecdsa-sk”, “ed25519”, “ed25519-sk”, or “rsa”

-b : Specifies the number of bits in the key to create

-C : Provides a new comment


3)Copy the contents of the public key generated.Public key will be in the format of 'nameofthekey.pub'

4)Navigate to the IAM user from the AWS-console

5)Select our desired IAM user -> Security Credentials

6)Select "Upload SSH public key" under SSH keys for AWS CodeCommit

7)Paste the contents of the public key

8)We now see an SSH key ID generated. Take a note of this SSH Key ID

9)Navigate to our workstation

10)cd ~/.ssh

11)Create a config file [ vi config]

```
Host git-codecommit.*.amazonaws.com
  User APKAEIBAERJR2EXAMPLE
  IdentityFile ~/.ssh/<your privatekey>
```
The above essentially means that, for any host that starts with 'git-codecommit' and ends with 'amazonaws.com' , use the below User ID and the key for authntication

====
