Nesta aula nós utilizamos alguns valores numéricos, dentre eles, o tipo float ou double, que nos permite representar valores decimais. Há um problema com esse tipo de dado: a precisão. Ao realizar operações matemáticas com números do tipo float ou double, podemos ter resultados inesperados.

Assim como no sistema decimal (o que usamos no dia a dia), dividir 1 por 3 nos dá um resultado impreciso (0,33333…), no sistema binário (o que as máquinas utilizam) há imprecisões. Para resolver esses problemas no sistema decimal, nós utilizamos frações, então 1 dividido por 3 é exatamente ⅓ (um terço). Já na computação nós utilizamos valores de precisão arbitrária.

Cada linguagem vai fornecer esse tipo de valor decimal com precisão arbitrária de uma forma diferente. No PHP, há duas formas e ambas são através de extensões (https://dias.dev/2022-02-13-extensoes-php/), mas você não precisa se preocupar com esses detalhes agora. O ponto é: se for realizar operações matemáticas em números decimais (como aplicar descontos ou somar valores monetários), não faça isso com float ou double em sistemas reais de produção. Em ambientes de aprendizado não há problema nenhum, mas esse aviso é para seu futuro!

Se quiser ver e entender um pouco melhor sobre esse problema, pode conferir um vídeo sobre números decimais: https://youtu.be/qeZloBkUf6M
