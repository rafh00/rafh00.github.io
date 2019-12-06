---
layout: post
title:  "Python para Engenheiros e outros malucos #01"
date:   2019-12-06 15:47:42 -0400
categories: posts
tags: [Python, malucos, série]
author: Rafael A. Fuhrmann
comments: true
---

## INTRODUÇÃO

Programar é, para uns, uma arte enquanto para outros um suplício, principalmente dentro da engenharia, cujo tradicionalismo por vezes torna obscura as facilidades que saber um pouco de código pode trazer ao dia a dia. Seja você estudante, ou alguém que já atua, creio que conhecer código será útil na sua vida!
Por isso, vamos falar sobre Python. Esta é uma linguagem de alto nível (em todos os sentidos, diga-se de passagem) que é gratuita, open-source, com milhões de possibilidades, facilidades e aplicabilidades. Particularmente, gosto dela por não ser burocrática, o que se alinha a minha mentalidade de “para resolver um problema, não crie outro”!
Assim, no post inaugural de hoje eu trarei a vocês um pouco do Python e sua sintaxe. Àqueles mais versados em programação fica o aviso: orientação a objetos não será abordada, por hora. A versão que utilizarei será a do Python 3 por motivos de: prefiro essa.

## INSTALAÇÃO

Para quem usa Windows: acessem https://www.python.org/downloads/ e baixem a versão mais recente do Python 3. A instalação é super simples, apenas dar next ad infinitum.
Para usuários de Linux: provavelmente o python já veio instalado, porém é importante verificar se a versão será a 3. Como ter certeza? Abra o terminal e digite:

		```
		>> python
		```
Se estiver instalado, o console abrirá e a versão aparecerá logo nas primeiras linhas. Se for necessário o download, recomendo que busquem no site do python, pois lá se encontram instruções específicas para sistemas que utilizam apt, yum e etc.

## HELLO WORLD
    
Agora começaremos com o maior e mais amado clichê da história da programação: o famoso “Hello World”. Por que? Porque podemos! E, também, para deixar bem clara a falta de burocracia que tanto embeleza o python. Pois bem, para isso utilizaremos o IDLE, a IDE que acompanha já de longa data as instalações do python.
Para abri-lo, eu recomendo acessarem a barra de buscas do seu sistema operacional e procurarem por “IDLE”, sem as aspas.

![Abrindo o IDLE](/assets/serie-python-01/abrindo_idle.png)
	
![Novo arquivo](/assets/serie-python-01/idle_aberto.png)

Uma vez aberto, somos agraciados com uma interface simples contendo apenas o menu superior e o console do python já rodando a pleno vapor. É nele mesmo em que marcaremos a história da programação. Preparem-se! Dedos a postos, digitem:
		```python
		>> print(“Hello world! \n”)
		```
Pasmem e contemplem o resultado, na linha seguinte à do comando temos o nosso belíssimo Hello World, exatamente onde ele deveria estar! Certamente que isso fora deveras trivial, porém notem que apenas uma linha de código, bastante legível e próxima à língua natural (dos anglófonos) fora suficiente para cumprir o papel proposto.

## CONHECENDO A LINGUAGEM: UM PROGRAMA EDUCADO

Para fechar esta pincelada de python, vamos prosseguir a um exemplo um pouquinho mais completo envolvendo entradas e saídas com o usuário. Façamos um código que seja capaz de ler uma mensagem digitada por você no teclado, como o seu nome, e retorne no console alguma mensagem contendo aquilo que você inseriu.
Desta vez sairemos do console e partiremos para a escrita de texto de verdade. Para isso, criem um novo arquivo em “File/ New file” ou pelo famoso “Ctrl+N”.

![salvando](/assets/serie-python-01/idle_menu_new.png)
	
![salvando](/assets/serie-python-01/idle_new_file_open.png)

Arquivo novo, vida nova. Começaremos dando um ar de projeto ao nosso código, usando uma ferramenta que toda linguagem de programação que se preze contém: os comentários. Façamos um cabeçalho que nos orgulhe a cada vez que o arquivo for aberto:

	```python
	# Comentários são feitos com o famoso “jogo da velha”
	# Programa muito educado
	# Feito por ninguém menos que:
	# Em Dia/Mês/Ano
	```
Como preencher estas informações acima não é nenhum mistério, né? Pois então, agora começaremos a programar.
	
{% highlight python %}	
	
	print(“\n $$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$”)
	print(“\n $$$$$$ Oi, meu chapa!                                              $$$$$”)
	print(“\n $$$$$$ Como eh que a vossa grandeza se chama?   $$$$$”)
	print(“\n $$$$$$ Diz ae:                                                             $$$$$”)
	print(“\n $$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$\n”)
	nome = input()
	print(“\n “+nome+” Ce eh o bichao mesmo hein”)
{% endhighlight %}
	
Copiem, salvem na extensão ‘.py’ e executem através de “Run/Run module” ou pelo famoso ‘F5’. 
	
![salvando](/assets/serie-python-01/idle_salvando_arquivo.png)
	
![execução](/assets/serie-python-01/idle_run.png)
	
![execução](/assets/serie-python-01/idle_run.png)

O que fizemos aqui? Bem, primeiramente imprimimos na tela uma espécie de interface, usando o caractere ‘$’ para criar uma sensação de preenchimento na tela e nos lembrarmos que o dólar está alto. A mágica do negócio ficou por conta da linha
	
	```python
	>> nome=input()
	```

O que fizemos nela? Primeiro, criamos uma variável chamada de nome. O que são variáveis? Grosso modo: posições de memória que podem assumir o valor que dissermos para elas assumirem e sobre as quais podemos realizar operações. Na prática, utilizaremos elas para armazenar qualquer tipo de informação que nos for pertinente.
a função ‘input()’ é responsável por ler o que for digitado no terminal, se sua leitura é finalizada quando a tecla ‘enter’ for detectada. Sua entrada, aqui, é de texto. Por fim, o operador ‘=’ é chamado aqui de operador de atribuição, no sentido de que atribui o valor da DIREITA à variável que está a ESQUERDA.
Com o nosso dado em mãos, deveremos apresentá-lo na tela, pois é isso que o nosso programa se propõe a fazer. Por isso utilizamos da nossa linda e cheirosa função ‘print()’, aqui porém com uma diferença.
Notaram o sinal de adição ‘+’ entre as informações contidas em aspas duplas e o nome da variável? Aqui, o ‘+’ faz a operação de concatenação, que consiste em juntar, ou concatenar, duas strings de texto. Sendo ‘nome’ uma string também, ela foi concatenada, e a nossa saudação ficou pronta para fazê-lo, leitor, se sentir um “bichão mesmo”.
Uma ressalva àqueles que acharem que o autor é analfabeto: tradicionalmente se programa no console sem se utilizar de acentos, por conta da codificação ASCII e da burocracia envolvida em se descobrir qual é o bendito código do ‘ç’ ou em se usar a codificação UTF. Mais a frente, porém, mostrarei como utilizá-las.
    
E é isso. Mais python em breve!
