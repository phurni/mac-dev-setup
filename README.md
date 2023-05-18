# mac-dev-setup

This script and playbook installs and configures most of the software I use on my Mac for web and software development.

## Credits

The material you'll find here is a mix from my own production and the ones found in these sources:
 
 - https://github.com/thoughtbot/laptop
 - https://github.com/axinorm/macbook-setup
 - https://github.com/geerlingguy/mac-dev-playbook

## How to run

### bootstraping

You have to run the `bootstrap_ansible` script found here to install a minimum setup that may run _ansible_.

If your current macOS setup doesn't have `git`, get and run the script like this (skip if you have `git`):

    curl --remote-name https://raw.githubusercontent.com/phurni/mac-dev-setup/master/bootstrap_ansible
    sh bootstrap_ansible

Having `git`, clone the repo and run the script:

    cd ~ && git clone https://github.com/phurni/mac-dev-setup.git && cd mac-dev-setup
    ./bootstrap_ansible

## Manual steps

Usually there's no need for manual steps before running the scripts.

However you'll find below usefull steps listed as a reminder.

### Hostname

If you didn't choose a correct name for your computer when installing,
open a terminal and run this to update it (replace `choose_your_machine_name` with your wish):

```
NEW_HOSTNAME=choose_your_machine_name
scutil --set HostName $NEW_HOSTNAME
scutil --set LocalHostName $NEW_HOSTNAME
scutil --set ComputerName $NEW_HOSTNAME
dscacheutil -flushcache
```
