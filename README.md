# SQL Server 2019 running in linux

Provisioning and running mssql-server in linux using vagrant + virtualbox + ansible

## Installation
First of all, you will need install according your SO:

1. [Vagrant](https://www.vagrantup.com/downloads.html)
2. [Virtualbox](https://www.virtualbox.org/wiki/Downloads)


## Usage
Open your terminal and go to path root project where vagrant file is and type the next command
```bash
vagrant up
```

## Recommendations
If something is wrong you can destroy the virtual typing and re-run the above command:
```bash
vagrant destroy -f
```
If you edit the playbook.yml file, type the next command to apply and test your own configuration: 
```bash 
vagrant provision
```

Connecting to virtual machine and playing with [sqlcmd utility](https://docs.microsoft.com/en-us/sql/tools/sqlcmd-utility?view=sql-server-linux-ver15)
```bash
vagrant ssh
```
[Read more](https://docs.microsoft.com/en-us/sql/linux/quickstart-install-connect-ubuntu?view=sql-server-linux-ver15)
