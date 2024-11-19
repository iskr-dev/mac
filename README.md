# Mac Provisioning
```commandline
xcode-select --install

/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> /Users/(username)/.zprofile

eval "$(/opt/homebrew/bin/brew shellenv)"

brew install ansible

mkdir Code

cd Code

git clone https://github.com/iskrmky/mac.git

ansible-playbook -i inventory/localhost localhost.yml --ask-become-pass --ask-vault-pass

conda init --all
```

## Note
Delete Pycharm data
```commandline
find ~/Library -iname "*pycharm*" -exec rm -r "{}" \;
```

Decrypt secret file
```commandline
ansible-vault decrypt secret.yml
```

Encrypt secret file
```commandline
ansible-vault encrypt secret.yml
```
