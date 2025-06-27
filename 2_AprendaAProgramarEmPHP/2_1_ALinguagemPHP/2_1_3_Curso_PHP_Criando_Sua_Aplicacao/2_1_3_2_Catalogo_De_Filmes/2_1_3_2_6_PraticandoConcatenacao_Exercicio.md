Alice resolveu praticar os conceitos de concatenação e interpolação de strings e elaborou o seguinte trecho de código:
```php
$saudacao = "Olá, meu nome é ";
$nome = "Alice ";
$continuacao = "e minha idade é ";
$idade = 17;
echo "$saudacao . $nome . $continuacao" . $idade;
```
O código de Alice possui algum problema?


a) Não, pois as aspas duplas permitem o operador de concatenação dentro da string.
Alternativa incorreta: a diferença entre aspas duplas (") e aspas simples (') é que as variáveis serão interpretadas mas os operadores não. Os operadores dentro de uma string se tornam um caractere como qualquer outro.

b) Sim, pois não é possível concatenar variáveis do tipo int com string.
Alternativa incorreta:é perfeitamente válido concatenar variáveis de tipos diferentes. Podemos concatenar números em um texto sem problemas.

c)Sim, pois o operador de concatenação está dentro da string, ou seja, será exibido.
Alternativa correta: a mensagem que será exibida ao executar esse código é Olá, meu nome é . Alice . e minha idade é 17. A concatenação entre a variável $idade e o restante funcionará, pois essa variável está fora da string.


d) Não há problemas, e a concatenação será feita corretamente como é esperado.
Alternativa incorreta: na verdade, o operador de concatenação foi inserido no código de forma incorreta e o texto não será exibido como Alice deseja.
