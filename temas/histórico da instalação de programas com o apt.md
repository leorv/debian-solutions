`history | grep -E '(sudo )?apt'`

lista de tudo que foi instalado com o apt install:

```
zgrep 'apt install' /var/log/apt/history.log* | awk -F 'install( -y)?' '{print $2}' | tr ' ' '\n' | tr -s '\n' | sort
```

O zgrep é pra fazer o grep em arquivos gz recursivamente.


