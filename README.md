# DSE
A project using Vagrant, Ansible & Virtualbox to create a Datastax Enterprise (single node) and OpsCentre environment.

# Getting Startsed

```
git clone https://github.com/rhysmeister/DSE.git
cd DSE
```

Then get tar bundles for Datastax Enterprise, OpsCenter and Datastax Agent from http://downloads.datastax.com/enterprise/

Place them in <project root>/archives/

The files used at the time of writing are...

```
dse-6.0.2-bin.tar.gz
opscenter-6.5.2.tar.gz
datastax-agent-6.5.2.tar.gz
```
Now the VM is ready to be fired up...

```
vagrant up
```
The services must be started manually by logging into the VM. Some aliases have been created to assist this;

```
vagrant ssh
dse; # Start Datastax Enterprise
ops; # Start OpsCenter
agent; # Start the Datastax Agent
```

You should be be able to access OpsCenter from the following url; http://localhost:8888/
