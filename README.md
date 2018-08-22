# DSE
A project using Vagrant, Ansible & Virtualbox to create a Datastax Enterprise and OpsCentre environment

# Getting Startsed

```
git clone https://github.com/rhysmeister/DSE.git
cd DSE
vagrant up
```
The services must be started manually by logging into the VM. Some alises have been created to assist this;

```
dse; # Start Datastax Enterprise
ops; # Start OpsCenter
agent; # Start the Datastax Agent
```

You should be be able to access OpsCenter from the following url; http://localhost:8888/
