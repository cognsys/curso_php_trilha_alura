Quando trabalhamos com um programa real, lidamos o tempo todo com dados externos, sejam dados armazenados em algum lugar ou dados fornecidos pela pessoa usuária que está utilizando nosso programa.

Entrada de dados
Se estamos falando do mundo web, por exemplo, um formulário é uma maneira da pessoa usuária entrar dados em nosso programa. A pessoa digita dados no formulário e, ao enviar esse formulário, os dados chegam em nosso servidor, no nosso código PHP.

Como não estamos falando do mundo web, podemos explorar uma forma de receber dados do terminal. Por exemplo, queremos abrir o terminal, executar o programa com php screen-match.php e também digitar o ano de lançamento desse filme, por exemplo, 2022 e conseguir pegar esse dado em nosso programa.
```php
php screen-match.php 2022
```
No PHP, é muito fácil fazer isso, da mesma forma como é feito em C ou Java. A diferença é que nessas linguagens envolve um conceito mais complexo de funções. Enquanto em PHP, temos uma variável quase mágica, que é criada automaticamente.

Essa variável, que queremos atribuir ao ano de lançamento, é chamada de $argv, a qual contém todos os valores que forem passados no terminal.
```php
screen-match.php:
```
```php
$anoLancamento = $argv;
```
Esse $argv contém diversos valores, porque é possível passar números, textos e uma infinidade de outros valores na linha de comando.

Mas, como o $argv vai saber qual dos valores ele deve armazenar? Ele não sabe, portanto, ele armazena todos - inclusive o nome do programa que está sendo executado, nesse caso, screen match.php.

Começando no índice 0, ele vai armazenar o nome do arquivo que está sendo executado, e depois, todos os parâmetros que passarmos. No caso, 2022 e qualquer outra coisa.

Se ele começa no índice 0, queremos pegar o índice 1 desse $argv. Só que não podemos pegar $argv1 direto, senão estaríamos acessando uma variável chamada $argv1. O que queremos é acessar um índice, um item de número 1 dentro dessa variável $argv.

Para isso, vamos utilizar uma sintaxe que conheceremos melhor mais para frente, mas por enquanto, basta colocar o número do índice entre colchetes.
```php
$anoLancamento = $argv[1];
```
Isso vai pegar o primeiro parâmetro que passarmos depois do nome do nosso programa.

No final do arquivo, podemos exibir o texto "Ano de lançamento", dois pontos seguido da variável $anoLancamento. Vamos quebrar a linha com \n e adicionar um ponto e vírgula no final.
```php
echo "Ano de lançamento: $anoLancamento\n";
```
Agora, estamos exibindo o ano de lançamento, que é uma informação que vem da pessoa usuária, que vem da nossa linha de comando.

Também vamos mostrar outro operador para definir um valor padrão caso a pessoa usuária não informe nada. Após $arg[1], vamos colocar dois pontos de interrogação.

O nome técnico de ?? é operador de coalescência nula. O que isso quer dizer? Se o que está à esquerda desse operador for nulo, o que vem à direita vai ser utilizado. Então, vamos colocar o 2022 como valor padrão.
```php
$anoLancamento = $argv[1] ?? 2022;
```
O valor nulo é um tipo específico em linguagens de programação. Em algumas linguagens, como C ou Java, pode ser um valor muito problemático. No PHP, é um valor que pode até nos ajudar às vezes, ele não traz tantos problemas.

Caso não passemos nenhum valor, ou seja, o índice 1 não exista, o $argv[1] vai ser nulo. Então, esse operador entenderá isso e entregará o valor 2022 para a variável $anoLancamento.

Após salvar, vamos executar o programa, passando o seguinte comando no terminal:
```php
php screen-match.php 2021
```
Com isso, o ano de lançamento exibido precisa ser 2021. E é exatamente o que acontece:
```php
Bem vindo(a) ao screen match!

Nome do filme: Top Gun - Maverick

Nota do filme: 7.1

Ano de lançamento: 2021
```
Se apertamos a seta para cima, para pegar o último comando, e trocamos 2021 por 2020, o que vai ser exibido é "Ano de lançamento: 2020". Agora, se apertamos a seta para cima e apagamos esse parâmetro, seria exibido o ano de 2022, que é o valor padrão.

Próximos passos
Agora, conseguimos receber valores da pessoa usuária. Desse modo, é possível ter um código que pode mudar seu comportamento. Podemos tomar decisões no nosso código.

Por exemplo, se o filme tiver uma nota alta, queremos recomendá-lo. Se tiver uma nota baixa, queremos dizer que não recomendamos. Ou, como estamos trabalhando com o ano, podemos dizer que é um filme recente, se for um filme lançado depois de 2022. Caso contrário, dizemos que é um filme antigo.

Como podemos tomar decisões e controlar o fluxo de execução do nosso código? É isso que vamos aprender na próxima aula.
