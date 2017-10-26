# Ansible playbook for Kibana 5.6

## Install Ansible

1. Install Ansible using `sudo dnf install ansible` (Fedora) or `sudo yum install ansible` (CentOS)
1. Check that you have `libselinux-python` also installed in your system
1. Clone this repository using `git clone`
1. Restore submodules by running `git submodule init` and `git submodule update`

## Running this playbook and installing Kibana

1. Run `ansible-playbook -i inventory-local kibana-install.yml --ask-become-pass` for local testing
1. Run `ansible-playbook -i inventory kibana-install.yml` for deployment

## Uninstall Kibana

1. Run `sudo dnf remove kibana` (Fedora) or `sudo yum remove kibana` (CentOS)
1. More details [here](https://www.elastic.co/guide/en/kibana/current/rpm.html)