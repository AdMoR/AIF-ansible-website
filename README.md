# Deployment script for AIF website and Helpbot

The link of the deployed repos are :
[Webserver](https://github.com/AdMoR/Alliance_industrie_futur),
[Slack bot](https://github.com/AdMoR/helpbot_AIF)

The script deploys both repositories behind a nginx.
Required packets are installed for python.

An overview of the finished deployment is : http://jeunes-industrie-du-futur.fr


To deploy :
- Set up the ip adress of the host in
inventory/hosts
- Run `ansible-playbook -s playbooks/cf-dev.yml --ask-pass --user=xxxx --extra-vars "ansible_sudo_pass=xxxx"`

You need to provide the right token for the slack bot in playbooks/vars

/!\ You need to have python installed on the distant host to be able to run the script /!\