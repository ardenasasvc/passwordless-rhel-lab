# passwordless-rhel-lab

A repo to accompany my blog post about testing new passkey features in RHEL 9.4.

## about

not for prod use. set of ansible playbooks to deploy an idm server and client.


## requirements

- At least two hosts with RHEL 9.4+ 
- FIDO2-compliant passkey (tested with Yubikey 5C NFC)

## usage

Change the variables in inventory to something appropriate for your testing. Depending on your deployment configuration, you may wish to declare `ansible_host` IPs for your inventory to simplify setup.

Install the server:
```bash
ansible-playbook -i inventory.ini server/install-server.yml
```

Install the client:
```bash
ansible-playbook -i inventory.ini client/install-client.yml
```