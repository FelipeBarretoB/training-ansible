# training-ansible

SHADOW WIZARD MONEY GANG; WE LOVE CASTING SPELLS

SO; we're using macOS because we're cool and we're using ansible because we're lazy.

so, we install ansible with pip:

```bash
pip install ansible
```

then, because of this line of code:

```yaml
172.191.115.133 ansible_user=azureadmin ansible_ssh_pass=**.
```
we need to install sshpass:

```bash
brew install hudochenkov/sshpass/sshpass
```

now, everything should work.

run:

```bash
ansible-playbook -i inventory/hosts.ini playbooks/install_docker.yml

ansible-playbook -i inventory/hosts.ini playbooks/run_container.yml

```

now, we can connect using ssh, and check if the container is running:

```bash
sudo docker ps
```

HOWEVER, because I'm cool and a software engineer, I cannot (for the life of me) understand network rules, so ask someone who does
then, you can connect to the container using the IP address and the port number.

use the vm's public address and the port number to connect to the container. the port number is 8787