# ansible-install-docker

This repo contains an ansible playbook + role to install docker and docker compose v2 (and optionally also v1).

There is a Vagrantfile that can be used to test this ansible playbook against Debian 10,11,12 and Ubuntu 18.04 (bionic), 20.04 (focal), 22.04 (jammy).

More details can be found here: https://srijan.ch/testing-ansible-playbooks-using-vagrant

## Run the vagrant test

The test can be run using:

```
vagrant up
```

If the boxes are already up, to re-run provisioning, run:

```
vagrant provision
```
