## Ansible Role: Common
Este playbook realiza uma configuração inicial para sistemas operacionais CentOS7 onde instala os pacotes necessários e configura alguns arquivios de configuração como.
- sshd_conf
- bashrc
- vimrc
- e outros

### Variáveis: vars
Com esta variavel você pode preparar sua máquina para instalar os seguintes pacotes e entre outros, adionando o nome do pacote como o exemplo abaixo. veja [roles/common/vars/main.yml](roles/common/vars/main.yml)
```yaml
    yum_packages:
        - "@Development tools"
        - libselinux-python
        - bash-completion
        - dmidecode
        - traceroute
        - tcpdump
        - telnet
        - wget
        - mlocate
        - net-tools
        - lynis
        - iotop
        - iftop
```
### Pré requisitos:
None

### Inventário:
O playbook pega os hosts no arquivo padrão do ansible em /etc/ansible/hosts
```yaml
[CentOS]
192.168.33.10
192.168.33.11
```
### Playbook: playbook-common.yml
```yaml
---
 - hosts: all
   gather_facts: False
   remote_user: root
   roles: 
     - common
```
### Executando playbook
```yaml
sudo ansible-playbook playbook-common.yml -l foreman --tags=reboot --ask-pass
```
### Sistema Operacional
CentOS7

### Autor
[Fabio Coelho](http://github.com/fcruzcoelho)


