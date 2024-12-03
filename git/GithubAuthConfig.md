# Github Auth Config

## SSH Public Key (Better)

Get your public key at `~/.ssh/*.pub`, and fill public key to `Github->Settings->SSH and GPG keys`
```Bash
# If you don't have a ssh public key, use kengen to generate one
ssh-keygen -t rsa -C "xxx@xxx.com"
# Check availability
ssh -T git@github.com
# Please clone repo with SSH URL
git clone git@github.com:your_account/repo.git
```
> If some SSH keys you do not use anymore, delete them at `Github Settings` to keep safety. 

## Access Token

Go to `Github->Settings->Developer Settings->Personal Access Tokens->Tokens(Classic)` and create an access token. And create a file at `~/.netrc` content as follow.

```Bash
machine github.com
login your_account
password your_access_token
```