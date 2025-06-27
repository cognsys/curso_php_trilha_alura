Falamos brevemente sobre operadores e tudo mais, porque isso é um assunto que já abordamos nos cursos de introdução à programação. Conseguimos observar que a sintaxe do PHP é bastante semelhante à linguagem que você já utilizou.

No entanto, existem alguns detalhes que são mais específicos de linguagem para linguagem. Cada linguagem tem sua particularidade quando o assunto é texto.

O tipo de dados que conhecemos até agora foram:

integer: para um número inteiro, como $anoLancamento;
float (ou double): para um número decimal, como $notaFilme;
boolean (ou booleano) : para verdadeiro ou falso, como $planoPrime.
E qual o nome do tipo de dados onde armazenamos texto? No PHP é string.

Trabalhando com textos
String é o nome do tipo de dados que armazena texto. Esse texto pode ser um único caractere ou um conjunto de caracteres.

No PHP, não existe um tipo específico para uma única letra, para um caractere. Algumas linguagens possuem isso. No PHP, tudo é string.

Podemos operar em uma string, ou seja, fazer diversas coisas em uma string. Inclusive, é possível realizar operações matemáticas em strings, porque o PHP tem o conceito de strings numéricas.

Strings numéricas
Como exemplo, vamos criar um novo arquivo chamado string-numerica.php. Vamos abrir a tag php e exibir o resultado da string 5 mais a string 10. Note que ambos estão entre aspas, pois são textos.

string-numerica.php:
```php
<?php

echo "5" + "10";
```
No terminal, vamos executar o arquivo com o comando:
```php
php string-numerica.php
```
```php
15
```
Tivemos o resultado 15. Portanto, se temos em uma string, ou seja, em um texto, apenas valores numéricos, e vamos realizar operações matemáticas com essa string, o PHP sabe realizar as operações.

Ele converte isso para um número e realiza as operações necessárias, mas isso pode ser perigoso em alguns casos. Contudo, é importante saber desse detalhe.

Caracteres de escape
A maioria das linguagens de programação possuem o conceito de caracteres de escape, que são caracteres que têm significados especiais. Por exemplo, uma quebra de linha.

No texto de boas-vindas, adicionamos literalmente uma quebra de linha, pressionando "Enter". Mas, às vezes, queremos deixar o código mais organizado em uma única linha, e queremos colocar uma quebra de linha.

Podemos utilizar o caractere de escape através de contrabarra (\) e o seu código, que no caso de quebra de linha é o n.

Esse \n não é uma especificidade do PHP, é um código de um caractere de escape. Portanto, o \n significa quebra de linha em qualquer linguagem, seja JavaScript, C, Java ou expressões regulares.

Assim como \t é um "Tab", uma tabulação. Portanto, o \t cria aquele espaço grande que a tecla "Tab" faz.

screen-match.php

echo "Bem vindo(a) ao\t\tscreen match!\n";
Copiar código
Vamos executar o Screen Match no terminal e conferir o resultado:
```php
php screen-match.php
```
```php
Bem vindo(a) ao screen match!

7.1
```
O terminal vai exibir as tabulações como espaço, mas em uma planilha, por exemplo, isso poderia fazer a diferença.

Vamos transformar esses \t em espaço novamente para o texto ficar bem formatado:
```php
echo "Bem vindo(a) ao screen match!\n";
```
Concatenação e interpolação
Como poderíamos fazer para escrever "Nome do filme", dois pontos, e exibir o nome? Ou "Nota do filme", dois pontos e exibir a nota?

Sua primeira solução, caso você não saiba muito de PHP, pode ser dar um echo no texto "Nome do filme". Entre as aspas, também colocaríamos dois pontos e espaço. Para fechar essa string, adicionamos ponto e vírgula.

Em seguida, você exibiria a variável $nomeFilme em outra instrução echo. Depois, exibiria uma quebra de linha \n entre aspas. Logo, exibiria mais um echo com o texto "Nota do filme", dois pontos, espaço e assim por diante.
```php
echo "Nome do filme: ";
echo $nomeFilme;
echo "\n";
echo "Nota do filme: ";
echo $notaFilme;
```
Isso vai funcionar. Ao executar o último comando do terminal, usando seta para cima e "Enter", teremos o nome do filme e sua nota:
```php
Nome do filme: Top Gun - Maverick

Nota do filme: 7.1
```
Porém, às vezes, não queremos colocar várias instruções para exibir uma única linha, ou, nesse caso, para exibir algo tão pequeno assim.

Como podemos unir textos, unir strings? Temos duas formas: concatenação e interpolação. Ambas palavras podem parecer complicadas, mas significam juntar. Portanto, são formas diferentes de juntar textos.

Podemos pegar os vários echo que havíamos feito. No final do nosso programa, vamos colocar echo e, entre aspas, o texto "Nome do filme", dois pontos, espaço.

Fora das aspas, vamos utilizar um novo operador, que é um operador ponto (.). Esse operador ponto é o operador de concatenação, de juntar dois textos. Portanto, vamos colocar $nomeFilme e ponto vírgula para encerrar a instrução.
```php
echo "Nome do filme: " . $nomeFilme;
```
Podemos abrir o terminal, limpar a tela com cls e digitar php screen-match.php para executar o programa.

Teremos a concatenação dos dois textos:
```php
Nome do filme: Top Gun - Maverick
```
Além disso, poderíamos concatenar novamente com uma quebra de linha, por exemplo.
```php
echo "Nome do filme: " . $nomeFilme . "\n";
```
Nesse caso, depois da execução, teríamos uma linha vazia no terminal.

Vamos fazer agora de forma diferente para a exibição nossa nota. Em uma nova linha, digitamos echo "Nota do filme: ". E, ao invés de sair da string, juntar com uma variável, que é uma outra string, e depois juntar com outra variável, que é a quebra de linha, vamos colocar tudo junto dentro dessa string. Isso é uma interpolação.

Portanto, entre as aspas, adicionamos $notaFilme\n - já colocando a quebra de linha no final.
```php
echo "Nome do filme: " . $nomeFilme . "\n";
echo "Nota do filme: $notaFilme\n";
```
Nem toda linguagem de programação trabalha com interpolação da mesma forma. No PHP, desde que seja dentro de aspas duplas, conseguimos interpolar variáveis.

Vamos abrir o terminal e executar para conferir se teremos o resultado esperado.
```php
Nome do filme: Top Gun - Maverick

Nota do filme: 7.1
```
Note que dissemos que conseguimos interpolar variáveis com aspas duplas. O que acontece se trocarmos todas as aspas por aspas simples? Vamos fazer isso.
```php
echo 'Nome do filme: ' . $nomeFilme . '\n';
echo 'Nota do filme: $notaFilme\n';
```
Note que agora as cores no nosso editor de código estão um pouco diferentes. Quando tentamos executar, ele não está exibindo o que esperávamos:
```php
Nome do filme: Top Gun - Maverick\nNota do filme: $notaFilme\n
```
O nome do filme, Top Gun Maverick, funcionou, mas a quebra de linha não. E, em nota do filme, não foi exibida a nota do filme, mas, sim, o nome da variável $notaFilme, e de novo, o \n. O que aconteceu?

No PHP, existe uma diferença entre aspas simples (ou apóstrofos) e aspas duplas. A diferença é, com aspas simples, ele não vai interpretar nada do que estiver em uma string. Apenas vai fazer sua exibição. Porém, se utilizarmos aspas duplas, aí o PHP vai tentar interpretar - seja uma variável ou sejam caracteres de escape, como é o caso da quebra de linha.

Atenção: se vamos realizar uma interpolação de textos com variáveis ou caracteres de escape, precisamos usar aspas duplas.

Se não, podemos utilizar as aspas simples. E aí, para adicionar alguma coisa, utilizamos a concatenação. Por exemplo, podemos concatenar um texto entre aspas simples com uma quebra de linha entre aspas duplas:
```php
echo 'Texto' . "\n";
```
Existe alguma vantagem de usar aspas simples ou aspas duplas? Não existe vantagem. São formas diferentes de trabalharmos com texto em PHP.

Quando trabalhamos em equipes, normalmente, entramos num consenso e estabelecemos um padrão. Por exemplo, se vamos sempre utilizar aspas simples, se vamos sempre utilizar aspas duplas ou em quais casos vamos utilizar cada uma.

Nomenclatura
Falando em padrões, um detalhe importante é a nomenclatura.

Nós escolhemos nomear nossas variáveis começando por letra minúscula e colocando a primeira letra de cada palavra subsequentemente em maiúscula, sem espaços. Um exemplo é a variável $nomeFilme. Isso é conhecido como camelCase.

Outras pessoas poderiam usar o underline para separar as palavras, por exemplo, $nome_filme. Essa convenção é o snake_case.

Tudo essas formas são válidas e funcionam. Só que, normalmente, cada linguagem de programação tem seus padrões de nomenclatura. Conforme você for avançando com PHP e criar funções, classes, métodos, você aprenderá que existem padrões bem definidos pela comunidade PHP para fazer isso.

Vamos deixar uma atividade de "Para Saber Mais" com padrões estabelecidos para nomear todo tipo de coisa - muitas delas talvez você ainda não conheça. O objetivo é entender que existe um padrão que deve ser seguido.

Um detalhe importante é que, com variáveis, você pode ter padrões diferentes. Normalmente, entre uma equipe, você escolhe e segue um padrão. Geralmente, escolhemos entre o camelCase ou snake_case.

Próximos passos
Antes de fazer algo com esses dados, vamos levantar um último ponto interessante aqui para finalizar a manipulação de dados.

Até agora trabalhamos sempre com o mesmo filme, ano e notas. Mas, e se quiséssemos receber da entrada do teclado, como parâmetro na execução do nosso comando, todas as notas? Ou pelo menos o ano de lançamento?

Isso significa que queremos trabalhar com a entrada de dados, ou seja, queremos que o usuário nos forneça informações - não digitar tudo no código. Afinal de contas, a ideia de variável é justamente ter valores que variem, isto é, valores que não conhecemos na hora de codificar e que podem vir do mundo exterior.

No próximo vídeo, abordaremos entrada de dados e como podemos receber alguma informação direto da linha de comando.
