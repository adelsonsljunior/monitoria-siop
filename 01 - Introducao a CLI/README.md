# Introdução a interface da linha de comando (CLI)

## Exercícios dos slides

<br>

> Pesquisando o local dos comandos

- Pesquise onde está localizado o comando ls

~~~sh
$ which ls
~~~

- Pesquise onde está localizado o comando which

~~~sh
$ which which
~~~

<br>

> Comando history

- Digite os seguintes comandos:
pwd;
date;
ls –l /usr;
whoami;
history;
clear;

~~~sh
$ pwd
$ date
$ ls –l /usr
$ whoami
$ history
$ clear
~~~

- Agora, usando as teclas direcionais, reexecute o comando date.

~~~sh
$ date
~~~

- Limpe o histórico

~~~sh
$ history -c
~~~

- Digite novamente os comandos do exercício anterior

~~~sh
$ pwd
$ date
$ ls –l /usr
$ whoami
$ history
$ clear
~~~

- Agora, através do comando !*, execute novamente date
~~~sh
$ !*
~~~

<br>

> Comando Echo

- Utilize o echo para imprimir a seguinte cadeia de strings: “olá, sou o echo”

~~~sh
$ echo "olá, sou o echo"
~~~

- Agora execute as seguintes fórmulas lógicas e aritméticas:
    - 2 + 3
    - 2 > 3
    - 2 <= 3
    - 2 != 3
    - 2 == 3
    - 2 & 3
    - 2 | 3

~~~sh
$ echo $((2 + 3)) # ou echo $[2 + 3]
$ echo $((2 > 3)) # ou ~~echo $[2 > 3]
$ echo $((2 <= 3)) # ou echo $[2 <= 3]
$ echo $((2 != 3)) # ou echo $[2 != 3]
$ echo $((2 == 3)) # ou echo $[2 == 3]
$ echo $((2 & 3)) # ou echo $[2 & 3]
$ echo $((2 | 3)) # ou echo $[2 | 3]
~~~

<br>

> Comando expr


- Utilize o expr para realizar as seguintes operações:
    - 2 + 2
    - 2 – 2
    - 2 = 2
    - 2 != 2
~~~sh
$ expr 2 + 2
$ expr 2 - 2
$ expr 2 = 2
$ expr 2 != 2
~~~

- Utilize a seguinte frase para este exercício: “Eu amo linux”;
1. Compare a frase com as palavras: “Eu” e eu;

~~~sh
~~~

2. imprima somente a palavra linux;
~~~sh
expr substr "Eu amo linux" 8 7
~~~

3. Conte o número total de strings;
~~~sh
$ expr length "Eu amo linux"
~~~

<br>

> Variáveis do shell

- Crie uma variável de nome VARIAVEL1, que contem o
seguinte: “sou o clone de $HOME”
~~~sh
$ VARIAVEL1="sou o clone de $HOME"
~~~

- Imprima o conteúdo da VARIAVEL1
~~~sh
$ echo $VARIAVEL1
~~~

- Inicie um novo shell digitando bash
~~~sh
$ bash
~~~

- Imprima o conteúdo da VARIAVEL1
~~~sh
echo $VARIAVEL1
~~~

- Volte para o bash anterior com o comando exit
~~~sh
$ exit
~~~

- Adicione o seguinte conteúdo na VARIAVEL1: mas sou um clone fake
~~~sh
$ VARIAVEL1="sou o clone de $HOME mas sou um clone fake"
~~~

- Torne a VARIAVEL1 global
~~~sh
$ export VARIAVEL1
~~~

- Execute o seguinte comando: printenv | grep VARIAVEL1
~~~sh
$ printenv | grep VARIAVEL1
~~~

- Inicie um novo bash
~~~sh
$ bash
~~~

- Imprima a VARIAVEL1
~~~sh
$ echo $VARIAVEL1
~~~

- Exclua a VARIAVEL1
~~~sh
$ unset $VARIAVEL1
~~~

<br>

> Aliases (Apelidos)

- Crie o aliase lh para o comando ls -Shl

~~~sh
$ alias lh='ls -Shl'
$ lh
~~~

<br>

> Metacaracteres

- Vá para o diretório /usr/bin
~~~sh
$ cd /usr/bin
~~~

- Liste todos os arquivos que terminam com “e”
~~~sh
$ ls *e
~~~

- Liste todos os arquivos que terminem entre os caracteres “a” e “d”
~~~sh
$ ls *.a && ls *.d
~~~

- Liste todos os arquivos com a extensão .sh e .g???
~~~sh
$ ls *.sh && ls*.g
~~~

<br>

> Aspas duplas

- Imprima a seguinte linha de texto usando aspas duplas: Todos os arquivos * do Linux encontram-se nos seguintes diretórios: $PATH
~~~sh
$ echo "Todos os arquivos * do Linux encontram-se nos seguintes diretórios: $PATH"
~~~

<br>

> Aspas simples

- Imprima a linha de texto do exercício anterior usando aspas simples.
~~~sh
$ echo 'Todos os arquivos * do Linux encontram-se nos seguintes diretórios: $PATH'
~~~

<br>

> Aspas invertidas

- Imprima a seguinte frase: Hoje é dia date
~~~sh
$ echo "Hoje é dia `date`"
~~~

<br>

> Declarações de controle

- Imprima os meses de novembro e dezembro de 2022; Para tanto, utilize o comando cal mês ano.

~~~sh
$ cal 11 2022
~~~
