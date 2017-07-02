## Ansible Role: Common
Este playbook realiza uma configuração inicial para sistemas operacionais CentOS7 onde instala os pacotes necessários e configura alguns arquivios de configuração como.
- sshd_conf
- bashrc
- vimrc
- e outros

### Variáveis:
Com esta variavel você pode preparar sua máquina para instalar os seguintes pacotes e entre outros, adionando o nome do pacote como o exemplo abaixo. veja vars/main.yml

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

### Pré requisitos:
None

### Sistema Operacional
CentOS7

### Autor
[Fabio Coelho](http://github.com/fcruzcoelho)


