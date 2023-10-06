# Comandos de Ajuda

## Exercícios dos slides


<br>


> Chamada do man

+ Execute o comando date

~~~sh
$ date
~~~

+ Agora execute man date

~~~sh
$ man date
~~~

<br>

> Seções

+ Utilize o comando date para exibir a data nos seguintes formatos (utilize o man para coletar informações):
    + DD/MM/YY
    + DD-MM-YY
    + MM/DD/YY

~~~sh
$ date +%d/%m/%y
$ date +%d-%m-%y
$ date +%m/%d/%y
~~~

<br>

> Locais do Man

+ Pesquise quais man pages existem com o nome passwd e sua localização.

~~~sh
$ man -f pasaswd
~~~

<br>

> Comando Whatis

+ Faça o exercício anterior usando o comando whatis;

~~~sh
$ whatis passwd
~~~

<br> 

> Acessando um local específico

+ Exiba a man page passwd localizada na seção 5.

~~~sh
$ man 5 passwd
~~~

<br>

> Localizando man pages

+ Procure por comandos relacionados à palavra password.

~~~sh
$ man -k passwd
~~~

<br>

> O comando info

+ Procure pelo info do comando ls;

~~~sh
$ info ls
~~~

+ Agora, liste os arquivos contidos em /home/$USER ordenando-os por tamanho (do maior para o menor). Utilize o comando info para colher tais informações.

~~~sh
$ ls -S /home/$USER
~~~

<br>

> A opção Help

> Pesquisando por qualquer arquivo ou diretório

+ Pesquise pelo termo crontab
~~~sh
$ 
~~~

+ Liste a quantidade de arquivos na saída
~~~sh
$ 
~~~

+ Liste a quantidade de arquivos na saída que sejam nomeadas exclusivamente com o termo crontab.
~~~sh
$ 
~~~

+ Execute o man para crontab afim de obter informações.
~~~sh
$ man crontab
~~~

<br>

> Pesquisa utilizando o find

+ Da mesma forma que o anterior, pesquise pelo termo crontab no diretório /etc, exibindo seus detalhes com o comando ls –l.
~~~sh
$ find /etc -name crontab -type f -exec ls -l {} \;
~~~

+ Depois, utilizando o –exec insira: echo "achei o arquivo:".
~~~sh
$ find /etc -name crontab -type f -exec echo "achei o arquivo:" {} \; | ls -l
~~~

+ Agora, utilizando o comando man, verifique a função do crontab
~~~sh
$  man crontab
~~~

+ Tomando como base o que foi visto no man, programe o sistema para inserir em um arquivo a seguinte mensagem a cada dois minutos: A aula está acabando.
~~~sh
$ crontab -e
~~~

Este comando irá abrir o arquivo de crontab do usuário atual no editor de texto padrão.

No editor de texto, adicione a seguinte linha:

~~~sh
*/2 * * * * echo "A aula está acabando" > /tmp/aula_acabando
~~~