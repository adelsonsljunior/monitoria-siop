# Edição e manipulação de arquivos – Pipes e Redirecionamento

## Exercícios dos slides

<br>

> O editor de textos NANO


+ Vá para o diretório documentos e crie um diretório com o nome: editor_textos;

~~~sh
$ cd ~/Documentos
$ mkdir editor_textos
~~~

+ Crie dois arquivos do tipo .txt com os nomes: bkp_passwd e bkp_login;

~~~sh
$ nano bkp_passwd.txt
$ nano bkp_login.txt
~~~

+ Dentro dos arquivos, coloque um título: Backup Password e Backup Login;

~~~
Backup Password
~~~

~~~
Backup Login
~~~

+ Salve os arquivos;

    + No arquivo bkp_passwd, pressione Ctrl+X para sair do editor nano. Quando for solicitado, pressione Y para confirmar o salvamento do arquivo.

    + No arquivo bkp_login, pressione Ctrl+X para sair do editor nano. Quando for solicitado, pressione Y para confirmar o salvamento do arquivo.

<br> 

+ Crie uma variável global em /home/user/.bashrc;

~~~sh
$ nano ~/.bashrc
~~~

Adicione a seguinte linha ao arquivo:
    
~~~sh
export VARIAVEL="VARIAVEL"
~~~ 

Salve o arquivo.

Pressione Ctrl+X para sair do editor nano. Quando for solicitado, pressione Y para confirmar o salvamento do arquivo.


+ Reinicie a sessão e imprima a variável;

~~~sh
$ bash 
$ echo $VARIAVEL
~~~

+ Agora edite novamente o arquivo retirando a variável;

~~~sh
$ nano ~/.bashrc
~~~

Retire a linha que foi adicionada no arquivo:
    
~~~sh
export VARIAVEL="VARIAVEL"
~~~ 

Salve o arquivo.

Pressione Ctrl+X para sair do editor nano. Quando for solicitado, pressione Y para confirmar o salvamento do arquivo.


+ Reinicie a sessão e imprima a variável.

~~~sh
$ bash 
$ echo $VARIAVEL
~~~

<br>

> Editor de textos VIM

+ Com o VI, insira o texto no arquivo exemplovi:

“O vi foi criado por Bill Joy em 1975 para o BSD. O nome é uma forma abreviada para
visual, um comando do editor de texto ex que o faz oferecer recursos parecidos com
os do vi. Em 1991, foi lançado o editor Vim, uma derivação melhorada do vi (o nome
Vim é abreviação para Vi IMproved, ou Vi Melhorado). Ele está presente em quase
todas as distribuições Linux, oferecendo mais recursos. Usuários do editor Emacs, que
também surgiu em 1975, acabam sempre gerando discussões com usuários mais
assíduos do vi por questões de gosto pessoal, apesar de que o padrão POSIX exige a
presença do editor vi o que o torna mais disseminado. Como é pequeno e leve, pode
ser colocado dentro de mídias com pouca capacidade de armazenamento para ser
utilizado em manutenção, por exemplo, ou mesmo usá-lo em situações em que há
pouco recurso computacional.”
Fonte: Wikipedia

~~~sh
$
~~~