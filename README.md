# Ansible playbook for Kibana 5.6

## Install Ansible

1. Install Ansible using `sudo dnf install ansible` (Fedora) or `sudo yum install ansible` (CentOS)
1. Check that you have `libselinux-python` also installed in your system
1. Clone this repository using `git clone`
1. Restore submodules by running `git submodule init` and `git submodule update`
1. If Elasticsearch is deployed not on the same host, please change its host in `kibana_elasticsearch_url` variable in file `kibana/defaults/main.yml`

## Running this playbook and installing Kibana

1. Run `ansible-playbook -i inventory-local kibana-install.yml --ask-become-pass` for local testing
1. Run `ansible-playbook -i inventory kibana-install.yml --ask-pass --ask-become-pass` for deployment
1. The latter command will ask you for SSH user password and later sudo user password. If SSH user is not "root" please change the name in the `inventory` file

## Uninstall Kibana

1. Run `sudo dnf remove kibana` (Fedora) or `sudo yum remove kibana` (CentOS)
1. More details [here](https://www.elastic.co/guide/en/kibana/current/rpm.html)