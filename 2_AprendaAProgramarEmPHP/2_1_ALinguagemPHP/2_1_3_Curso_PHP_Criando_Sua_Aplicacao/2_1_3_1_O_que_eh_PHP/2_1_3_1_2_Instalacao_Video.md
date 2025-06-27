Olá, pessoal! Boas-vindas de volta! Antes de começarmos a aprender e utilizar o PHP, vamos preparar nosso ambiente e instalar o PHP. Faremos isso tanto no Windows quanto no Linux, e também comentaremos brevemente sobre como fazer no Mac. Assim, independentemente do sistema operacional que você esteja usando, será possível reproduzir o processo.

Instalando PHP no Linux
Começaremos com o Linux. Se você estiver usando uma distribuição como Ubuntu, Debian, ou qualquer outra equivalente que utilize o APT como instalador de pacotes, poderá simplesmente executar o comando apt install php. Claro, se você não estiver logado como root, como não deveria, é só colocar o sudo na frente.

No entanto, as versões mais recentes do Ubuntu possuem o PHP disponível nos pacotes até uma versão um pouco mais antiga. Portanto, vamos dar uma dica para você conseguir instalar a versão mais recente do PHP.

Você vai executar o seguinte comando: sudo add-apt-repository ppa:ondrej/php. Isso vai adicionar um PPA, que é basicamente um outro repositório, um outro local para você buscar pacotes.

Adicionado esse repositório, você vai conseguir instalar diversas outras versões do PHP. Então, basta executar o sudo apt install php 8.3. Isso vai fazer algumas perguntas e tudo mais. E no final, quando você executar o comando php -v, você vai ter uma saída parecida com essa, mostrando que você tem instalada a versão 8.3 do PHP.
```
root@c65d8f517729:/# php -v
PHP 8.3.2-1+ubuntu22.04.1+deb.sury.org+1 (cli) (built: Jan 20 2024 14
:16:40) (NTS)
Copyright (c) The PHP Group
Zend Engine v4.3.2, Copyright (c) Zend Technologies
    with Zend OPcache v8.3.2-1+ubuntu22.04.1+deb.sury.org+1, Copyrigh
t (c), by Zend Technologies
root@c65d8f517729:/#
```

Se, quando você estiver assistindo esse vídeo, a versão mais nova do PHP for outra, como 8.4, 9.0, sem problemas, pode sempre instalar a versão mais recente.

Instalando PHP no Windows
Agora vamos ver como fazer no Windows, que é um pouco mais complicado. Vamos acessar php.net no navegador, e isso vai abrir o site oficial do PHP.

Nele, conseguimos ver que a versão mais recente é 8.3. E mais uma vez, se a versão mais recente for outra, pode baixar a mais recente sem problema.

Agora vamos acessar a página de Download. Aqui temos algumas opções, e no topo estar sempre a mais recente. Então, nessa versão do topo, vamos acessar o link de Windows downloads (Downloads para Windows).

Ele vai abrir uma outra página, já com essa versão mais recente, com algumas opções, e vamos baixar essa primeira opção, que é um arquivo Zip. Aqui temos um arquivo zip mostrando o tamanho desse download, é ele que vamos baixar. Não precisa se atentar a esses detalhes de vs16, x64, "Non Thread Safe", não precisa se atentar a isso. Por padrão, você vai sempre baixar essa primeira opção, com o zip.

Feito o download, acessaremos o arquivo na minha pasta de downloads. Vamos simplesmente extrair o arquivo compactado clicando sobre ele e selecionando a opção Extrair Tudo no menu superior do Explorador de Arquivos. Em seguida, vamos clicar em Extrair, que extraíra os arquivos nessa mesma pasta.

Acessaremos a pasta com os arquivos extraídos e nela temos um arquivo chamado php.exe. Nessa pasta temos nosso PHP. Então poderíamos tentar abrir o terminal, por exemplo, clicando aqui no menu Iniciar, vamos digitar cmd, ele abre o Prompt de Comando.

Poderíamos tentar digitar php -v, igual fizemos lá no Linux, só que isso ainda não vai encontrar o PHP. Por quê? O Windows não sabe que ele precisa encontrar o PHP nessa pasta que acabamos de extrair.

Então o que vamos fazer? No topo, onde temos o nome da pasta, vamos clicar e copiar esse caminho completo da pasta. Agora vamos abrir nosso menu Iniciar e pesquisar por variáveis de ambiente. E uma das opções que aparecerá é Editar as variáveis de ambiente do sistema.

Ao selecioná-la, isso vai abrir uma janela, vamos clicar num botão chamado variáveis de ambiente. Agora temos as opções das variáveis de ambiente para o nosso usuário e do sistema como um todo. Você pode editar o que você preferir, vamos editar a do nosso usuário e não do sistema todo.

Aqui temos uma variável chamada path. Vamos clicar em cima dessa variável e clicar no botão Editar, logo abaixo da lista de variáveis.

Agora temos uma lista de caminhos de pastas onde o Windows procura pelos comandos que digitamos. Então aqui vamos clicar em Novo para adicionar um novo caminho e vamos colar aquele que copiamos. Então vamos dar Enter e clicar em Ok três vezes para fechar todas as janelas abertas.

Agora vamos abrir um novo terminal. Então abrimos o menu Iniciar de novo, procuramos o Prompt de Comando e digitamos cmd. Não pode ser naquele mesmo terminal, senão ele não vai ter essa variável de ambiente atualizada. E agora digitamos php -v e temos lá o PHP instalado na sua versão 8.3. Agora o nosso ambiente no Windows está completo.

Instalando no Mac
Por último, vamos deixar um detalhe para vocês, vamos abrir aqui o outro terminal. No ambiente Mac, você vai precisar da ferramenta chamada homebrew. Quem utiliza Mac já está acostumado com essa ferramenta e via de regra já tem ela instalada.

Com o homebrew instalado, você simplesmente vai digitar brew install php. E isso já vai trazer a versão mais recente disponível do PHP. Então com isso você vai ter o PHP instalado no seu Linux, no seu Mac ou no seu Windows. Assim, estamos prontos para escrever código e executar PHP.

Onde escreveremos o código?
Então um último detalhe para termos nosso ambiente completo é, onde vamos escrever esse código? Poderíamos escrever código no nosso bloco de notas, no nosso notepad, sem problemas.

Mas não é muito usual escrever código em uma ferramenta tão crua. Então vamos utilizar algo que é mais específico para a criação de códigos mesmo. Vamos utilizar o Visual Studio Code.

Com o Visual Studio Code não temos um ambiente completo de desenvolvimento. Vamos até deixar um link Para Saber Mais depois falando sobre isso. Mas ele já é um bom começo. Ele vai te ajudar deixando os códigos coloridos, ele tem um terminal. Então ele ajuda um pouco na hora de escrever nosso código.

Então utilizando o Visual Studio Code, já que temos o PHP instalado, na próxima aula vamos criar um projeto e efetivamente executar nosso primeiro código PHP entendendo o que é esse tal PHP, onde o PHP é utilizado e para que serve. Isso tudo na próxima aula.
