Olá, pessoal, boas-vindas de volta! O combinado era falar mais sobre textos e disponibilizar uma atividade sobre os operadores. Contudo, acreditamos que este último é um conteúdo muito importante, por isso decidimos gravar um vídeo para falar sobre alguns operadores que podemos utilizar quando lidamos com variáveis.

Entendendo os operadores matemáticos
Voltando ao Visual Studio Code, vamos tomar como exemplo a nota de um filme. Normalmente, a nota do filme é calculada a partir da média de várias notas que outras pessoas deram.

Vamos supor que demos nota 9 para esse filme, mas outra pessoa deu a nota 6, outra deu a nota 8, outra a nota 7,5, e uma última pessoa deu a nota 5, uma nota bem baixa. Queremos somar o nosso 9 com os valores das outras pessoas. Para isso, vamos utilizar entre cada número o símbolo de adição (+), usado no PHP para realizar somas.

Essa alteração será feita na linha 8, onde temos a variável $notaFilme. Vamos substituir seu valor 8.8 pela soma mencionada.
```
$notaFilme = 9 + 6 + 8 + 7.5 + 5;
```

Em seguida, queremos tirar a média dessas notas. Então, queremos somar cinco notas e dividir essa soma por 5, que é o total de notas que temos. Poderíamos acessar o final dessa linha, após o 5 e dividir esse valor todo por 5, adicionando o símbolo de divisão no PHP que, assim como na maioria das linguagens, é a barra (/), seguida do 5.
```
$notaFilme = 9 + 6 + 8 + 7.5 + 5 / 5;
```
Entendendo as precedências
Todo operador em linguagens de programação possui alguma precedência, assim como na matemática. A diferença da programação e da matemática é que, por exemplo, o símbolo =, que parece ser um igual, é um símbolo de atribuição, ele também tem uma precedência.

Ou seja, não só os operadores matemáticos, mas qualquer operador na programação possui uma precedência. E o operador de divisão tem uma precedência maior do que o operador de soma.

O que isso quer dizer? Se executarmos esse código, primeiro ele vai dividir 5 por 5, isso vai resultar em 1, e depois ele vai realizar todas as somas, exatamente como na matemática.

Para a maioria dos casos, se temos vários operadores com a mesma precedência, eles são resolvidos da esquerda para a direita — exatamente como na matemática.

Na matemática, se quiséssemos realizar a soma primeiro para só depois dividir, a colocaríamos entre parênteses. E na programação, com PHP, é a mesma coisa. Com os parênteses, o PHP vai realizar primeiro toda a soma, e depois dividir por 5.
```
$notaFilme = (9 + 6 + 8 + 7.5 + 5) / 5;
```
No final do código, onde temos echo $nomeFilme, vamos exibir a nota do filme, substituindo o valor desse echo para $notaFilme.
```php
<?php

echo "Bem-vindo(a) ao screen match!"
;

$nomeFilme = "Top Gun - Maverick";
$anoLancamento = 2022;
$notaFilme = (9 + 6 + 8 + 7.5 + 5) / 5;
$incluidoNoPlano = true;

echo $notaFilme;
```
Vamos abrir o terminal, limpá-lo com o comando cls, e exibir de novo com o comando abaixo.
```
php screen-match.php
```
E temos no resultado a nota calculada, agora como 7.1.
```
Bem-vindo(a) ao screen match!

7.1
```
Podemos separar isso em variáveis diferentes. Por exemplo, vamos copiar toda a soma 9 + 6 + 8 + 7.5 + 5, e criar, logo acima da $notaFilme, uma variável $somaDeNotas, que vai receber a soma.

No lugar da soma, em $notaFilme, podemos utilizar outra variável para realizar operações — vamos adicionar $somaDeNotas, que será dividida por 5.
```
$nomeFilme = "Top Gun - Maverick";
$anoLancamento = 2022;
$somaDeNotas = 9 + 6 + 8 + 7.5 + 5;
$notaFilme = $somaDeNotas / 5;
$incluidoNoPlano = true;
```
Devemos perceber que o $somaDeNotas sendo dividido por 5 não precisa de parênteses, porque o seu valor já é a soma. Ou seja, no cálculo da nota do filme, não temos nenhuma soma sendo feita — ela já foi feita anteriormente. E vamos dividir esse único valor por 5.

Se exibirmos o resultado no terminal executando o php screen-match.php, temos os mesmos 7.1.

Conclui-se que conseguimos utilizar variáveis em operações matemáticas e conseguimos ter operações matemáticas no nosso código. Existem os operadores matemáticos de soma, subtração, divisão, e outro que não vimos, o de multiplicação, que é o asterisco (*). Esse símbolo é o operador de multiplicação na grande maioria das linguagens de programação.

Unindo operadores
Às vezes, podemos unir operadores. Vamos adicionar um espaço acima e abaixo da linha $somaDeNotas para trabalhar com um exemplo.
```php
<?php

echo "Bem-vindo(a) ao screen match!"
;

$nomeFilme = "Top Gun - Maverick";
$anoLancamento = 2022;

$somaDeNotas = 9 + 6 + 8 + 7.5 + 5;

$notaFilme = $somaDeNotas / 5;
$incluidoNoPlano = true;

echo $notaFilme;
```
Poderíamos fazer o seguinte, a primeira nota vai ser somente 9.
```
$somaDeNotas = 9;
```
Vamos duplicar essa linha abaixo dela mesma e depois trocar o valor da $somaDeNotas para $somaDeNotas mais a nota 6.
```
$somaDeNotas = 9;
$somaDeNotas = $somaDeNotas + 6;
```
Vamos duplicar essa segunda linha abaixo de si e dizer que $somaDeNotas recebe o valor da $somaDeNotas mais a nota 8.
```
$somaDeNotas = 9;
$somaDeNotas = $somaDeNotas + 6;
$somaDeNotas = $somaDeNotas + 8;
```
Vamos duplicar de novo e colocar a nota 7,5. No final, vamos duplicar de novo e colocar a nota 5.
```
$somaDeNotas = 9;
$somaDeNotas = $somaDeNotas + 6;
$somaDeNotas = $somaDeNotas + 8;
$somaDeNotas = $somaDeNotas + 7.5;
$somaDeNotas = $somaDeNotas + 5;
```
Temos as 5 notas. Estamos atribuindo e acumulando valores na $somaDeNotas. Primeiro, a $somaDeNotas vai ser 9, depois vai ser 9, porque é o que temos, mais 6, ou seja, vai ser 15. Depois, vai ser 15 mais 8, e depois o resultado mais 7,5 e esse resultado mais 5.

Vamos executar no terminal e ver que temos o mesmo valor de resultado, 7.1.

Dissemos anteriormente que, às vezes, podemos unir operadores. Se temos uma variável sendo adicionada cumulativamente ao valor dela mesma, ao invés de precisar escrever o nome da variável mais o outro número, podemos escrever o símbolo += no lugar do igual. Faremos isso no lugar da primeira duplicata do $somaDeNotas.
```
$somaDeNotas = 9;
$somaDeNotas += 6;
$somaDeNotas = $somaDeNotas + 8;
$somaDeNotas = $somaDeNotas + 7.5;
$somaDeNotas = $somaDeNotas + 5;
```
Esse operador acumulará o valor 6 ao valor da própria variável $somaDeNotas, ou seja, adiciona o que colocarmos à direita desse operador ao valor da própria variável. Portanto, o += é um operador de acumulação.

Vamos utilizar esse mesmo operador em todas as duplicatas que temos.
```
$somaDeNotas = 9;
$somaDeNotas += 6;
$somaDeNotas += 8;
$somaDeNotas += 7.5;
$somaDeNotas += 5;
```
Com isso, estamos acumulando na $somaDeNotas e, no final, dividimos tudo. O código completo se encontra abaixo.
```php
<?php

echo "Bem-vindo(a) ao screen match!"
;

$nomeFilme = "Top Gun - Maverick";
$anoLancamento = 2022;

$somaDeNotas = 9;
$somaDeNotas += 6;
$somaDeNotas += 8;
$somaDeNotas += 7.5;
$somaDeNotas += 5;

$notaFilme = $somaDeNotas / 5;
$incluidoNoPlano = true;

echo $notaFilme;
```
Vamos abrir o terminal, limpá-lo e executar o programa para ver os mesmos 7.1.

Assim, vimos operadores matemáticos e entendemos que existem alguns operadores diferentes. É importante saber que existem outras combinações que formam novos operadores junto ao de atribuição. Assim como o de soma, podemos unir o de subtração, de multiplicação, de divisão e assim em diante.

Utilizando operadores lógicos
Já utilizamos operadores matemáticos e agora usaremos operadores lógicos. Em relação à verificação de um filme incluído no plano, podemos adicionar um passo para verificar se a pessoa tem o plano prime incluído ou se esse filme é antigo.

Vamos abrir duas linhas vazias abaixo de $notaFilme = $somaDeNotas / 5 e, na primeira, adicionar a variável $planoPrime para dizer se é um plano prime. Vamos colocá-la com o valor verdadeiro, indicando que é um plano desse tipo.
```
$notaFilme = $somaDeNotas / 5;
$planoPrime = true;

$incluidoNoPlano = true;

echo $notaFilme;
```
Podemos dizer que o filme está incluído no plano se a pessoa tiver o plano prime ou outra condição. Para isso, temos operadores lógicos como o operador de dois pipes (||), que significa "ou".

Na variável $incluidoNoPlano, no lugar do true, vamos adicionar $planoPrime ||.
```
$notaFilme = $somaDeNotas / 5;
$planoPrime = true;

$incluidoNoPlano = $planoPrime ||;

echo $notaFilme;
```
Com isso, estamos dizendo que o filme é incluído no plano se a pessoa tem o plano prime ou se ocorrer outra condição — no caso, se é um filme antigo.

Para verificar se esse filme é antigo, podemos utilizar mais operadores lógicos. Por exemplo, se o seu ano de lançamento for menor do que 2020, isso seria um filme antigo. Portanto, após o sinal ||, podemos colocar $anoLancamento, sinal de menor (<), 2020.
```
$notaFilme = $somaDeNotas / 5;
$planoPrime = true;

$incluidoNoPlano = $planoPrime || $anoLancamento < 2020;

echo $notaFilme;
```
Esse é um operador de comparação. Ele vai resultar em um booliano. Ou seja, a comparação $anoLancamento < 2020 vai retornar falso. No final, é como se $incluidoNoPlano fosse verdadeiro ou falso.

Neste momento, entramos nos detalhes de operadores lógicos: a comparação entre "ou" e um valor verdadeiro ou falso resulta em verdadeiro.

Se usarmos outro operador, como o "e", que é feito através de dois "e"s comerciais (&&), perguntaríamos se está incluído no plano prime e se o ano de lançamento é menor do que 2022, que no caso não é. Com isso, o resultado de $incluidoNoPlano seria falso.
```
$notaFilme = $somaDeNotas / 5;
$planoPrime = true;

$incluidoNoPlano = $planoPrime && $anoLancamento < 2020;

echo $notaFilme;
```
Com esses exemplos, percebemos que temos vários operadores em PHP:

Operadores lógicos;
Operadores condicionais, que são operadores de comparação;
Operadores matemáticos.
Após entender o que são operadores, disponibilizaremos uma atividade "Para saber mais" com mais detalhes sobre eles. Nela, os operadores de comparação e lógicos, principalmente, vão ser vistos com mais detalhes, além de outros operadores, indicando quando cada um deles pode ser mais útil.

O mais importante é entender que a manipulação de dados pode ser feita através de operadores.

Neste vídeo, conhecemos operadores matemáticos, operadores lógicos e operadores de comparação. A seguir, vamos falar de forma bem resumida sobre textos, como podemos exibi-los, juntá-los, quebrar linhas de outra forma, entre outras funcionalidades. Para isso, vamos continuar utilizando o nosso Screen Match com PHP.
