# osu-connection-tester

This project is created to check if network connection of OpenStack is good enough to use BOSH and etc.

# What it does?

It clones recursively BOSH repo to the VM which IP you specify in `hosts` file.

# Requirements

1. Install ansible 1.9.2 (here are [details](http://docs.ansible.com/intro_installation.html)):

  ### For Mac OS
  ```
  brew install ansible
  ```
  ### For Ubuntu
  ```
  sudo pip install ansible
  ```

1. Create Ubuntu 14.04 LE instance with ssh access from your host VM.

# How to run

```bosh
git clone https://github.com/allomov/osu-connection-tester.git
cd osu-connection-tester
cp hosts{.example,}
vi hosts   # edit inventory file by chenging x.x.x.x to IP of your VM
ansible-playbook osu-connection-tester.yml
```

That's it!
