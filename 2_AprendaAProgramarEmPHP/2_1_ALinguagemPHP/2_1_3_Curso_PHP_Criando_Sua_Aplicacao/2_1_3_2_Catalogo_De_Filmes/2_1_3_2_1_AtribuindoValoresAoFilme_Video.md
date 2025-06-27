Olá, pessoal! Boas-vindas a mais uma aula deste curso, onde estamos conhecendo o PHP.

Vamos começar a praticar. Como mencionamos na aula anterior, o PHP é normalmente utilizado no lado do servidor de aplicações web, conhecido como back-end. O front-end é executado no cliente — por exemplo, no navegador —, já o back-end é executado no servidor, local no qual o PHP está.

Com isso em mente, que tipo de aplicação poderíamos desenvolver? Pensemos em um aplicativo de streaming, como o Screen Match, que vamos desenvolver aqui. Ele é uma plataforma de streaming onde temos o conceito de filmes, séries, etc.

Um filme, por exemplo, terá informações como o ano de lançamento, uma descrição, seu nome, entre outras. Precisamos manipular essas informações no servidor para, por exemplo, recomendar para quem estiver assistindo a determinado filme, exibir as informações de um filme quando alguém clicar na foto dele, armazenar a foto desse filme e permitir o cadastro de novos filmes. Esse tipo de lógica, ou seja, de programa, é o que escrevemos utilizando o PHP.

Neste curso, não vamos efetivamente utilizar a web, mas vamos abordar a ideia de uma plataforma de filmes, que estamos chamando de Screen Match. Vamos pensar em algumas coisas que podemos precisar para trabalhar com filmes nesse programa. Podemos ter, por exemplo, o nome do filme, seu ano de lançamento e uma nota que as pessoas deram para esse filme.

Quando estamos falando de programação, precisamos manipular dados o tempo todo. Nos cursos de introdução à programação, já vimos o conceito de variáveis. Agora, vamos aprender a utilizar variáveis no mundo do PHP.

Utilizando variáveis no PHP
Vamos acessar o Visual Studio Code e fechar a aba do terminal, acessando-o e clicando no botão de "X" chamado "Close Panel", ou apertando "Ctrl+`".

Acessando o explorador lateral esquerdo, vamos clicar no botão "New File" à direita do nome da pasta do projeto para criar um novo arquivo chamado screen-match.php. Podemos chamá-lo como quiser, não tem problema.

Acessando o interior desse arquivo, vamos abrir a tag <?php, ou seja, indicar para o PHP que queremos escrever códigos. Pularemos duas linhas e vamos exibir uma mensagem com o echo dizendo "Bem-vindo(a) ao screen match!" para dar as boas-vindas a quem estiver utilizando o programa.

screen-match.php
```php
<?php

echo "Bem-vindo(a) ao screen match!";
```

Vamos executar isso. Abriremos novamente o terminal e digitaremos nele:

php screen-match.php
Copiar código
Ao executar, veremos o texto de boas-vindas como resposta.

Bem-vindo(a) ao screen match!

Fechando o terminal de novo e voltando ao código, queremos armazenar as informações do filme. Assim como aprendemos na introdução à programação, temos o conceito de variáveis que nos permite ter nomes para dados que vamos manipular no sistema.

Por exemplo, vamos trabalhar com o nome de um filme. Na linha 5, poderíamos ter o nome Top Gun - Maverick entre aspas. Colocaremos pontoa e vírgula no final, porque é assim que sempre terminamos as instruções do PHP.
```php
<?php

echo "Bem-vindo(a) ao screen match!";

"Top Gun - Maverick";
```

Durante a execução do programa, como armazenamos essa informação para enviá-la a outro lugar? E como sabemos que esse é o nome do filme?

Para isso, temos os nomes de variáveis. Vamos chamar esse texto de nomeFilme, adicionando essa variável à sua esquerda.

```php
<?php

echo "Bem-vindo(a) ao screen match!";

nomeFilme"Top Gun - Maverick";
```

Utilizamos o "N" minúsculo, pois normalmente começamos as variáveis com uma letra minúscula. Já o filme, que é uma nova palavra, iniciamos com o "F" maiúsculo.

Contudo, a sintaxe (ou seja, a forma de escrever) que seguimos está incompleta. Não parece que está tudo certo.

Para corrigir, vamos dar um espaço entre a variável e o nome, colocar um sinal de igual entre eles, e adicionar outro espaço.

```php
<?php

echo "Bem-vindo(a) ao screen match!";

nomeFilme = "Top Gun - Maverick";
```

Esse sinal de igual significa "recebe". O nome oficial dele é operador de atribuição. Com esse sinal, estamos dizendo que nomeFilme, seja lá o que isso for, recebe o valor do que estiver à direita — neste caso, o texto"Top Gun - Maverick.

Só que temos um último problema. Esse nomeFilme, somente da forma como ele está, não significa muita coisa no mundo PHP. Para indicar que isso é uma variável, antes do nome da variável, sempre colocamos um símbolo de cifrão.

```php
<?php

echo "Bem-vindo(a) ao screen match!";

$nomeFilme = "Top Gun - Maverick";
```
Agora sim, $nomeFilme recebe Top Gun - Maverick. Isso vai trazer para nós o texto Top Gun - Maverick para dentro dessa variável $nomeFilme. Podemos salvar e continuar armazenando outras informações.

Na linha seguinte, salvaremos por exemplo, o ano de lançamento. Para isso, vamos criar uma variável, digitando cifrão. O nome da variável vai ser $anoLancamento.

Importante: No PHP, assim como a maioria das linguagens, é interessante não utilizar caracteres especiais, como acentos e cedilha. Isso é uma convenção. Não quer dizer que o código não vai funcionar, mas há pessoas que trabalham com teclados de outros idiomas, que não possuem essas teclas em seus teclados e que podem executar nosso programa. Podemos facilitar a vida delas com essa estratégia.

O ano de lançamento desse filme foi 2022. Essa informação pode estar errada, mas não tem problema.

Finalizaremos a linha com ponto e vírgula no final.
```php
<?php

echo "Bem-vindo(a) ao screen match!";

$nomeFilme = "Top Gun - Maverick";
$anoLancamento = 2022;
```
Podemos perceber que, no anoLancamento, não temos aspas. Isso ocorre, pois o valor não é um texto, mas sim um número. Nós podemos lidar com números no PHP sem precisar das aspas.

Nos referimos a esse tipo de número, no mundo da programação e também da matemática, como um valor inteiro, porque não possui nenhuma casa decimal.

O que mais podemos armazenar? Por exemplo, na linha seguinte, vamos adicionar a nota do filme por meio de $notaFilme, com F maiúsculo. Vamos dizer que esse filme recebe 8.8 de nota.

$nomeFilme = "Top Gun - Maverick";
$anoLancamento = 2022;
$notaFilme = 8.8;

Nessa variável, temos um valor decimal, que no PHP, vamos chamar de double ou float.

Esse float significa que ele é um número de ponto flutuante. É uma forma de se representar números decimais na programação. Já double significa um número de ponto flutuante com precisão dupla.

Não precisamos gravar todas essas informações. Podemos até chamar esse valor de número decimal, se quisermos.

No PHP, os nomes de tipos vão ser utilizados em outros momentos, mas na hora de declarar a variável, não é necessário. Mesmo assim, é interessante saber o motivo e o nome deles.

Nesse momento, temos um texto, um inteiro e um float.

Existem outros tipos de dados. Por exemplo, sabemos se esse filme está incluso no plano da pessoa que está logada no sistema?

Vamos criar uma nova variável abaixo na próxima linha, chamada $incluidoNoPlano, com "N" e "P" maiúsculos para indicar que são palavras diferentes. Após o sinal de igual, podemos adicionar se é verdadeiro ou falso, ou seja, se está ou não incluído no plano.

O nome desse tipo de valor é booliano, que trabalha com verdadeiro ou falso, sim ou não — true ou false, conforme escrevemos no código.

Se queremos informar que ele está incluído no plano, ou seja, se esse valor booliano é verdadeiro, escrevemos true, que é verdadeiro em inglês.

$nomeFilme = "Top Gun - Maverick";
$anoLancamento = 2022;
$notaFilme = 8.8;
$incluidoNoPlano = true;

Se quiséssemos informar que ele não está incluído, diríamos que é false.

Podemos perceber que já utilizamos diversos tipos de dados no nosso código PHP.

Vamos pular uma linha e tentar exibir somente o nome do filme, nada mais, por meio do comando abaixo.

echo $nomeFilme;

Vamos abrir o terminal, executar o comando cls para limpá-lo e rodar o seguinte comando:

php screenmatch.php

No retorno, veremos um detalhe interessante, temos "Bem-vindo(a) ao screen match" e, na mesma linha, já estamos exibindo o nome do filme, sem quebra de linha.

Bem-vindo(a) ao screen match!Top Gun - Maverick

Isso é um detalhe que pode passar despercebido, mas a instrução echo vai enviar para a saída (no caso, o terminal) exatamente o que estamos mandando, ou seja, o texto "Bem-vindo(a) ao screen match!", sem quebra para uma nova linha.

Com isso, se tentamos exibir outra coisa logo depois, como é o caso do texto "Top Gun - Maverick", vamos exibir direto na mesma linha.

Podemos, dentre várias opções, adicionar um "Enter" entre o texto de boas-vindas e o ponto e vírgula, para criar uma quebra de linha, e salvar. No PHP os textos podem ter várias linhas sem problema.

```php
<?php

echo "Bem-vindo(a) ao screen match!"
;
```
Ao executar novamente, temos no terminal o texto "Bem-vindo(a) ao screen match!", e na próxima linha temos "Top Gun - Maverick".

Bem-vindo(a) ao screen match!

Top Gun - Maverick

Existe muita coisa que podemos e devemos falar sobre variáveis, mas estamos partindo do princípio, como já foi dito, que sabemos o básico de programação. Já sabemos, por exemplo, realizar operações com variáveis. Mesmo assim, Disponibilizaremos uma atividade "Para saber mais" sobre os tipos de dados e os operadores para esses tipos.

O código completo deste vídeo pode ser consultado abaixo.
```php
<?php

echo "Bem-vindo(a) ao screen match!"
;

$nomeFilme = "Top Gun - Maverick";
$anoLancamento = 2022;
$notaFilme = 8.8;
$incluidoNoPlano = true;

echo $nomeFilme;
```
Neste vídeo, vimos como utilizar variáveis, abordamos rapidamente os tipos de dados do PHP e falamos sobre a exibição dos textos. A seguir, vamos falar de forma mais aprofundada sobre os textos no cenário do PHP.
