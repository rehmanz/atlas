# Atlas
Atlas is a tool for managing secrets for cloud environments


## Setup Git Secrets
* Install [git-secret](https://git-secret.io/installation)
* Setting up [git-secret in repository](https://git-secret.io/)
* Generate and add your gpg key
```commandline
gpg --gen-key
gpg --list-secret-keys
git secret tell <email@domain.com>
```

* Create a `dev` environment manually from GitHub UI

## Populating Git Secrets

* Install and authenticate GitHub CLI
```commandline
gh auth login
```

* Set an individual secret
```commandline
gh secret set -e dev MYSECRET -b "foo"
```

* Setup secrets from a file
```commandline
gh secret set -e dev -f <source-file>
```
