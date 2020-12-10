
# HTTPS Username & Password
1) Create an IAM user with CodeCommitFullAccess.
2) Navigate to the IAM console -> IAM user -> Security Credentials 
3) Select "Generate Credentials" under HTTPS Git credentials for AWS CodeCommit
4) Copy the 'user-name' and 'password'. Else, Download the credentials

Resources: https://docs.aws.amazon.com/codecommit/latest/userguide/setting-up-gc.html#setting-up-gc-account

# HTTPS Credential Helper

1) Configure the machine with the IAM user which has the HTTPS credentials
2) Run the below commands 

```
git config --global credential.helper '!aws codecommit credential-helper $@'
git config --global credential.UseHttpPath true
```

Resources:https://docs.aws.amazon.com/codecommit/latest/userguide/setting-up-https-unixes.html#setting-up-https-unixes-account


The storage format is a .git-credentials file, stored in plaintext.

If this is not an acceptable security tradeoff, try git-credential-cache as a more secured practice [2].

git config credential.helper cache <timeout>

This takes an optional timeout parameter, determining for how long the credentials will be kept in memory. Using the helper, the credentials will never touch the disk and will be erased after the specified timeout. The default value is 900 seconds (15 minutes).

However, If you use the SSH transport for connecting to remotes, it’s possible for you to have a key without a passphrase, which allows you to securely transfer data without typing in your username and password, which is also recommended. 

