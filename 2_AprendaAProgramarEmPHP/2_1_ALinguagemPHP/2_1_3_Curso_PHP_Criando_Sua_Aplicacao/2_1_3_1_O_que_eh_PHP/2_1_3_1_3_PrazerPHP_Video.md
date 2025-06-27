Olá, pessoal! Boas-vindas de volta. Agora que já temos nosso ambiente configurado, vamos começar com um pouco de prática, e depois explicaremos melhor a teoria por trás do PHP.

Com o Visual Studio Code aberto, vamos abrir uma nova pasta. Para isso, clicamos em Open Folder (ou Abrir Pasta, se estiver em português). Selecionamos a pasta onde queremos criar nosso novo projeto e criamos uma nova pasta para este curso, que chamaremos de curso-PHP. Após criar a pasta, clicamos em Selecionar Pasta.

Com o primeiro passo concluído, algumas recomendações podem aparecer, mas não precisamos nos preocupar com isso agora, então fechamos a página de boas-vindas. Agora, ao lado do nome da pasta, no menu esquerdo, temos um botão que parece um sinal de mais e um arquivo, o New File. Clicamos nesse botão para criar um novo arquivo, que chamaremos de primeiro-programa.php.

A extensão .php é importante para o Visual Studio Code entender que se trata de um arquivo em PHP.

Para o PHP em si, isso não é tão importante, mas é sempre interessante que utilizemos a extensão .php para identificar para o nosso editor de código. Em configurações que já temos de outros programas que interagem com PHP, esse princípio já é presumido, eles já partem do princípio de que temos essa extensão de arquivo. Portanto, sempre utilizaremos a extensão .php.

É muito comum que o primeiro programa que escrevemos em qualquer linguagem seja exibir na tela a mensagem Hello World (Olá, Mundo). Então, vamos fazer isso em PHP. Digitamos Hello world!, sem nenhum comando, sem nenhum código. Salvamos com Ctrl + S e agora vamos abrir um terminal dentro do Visual Studio Code. Para isso, podemos fazer pressionando Ctrl + Shift + ´. Isso abrirá um terminal já na pasta correta, na pasta do nosso projeto.

Poderíamos abrir um terminal fora do VS Code e com o comando cd navegar até a pasta, mas é mais fácil abri-la diretamente no terminal.

Na pasta do projeto, podemos executar php primeiro-programa.php. Quando executamos, ele exibe para nós Hello world!. Reparem como é simples escrever um programa em PHP. Já escrevemos nosso primeiro programa, então agora vamos entender melhor o que estamos fazendo aqui.

Fazendo nosso primeiro programa com PHP
Se acessarmos o site oficial do PHP (php.net), observaremos que o PHP é uma linguagem de script de propósito geral popular, que é especialmente adequada para o desenvolvimento web. Ela é rápida, flexível e pragmática. O PHP potencializa tudo o que conseguimos fazer na web, desde um blog até os sites mais conhecidos do mundo.

O PHP é uma linguagem de programação de propósito geral, ou seja, podemos criar uma aplicação desktop em PHP, podemos utilizar PHP para fazer machine learning, isso tudo é possível e existem ferramentas para isso. Mas o PHP foi especialmente pensado para o desenvolvimento web.

A web funciona basicamente utilizando um protocolo chamado HTTP, e nesse protocolo temos a comunicação normalmente entre duas pontas: cliente e servidor.

Por exemplo, na comunicação com o site php.net, o cliente é o nosso navegador. Estamos utilizando um cliente HTTP para acessar um servidor que está nomeado como php.net. Esse servidor pode executar um programa lá dentro e nos devolver essa página que está exibindo as informações do PHP.

Esse ambiente do servidor que executa a lógica e que acessa dados é onde o PHP normalmente é executado, nos servidores web. Por exemplo, se postarmos uma foto no Instagram, o local onde essa foto foi armazenada e a lógica para saber para quem o Instagram vai exibir essa imagem, isso tudo é o que chamamos de servidor. E é nesse ambiente onde o PHP executa.

É o PHP que pode ver onde salvar essa imagem, para quem recomendar essa imagem. Quando curtimos a imagem, ele armazena o número de curtidas em algum lugar. O PHP é a linguagem que nos permite fazer esse tipo de coisa.

Neste curso, não vamos chegar nesse momento de web porque isso seria avançar um pouco mais. Mas vamos começar a entender a ideia por trás da linguagem PHP.

Embora no site oficial do PHP ele seja descrito como uma linguagem de script, não se deixem confundir:

PHP é uma linguagem de programação assim como qualquer outra que conhecemos, como Python, Java, Ruby, C++, C Sharp. É uma linguagem de programação completamente capaz de realizar tais tarefas gerais.

Com PHP, normalmente é dito que ela é uma linguagem interpretada, mas o que isso quer dizer na prática? Não precisamos rodar um processo de compilação para executar nosso código.

Como vimos, escrevemos um código e executamos. PHP, o nome do nosso arquivo, ele já executa na hora. Isso não quer dizer que ele vai lendo linha a linha do nosso programa. Ele é muito mais esperto que isso. Muita coisa acontece no plano de fundo. E o PHP compila o nosso código no plano de fundo, mas não precisamos nos atentar a esses detalhes de compilado, interpretado. Não é o momento ainda.

Voltando ao nosso código PHP, escrevemos somente um texto e o PHP exibiu esse texto para nós. Mas imaginem, se já sabem programar, vocês querem executar comandos, tomar decisões, saber se determinado valor é maior do que 20, por exemplo, fazer tal coisa, se for menor, fazer outra coisa. Então como podemos executar comandos se tudo que escrevermos o PHP vai exibir para nós?

Se queremos escrever código PHP e não somente texto, começamos o nosso arquivo com <?php. Quebramos linha para organizar o código. Podemos adicionar quantas quebras de linha quisermos. E depois vamos executar código PHP.

Para exibir algum texto em PHP, como podemos fazer? Vamos utilizar o comando, a função, como quiserem chamar, echo. Damos um espaço e entre aspas, podem ser aspas duplas ou aspas simples, colocamos nosso texto, nosso mesmo Hello world!. E no final de toda a instrução do PHP, precisamos do ponto e vírgula para indicar que aquela função acabou.

<?php

echo "Hello world!";

Salvamos novamente, abrimos o nosso terminal, limpamos a tela aqui com o comando cls (no Linux e no Mac é clear). E agora executamos de novo o mesmo programa. E temos exatamente o mesmo resultado, Hello world! sendo exibido.

C:\Users\carlo\Documents\code\curso-php>php primeiro-programa.php Hello world!

Se adicionarmos um ponto de exclamação aqui, salvamos, e executamos mais uma vez, vemos nossos dois pontos de exclamação sendo exibidos.

C:\Users\carlo\Documents\code\curso-php>php primeiro-programa.php Hello world!!

Então, instalamos o PHP, entendemos o que é PHP e onde normalmente ele é executado, e rodamos o nosso primeiro programa em PHP pelo terminal. Agora vamos entender como podemos gerenciar dados no PHP, e vamos entender qual é a aplicação que vamos construir durante este curso.

Esperamos vocês na próxima aula para conhecermos a aplicação com a qual vamos começar a trabalhar, e para conhecermos mais sobre essa linguagem maravilhosa que é o PHP.
