# ingryd-ansible-project
Ansible project from ingryd academy.

1. Install ansible
```
sudo apt-get install ansible -y
```

2. Test and establish ansible connection to all the servers
```
ansible all -m ping
```

> all means all hosts

3. Gather info about the servers
```
ansible all -m gather_facts
```

4. Gather facts expect a server
```
ansible all -m gather_facts --limit 192.168.122.33
```

AD HOC COMMANDS WITH ELEVATED PRIVILEGES
===
5. Update server
```
ansible all -m apt -a update_cache=true --become --ask-become-pass
```
> --become (same as sudo)
> --ask-become-pass (asks for password)
