Referência: https://www.youtube.com/watch?v=mi0vwVsfzGA


Primeiramente, criar o arquivo para ser o disco virtual.
Este arquivo é um "raw", ou seja, cru, cheio de zeros. Vamos fazer isso como root, ok.

```
dd if=/dev/zero of=disco-virtual bs=16M count=10000 status=progress
```

Depois, podemos mover ele para o diretório /

```
mv disco-virtual /
```

## Criando o disco virtual

com a ferramenta fdisk, ou qualquer uma de sua preferência (pode ser o gparted):

```
fdisk disco-virtual
```

Se tiver dúvidas, é aos 24 min do vídeo em epígrafe.

Caso tenha também curiosidade em ver como ficou:

```
xxd disco-virtual | less
```

Eu não tenho um dispositivo no momento, e para ficar fácil, vamos criar um:

```
losetup -P /dev/loop1 disco-virtual
```

Para verificar:

```
fdisk -l

resultado:

...outros dados...  
  
Disco /dev/loop1: 156,25 GiB, 167772160000 bytes, 327680000 setores  
Unidades: setor de 1 * 512 = 512 bytes  
Tamanho de setor (lógico/físico): 512 bytes / 512 bytes  
Tamanho E/S (mínimo/ótimo): 512 bytes / 512 bytes  
Tipo de rótulo do disco: dos  
Identificador do disco: 0x373dfe27

Dispositivo  Inicializar Início       Fim   Setores Tamanho Id Tipo  
/dev/loop1p1               2048 327679999 327677952  156,2G 83 Linux
```

Agora já podemos formatar.

```
mkfs.ext4 /dev/loop1p1
```

Montar a partição:

```
mount /dev/loop1p1 /mnt/

depois, pode dar um:
df -h
```


