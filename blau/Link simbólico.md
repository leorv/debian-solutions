
É muito raro eu copiar ou mover arquivos para o meu diretório *~/bin* ou qualquer outro diretório da variável *PATH*. Em vez disso, eu prefiro criar e fazer manutenção dos meus scripts nas pastas de seus respectivos projetos, para que eu possa executá-los de qualquer local, eu acho muito mais prático criar os *link simbólicos* apontando para os locais onde os scripts realmente estão.

```
ln -s ~/projetos/infos/infos.sh ~/bin/infos
```

Em sistemas *unix-like*