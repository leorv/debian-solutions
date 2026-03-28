É o interpretador de comandos padrão, o shell padrão do Debian GNU/Linux.

## Os comandos "*built in*" do Bash

São os comandos internos do bash.

Para ver a lista completa destes comandos, nós podemos utilizar o seguinte comando:

`help`

Para ver informações específicas:

`help nome_do_comando`

Se o retorno do comando acima for um erro, ele não é um comando interno do shell.

## Type

Outra forma de descobrir se o comando é um *built in* é com o type.

O comando type informa sobre o tipo de comando, mas informa principalmente como esse comando seria interpretado.

`type nome_do_comando`

Vamos ver alguns exemplos no terminal:

```
leonardo@predador:~/Documentos/aprendizado_linux$ type ls  
ls está apelidada para `ls --color=auto'
```

```
leonardo@predador:~$ type cd  
cd é um comando interno do shell
```

```
leonardo@predador:~$ type apt  
apt é /usr/bin/apt
```

Sempre que utilizarmos um comando *built in* do shell nós estaremos ganhando em processamento.

### O terminal como console interativo

Quando estamos dando comandos através do terminal, chamamos de modo interativo.

Quando estamos dando comando através de um arquivo, chamamos de modo não interativo.

Muitas linguagens oferecem consoles interativos onde você pode testar e executar trechos de seus programas.

No nosso caso, o emulador de terminal também pode ser visto como console interativo do bash/shell.

É importante que ele seja visto dessa forma a partir de agora.

O terminal será nossa principal ferramenta de trabalho e nosso melhor amigo.

## Como saber qual shell estamos utilizando

`echo $0`

Cuidado com o comando acima, porque ele mostra o nome do programa que está sendo executado. Não necessariamente o *bash*.

`echo $SHELL`

