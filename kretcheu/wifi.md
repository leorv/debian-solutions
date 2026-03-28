# Wifi

## Investigando

lspci -nnkd::0280

Sites de busca: debian wiki xxxx:xxxx

grep firm /var/log/syslog | grep fail

Sabendo o nome do arquivo, pode pesquisar o pacote pelo nome. packages.debian.org

apt install ./firmware-FAB.deb

/etc/apt/sources.list -> incluir seção non-free

apt update

apt install firmware-FAB

### Recarregando...

modprobe -r nome-do-modulo

modprobe nome-do-modulo

dmesg | grep firm

### verificando...

ip a

ip address

ip l

ip link

iw dev interface scan

iw dev wlp5s0 scan

pacote: iw

