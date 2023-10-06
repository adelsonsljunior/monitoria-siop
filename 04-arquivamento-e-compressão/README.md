# Arquivamento e Compressão

## Exercícios dos slides

<br>

> O comando tar

+ Crie dois diretórios, dentro de /tmp, cada um com 4 arquivos dentro;

~~~
$ mkdir /tmp/diretorio1 /tmp/diretorio2
$ cd /tmp/diretorio1 && touch arquivo1 arquivo2 arquivo3 arquivo4
$ cd /tmp/diretorio2 && touch arquivo1 arquivo2 arquivo3 arquivo4
$ cd /tmp
~~~


+ Com o comando tar , crie arquivos de backup para os diretórios criados (dica:
utilize a opção v para acompanhar a criação);

~~~
$ tar -cvf /tmp/backup-diretorio1.tar /tmp/diretorio1
$ tar -cvf /tmp/backup-diretorio1.tar /tmp/diretorio2
~~~

+ Remova os diretórios criados.

~~~
$ rm -rv /tmp/diretorio1
$ rm -rv /tmp/diretorio2
~~~

<br>

> Listando o conteúdo dos arquivos tar

+ Exiba o conteúdo dos backups criados;

~~~
$ tar -tf /tmp/backup-diretorio1.tar
$ tar -tf /tmp/backup-diretorio2.tar
~~~

+ Dica: utilize a opção v para exibir detalhes dos arquivos contidos em .tar

~~~
$ tar -tvf /tmp/backup-diretorio1.tar
$ tar -tvf /tmp/backup-diretorio2.tar
~~~

<br>

> Adicionando arquivos ao .tar


+ Crie um terceiro diretório com quatro arquivos dentro;

~~~
$ mkdir /tmp/diretorio3 && cd /tmp/diretorio3 && touch arquivo1 arquivo2 arquivo3 arquivo4
~~~

+ Adicione esse diretório ao arquivo de backup do primeiro diretório, realizado
no exercício 1;

~~~
$ tar -rvf /tmp/backup-diretorio1.tar /tmp/diretorio3
~~~

+ Remova o diretório 3;

~~~
$ rm -rv /tmp/diretorio3
~~~

+ Exiba o conteúdo do backup do primeiro diretório.

~~~
$ tar -tvf /tmp/backup-diretorio1.tar
~~~


<br>

> Extraindo arquivos .tar

+ Extraia o backup do diretório 1;

~~~
$ tar -xvf /tmp/backup-diretorio1.tar -C /tmp
~~~


+ Crie um quarto diretório e extraia o backup do diretório 2 nele.

~~~
$ mkdir /tmp/diretorio4
$ tar -xvf /tmp/backup-diretorio2.tar -C /tmp/diretorio4
~~~


<br>

> Comando gzip

+ Comprima o arquivo tar do backup do diretório 1

~~~
$ gzip -v backup-diretorio1.tar
~~~

+ Agora visualize o tamanho do arquivo tar compactado 

~~~
$ ls -lh /tmp/backup-diretorio1.tar.gz 
~~~

<br>

> Extraindo arquivos gzip

+ Extraia o backup do diretório 1;

~~~
$ gzip -dv backup-diretorio1.tar.gz
~~~


+ Agora visualize a diferença de tamanho entre o arquivo compactado e o não
compactado.

~~~
$ ls -lh /tmp/backup-diretorio1.tar
~~~


<br>

> Comando bzip2

+ Compacte o arquivo de backup do diretório 1 utilizando o bzip2;

~~~
$ bzip2 backup-diretorio1.tar
~~~

+ Visualize o seu tamanho.

~~~
$ ls -lh /tmp/backup-diretorio1.tar.bz2
~~~

<br>

> Extraindo arquivos bzip

+ Extraia o backup do diretório 1;

~~~
$ bzip2 -dv /tmp/backup-diretorio1.tar.bz2
~~~

+ Agora visualize a diferença de tamanho entre o arquivo compactado e o não
compactado.

~~~
$ ls -lh /tmp/backup-diretorio1.tar.
~~~

<br>

> Comprimindo arquivos tar diretamente

~~~
$ mkdir /tmp/diretorio1 /tmp/diretorio2 /tmp/diretorio3
$ cd /tmp/diretorio1 && touch arquivo1 arquivo2 arquivo3 arquivo4
$ cd /tmp/diretorio2 && touch arquivo1 arquivo2 arquivo3 arquivo4
$ cd /tmp/diretorio3 && touch arquivo1 arquivo2 arquivo3 arquivo4
$ cd /tmp
~~~

+ Compacte os diretórios 1, 2 e 3 em um arquivo de backup do tipo tar.gz;

~~~
$ tar -zcf /tmp/backup-diretorios.tar.gz diretorio1 diretorio2 diretorio3
~~~

+ Compacte os diretórios 1,2 e 3 em um arquivo de backup do tipo tar.bz2;

~~~
$ tar -jcf /tmp/backup-diretorios.tar.bz2 diretorio1 diretorio2 diretorio3
~~~

+ Visualize a diferença de tamanho entre eles.

~~~
$ ls -lh /tmp/backup-diretorios.tar.gz
$ ls -lh /tmp/backup-diretorios.tar.bz2 
~~~

<br>

> Extraindo o conteúdo

+ Extraia o conteúdo do backup tar.gz no diretório 4;

~~~
$ tar -xvf /tmp/backup-diretorios.tar.gz -C /tmp/diretorio4
~~~

+ Remova o conteúdo do diretório 4;

~~~
$ rm -rv /tmp/diretorio4/*
~~~

+ Extraia o conteúdo do backup tar.bz2 no diretório 4.

~~~
$ tar -xvf /tmp/backup-diretorios.tar.bz2 -C /tmp/diretorio4
~~~

<br>

> O comando zip

+ Dentro do diretório 4, arquive e compacte os diretórios de 1 a 3 em um
arquivo de backup.zip

~~~
$ cd /tmp/diretorio4
$ zip -r backup.zip /tmp/diretorio1 /tmp/diretorio2 /tmp/diretorio3
~~~

+ Agora liste o conteúdo do arquivo com a opção unzip –l

~~~
$ unzip -l backup.zip
~~~

Por fim, compacte o diretório /etc no arquivo bkpetc.zip e compare os
tamanhos do diretório e do diretório compactado.

~~~
$ zip -r /tmp/bkpetc.zip /etc
$ ls -lhd /etc
$ ls -lh /tmp/bkpetc.zip
~~~

<br>

> Extraindo o conteúdo de zip



Mova o arquivo de backup .zip para documentos;

~~~
$ mv -v /tmp/diretorio4/backup.zip ~/Documentos
~~~

+ Exclua todo o conteúdo do diretório 4;

~~~
$ rm -rv /tmp/diretorio4/*
~~~

Extraia o conteúdo do backup .zip para o diretório 4;

~~~
$ unzip ~/Documentos/backup.zip -d /tmp/diretorio4
~~~