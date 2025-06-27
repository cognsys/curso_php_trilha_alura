Praticar é muito importante! Por isso, preparamos uma lista de exercícios para você exercitar o conteúdo abordado nesta aula.

1 - Escreva um programa em PHP que exiba seu nome na tela.

2 - Crie um programa em PHP que calcule a média de três notas e exiba o resultado.

3 - Elabore um programa em PHP que receba um valor em metros e converta para centímetros.

4 - Desenvolva um programa em PHP que verifique se um ano é bissexto ou não.

5 - Escreva um programa em PHP que converta uma temperatura de Celsius para Fahrenheit.

Você pode clicar no botão “Opinião do instrutor” para conferir as respostas.

Opinião do instrutor

1 -
```php
<?php

echo "Seu Nome";
```
2 -
```php
<?php

$nota1 = 7;
$nota2 = 8;
$nota3 = 6;
$media = ($nota1 + $nota2 + $nota3) / 3;
echo "A média é: " . $media;
```
3 -
```php
<?php

$metros = 5;
$centimetros = $metros * 100;
echo "$metros metros equivalem a $centimetros centímetros.";
```
4 -
```php
<?php

$ano = 2024;
if (($ano % 4 == 0 && $ano % 100 != 0) || $ano % 400 == 0) {
    echo "$ano é bissexto.";
} else {
    echo "$ano não é bissexto.";
}
```
5 -
```php
<?php

$temperaturaEmCelsius = 30.4; // Modifique esse valor para a temperatura que desejar
$temperaturaEmFahrenheit = $temperaturaEmCelsius * 1.8 + 32;

$mensagem = "A temperatura de $temperaturaEmCelsius Celsius é equivalente a $temperaturaEmFahrenheit Fahrenheit";

echo $mensagem;
```
