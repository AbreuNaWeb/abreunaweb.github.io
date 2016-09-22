---
layout: post
title: "Trabalhando com vetores (arrays) em C - Parte 1"
date: 2016-09-21 23:59:16
image: '/assets/img/'
description: 'Aprenda a manipular vetores na linguagem de programação C.'
tags:
- C
categories:
twitter_text: 'Vetores (arrays) em C'
---

Após alguns dias fora, estou de volta — uma prova viva que nem sempre ressurreições acontecem em sete dias —

E já começo o post com um probleminha para resolvermos. Imagine a seguinte situação: precisamos desenvolver um sistema que leia o preço de quatro produtos de uma loja e depois mostre a sua média final. Bem, uma das maneiras seria fazer assim:

{% highlight c %}
#include <stdio.h>

int main()
{
    float precoPrimeiroProduto = 0;
    float precoSegundoProduto = 0;
    float precoTerceiroProduto = 0;
    float precoQuartoProduto = 0;
    double mediaPrecoProdutos = 0;

    printf("Informe o preço do primeiro produto: ");
    scanf("%f", &precoPrimeiroProduto);
    printf("Informe o preço do segundo produto: ");
    scanf("%f", &precoSegundoProduto);
    printf("Informe o preço do terceiro produto: ");
    scanf("%f", &precoTerceiroProduto);
    printf("Informe o preço do quatro produto: ");
    scanf("%f", &precoQuartoProduto);

    mediaPrecoProdutos = (precoPrimeiroProduto + precoSegundoProduto + precoTerceiroProduto + precoQuartoProduto) / 4;
    printf("A média do preço dos produtos informados é %f\n", mediaPrecoProdutos);

    return 0;
}
{% endhighlight %}

Tranquilo, né? 

<figure>
	<img src="{{site.baseurl}}/assets/img/2016/09/trabalhando-com-vetores-arrays-em-c-parte1/01.jpg" alt="Foto do Faustão bravo">
</figure>

É, mais ou menos... Imagine ler 400 produtos, e pior, com nome, preço e quantidade. Teríamos que criar 1200 variáveis? SIM! Mas há uma maneira mais fácil de fazer isso, os chamados “vetores”, também conhecidos por Arrays.
Graças a esse “carinha” podemos guardar diversos dados com um mesmo nome de variável. Confuso? Vamos lá...
{% highlight c %}
float preco[4];
{% endhighlight %}
O que eu disse é mais ou menos assim “C, meu amado, eu quero guardar **4** dados do TIPO **FLOAT** e quero identificar esses dados pelo nome de **preco**”. 
Logo, deu pra entender que sua estrutura é:

{% highlight c %}
<tipoDoVetor> nome [quantidade];
{% endhighlight %}

A primeira posição do vetor é o índice 0 (zero), ISSO MESMO. Pode até parecer estranho no começo, mas juro, depois se costuma:

+ preco[0] – PRIMEIRA posição
+ preco[1] – SEGUNDA posição
+ preco[2] – TERCEIRA posição
+ preco[3] – ÚLTIMA posição

**Regrinha: Número de elementos – 1 = total de índices.**

Se você tiver um vetor com 200 nomes de pessoas, e eu dizer pra guardar o nome “Ana” na 121° posição, você guarda o nome em qual índice? 120!
{% highlight c %} 
nome[120] = "Ana";
{% endhighlight %}

Sabendo isso, já podemos começar a utilizar vetores no nosso código. Ficaria mais ou menos assim:

{% highlight c %} 
#include <stdio.h>

int main()
{
    float preco[4];
    double mediaPrecoProdutos = 0;

    printf("Informe o preço do primeiro produto: ");
    scanf("%f", &preco[0]);
    printf("Informe o preço do segundo produto: ");
    scanf("%f", &preco[1]);
    printf("Informe o preço do terceiro produto: ");
    scanf("%f", &preco[2]);
    printf("Informe o preço do quatro produto: ");
    scanf("%f", &preco[3]);

    mediaPrecoProdutos = (preco[0] + preco[1] + preco[2] + preco[3]) / 4;
    printf("A média do preço dos produtos informados é %f\n", mediaPrecoProdutos);

    return 0;
}
{% endhighlight %}

Poxa, mesmo com vetor o nosso código continua enorme, né não? 

Mas fique tranquilo, vamos continuar reduzindo ele. Nos próximos posts , vou abordar laços de repetição, começando pelo FOR, usarei esse mesmo exemplo. E ah, algumas coisas a mais sobre vetores também. 

Enquanto isso, deixo um pequeno tema para você. Coloque a seguinte string: **“APRENDI VETORES”** na terceira posição do vetor que usamos nesse tutorial. SIM, o vetor:
{% highlight c %}
float preco[4];
{% endhighlight %}

Boas noites de sono e até o próximo tutorial.
