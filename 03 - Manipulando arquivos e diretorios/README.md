# Comandos de Ajuda

## Exercícios dos slides

<br>

> Navegando por diretórios

> Pathnames

+ Vá para o diretório etc, dentro do diretório raiz;
~~~sh
$ cd /etc
~~~

Agora vá para o diretório proc, dentro do diretório raiz;
~~~sh
$ cd proc
~~~

Vá para o diretório games, dentro do diretório usr/;
~~~sh
$ cd usr/games
~~~

Volte para o diretório home/$USER/.
~~~sh
$ cd home/$USER/
~~~

<br>

> Listando arquivos em um diretório

> Arquivos ocultos

+ Liste os arquivos do diretório /home/$USER;
~~~sh
$ ls /home/$USER
~~~

+ Agora exiba os arquivos ocultos do mesmo diretório.
~~~sh
$ ls -a /home/$USER
~~~

<br>

> Exibindo informações dos arquivos

+ Exiba as informações dos arquivos contidos no diretório
/home/$USER/;
~~~sh
$ ls -l /home/$USER/
~~~

+ Exiba as informações do arquivo .profile
~~~sh
$ ls -l /home/$USER/.profile
~~~

+ A quem o respectivo arquivo pertence?


<br>

> Exibindo informações de um diretório

+ Exiba as informações dos arquivos contidos em /usr/local/
~~~sh
$ ls -l /usr/local/
~~~

+ Agora exiba as informações do diretório /usr/local/
~~~sh
$ ls -ld /usr/local/
~~~

+ A quem pertence o diretório?

<br>

> Modo human

+ Qual o tamanho do arquivo /bin/bash/ em Megabytes?
~~~sh
$ ls -lh /bin/bash
~~~

+ Agora, qual o tamanho do diretório /bin/ ?
~~~sh
$ ls -ldh /bin/
~~~

+ Extra: pesquise sobre o comando du
~~~sh
$ man du
~~~

<br>

> Modo recursivo

+ Exiba o conteúdo de /usr/ e seus subdiretórios

~~~sh
$ ls -R /usr/
~~~

<br>

> Ordenando os arquivos

+  Ordene os arquivos contidos no diretório /usr/ por
tamanho, exibindo os seus tamanhos em kb ou mb;
~~~sh
$ ls -lSh /usr/
~~~

+ Ordene os arquivos contidos no diretório /usr/ por data de
modificação;
~~~sh
$ ls -ltr /usr/
~~~

+ Inverta a ordem de ordenação das questões anteriores.
~~~sh
$ ls -lt /usr/
~~~

<br>

> Criando arquivos e diretórios

+ Crie um diretório com seu nome dentro do diretório /tmp/
~~~sh
$ mkdir /tmp/adelson
~~~

+ Agora dentro do diretório com seu nome, crie uma árvore de diretórios da seguinte forma: diretório1/diretório2/diretório3;
~~~sh
$ cd /tmp/adelson/
$ mkdor -p diretório1/diretório2/diretório3
~~~

+ Dentro do diretório3 crie dois diretórios de mesmo nível hierárquico: subdiretório31 e subdiretório 32
~~~sh
$ cd diretório1/diretório2/diretório3
$ mkdir subdiretório31
$ mkdir subdiretório32
~~~

+ Crie um arquivo com o nome exemplo.txt dentro do diretório com seu nome.
~~~sh
$ cd /tmp/adelson
+ touch exemplo.txt
~~~

+ Agora atualize o horário do arquivo exemplo.txt para a data: 18/09/2030 16:50
~~~sh
$ touch -t 203009181650 exemplo.txt
~~~

<br>

> Deletando arquivos e diretórios

+ Remova o diretório que você criou;
~~~sh
$ cd /tmp/
$ rm -rv adelson
~~~

+ Agora crie novamente o diretório e, dentro dele, crie um
arquivo exemplo.txt;
~~~sh
$ mkdir adelson
$ touch exemplo.txt
~~~

+ Remova o arquivo exemplo.txt
~~~sh
$ rm exemplo.txt
~~~

<br>

> Copiando arquivos

+ Copie o diretório que você criou com o seu nome+cópia;
~~~sh
$ cd /tmp/
$ cp -rv adelson/ adelsoncopia/
~~~

+ Crie o arquivo exemplo2.txt no diretório com seu nome;
~~~sh
$ touch adelson/exemplo2.txt
~~~

+ Copie este arquivo para o diretório nome+cópia
~~~sh
$ cp -v adelson/exemplo2.txt adelsoncopia/
~~~

<br>

> Movendo arquivos

+ Mova o diretório nome+cópia para o diretório com seu
nome;
~~~sh
$ mv -v adelsoncopia/ adelson/
~~~

+ Renomeie o seu diretório, acrescentando o seu
sobrenome.
~~~sh
$ mv -v adelson/ adelsonjunior/
~~~

<br>

> Criando hard e soft links

+ Crie um arquivo com o nome teste;
~~~sh
$ touch teste
~~~

+ Crie um hardlink e um softlink para eles;
~~~sh
$ ln teste teste_link
~~~

+ Agora utilize o comando ls –i para mostrar os endereços dos inodes dos arquivos.
~~~sh
$ ls -i
~~~



