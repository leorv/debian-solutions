Se quisermos que um script seja executado a partir da invocação do nome do arquivo, o shell a ser utilizado terá que ser informado logo na primeira linha do código:

```
#!/bin/bash
```

Esta linha é chamada de *shebang, hashbang* ou, como eu prefiro, *linha do interpretador de comandos.*

Os caracteres #! no começo da primeira linha de um arquivo com permissão de execução são interpretados pelo kernel como uma instrução para executar o programa indicado na linha da *hashbang* utilizando o restante do conteúdo do arquivo como dados de entrada.

Uma forma que tem mais portabilidade:

```
#!/usr/bin/env bash
```

Mas tem ressalvas, nesta segunda, o programa env será encarregado de executar o bash, que buscará através da variável PATH, onde pode ser que haja um bash modificado e seja um programa malicioso. Acho isso um pouco exagerado, mas enfim.