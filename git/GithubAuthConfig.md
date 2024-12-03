# Github Auth Config

## SSH Public Key

Get your public key at `~/.ssh/*.pub`, and fill public key to `Github->Settings->SSH and GPG keys`
```Bash
# If don't have a ssh public key, use kengen to generate one 
ssh-keygen -t rsa -C "xxx@xxx.com"
```

## Access Token

Go to `Github->Settings->Developer Settings->Personal Access Tokens->Tokens(Classic)` and create an access token. And create a file at `~/.netrc` content as follow.

```Bash
machine github.com
login your_account
password your_access_token
```