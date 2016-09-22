---
layout: post
title: "Como ajustar a data do post no Jekyll"
date: 2016-09-22 04:05:34
image: '/assets/img/'
description: 'Aprenda a deixar a data do seu post em português no Jekyll'
tags:
- liquid
- jekyll
categories:
twitter_text: 'Ajuste a data dos seus posts no Jekyll'
---

Então você criou o seu blog com <a class="externalLink" href="https://jekyllrb.com/" target="_blank">Jekyll</a>, escolheu um tema bacana no 
<a class="externalLink" href="http://jekyllthemes.org/" target="_blank">Jekyll Themes</a>   , hospedou no 
<a class="externalLink" href="https://pages.github.com/" target="_blank">GitHub Pages</a>, e na hora de postar seu
primeiro artigo? PUUUM! Data com nome em inglês.



A maioria das pessoas não liga muito pra isso, ALIÁS, muitos BRASILEIROS escrevem o blog todo em inglês (o que eu acho maneiro).
Mas se você escreve o blog em português e liga pra esse tipo de coisa, chegou no post certo.

O Jekyll é escrito em <a class="externalLink" href="https://www.ruby-lang.org/pt/" target="_blank">Ruby</a>, e usa <a class="externalLink" href="https://shopify.github.io/liquid/" target="_blank">Liquid</a> (também escrito em Ruby) para carregar todo o conteúdo. 

Uma das maneiras para resolver o problema é "gerar" o post, e depois ir no código para editar a data na mão. Que trabalho, hein!

**LIQUID:** é justamente com esse cara que vamos trabalhar hoje. 

Se você chegou nesse post, é porque provavelmente conhece um pouco a estrutura que o Jekyll trabalha. Então mãos a obra...

O primeiro passo é ir no index.md (localizado na raíz do projeto) e achar um Span com nome "date" (ou algo parecido). 

<figure>
	<img src="{{site.baseurl}}/assets/img/2016/09/como-ajustar-a-data-do-post-no-jekyll/01.png" alt="Print Span Date">
</figure>

Vamos apagar tudo que está dentro da tag e adicionar o seguinte código:

{% highlight liquid %}
{% raw %} 
          {{ post.date | date: "%d" }} de 
          {% assign m = post.date | date: "%-m" %}
                    {% case m %}
                    {% when '1' %}Janeiro
                    {% when '2' %}Fevereiro
                    {% when '3' %}Março
                    {% when '4' %}Abril
                    {% when '5' %}Maio
                    {% when '6' %}Junho
                    {% when '7' %}Julho
                    {% when '8' %}Agosto
                    {% when '9' %}Setembro
                    {% when '10' %}Outubro
                    {% when '11' %}Novembro
                    {% when '12' %}Dezembro
                    {% endcase %}
                   de {{ post.date | date: "%Y" }}
{% endraw %} 
{% endhighlight %}


Veja como ficou:

<figure>
	<img src="{{site.baseurl}}/assets/img/2016/09/como-ajustar-a-data-do-post-no-jekyll/02.png" alt="Print Span Date">
</figure>

Problema quase resolvido. O que fizemos? Algo equivalmente a um "Switch". Se o mês for 1, então ele mostra Janeiro, se for 2, Fevereiro...

Agora clique no post, ele ainda estará mostrando a data com o nome de inglês. Vá na pasta **_layouts**, ache o arquivo post.md e faça a mesma alteração.
Se você não encontrar tags com o nome "date" nos **_layouts**, tente achar em **_includes.** 

Dependendo do template que você escolher, talvez você tenha dificuldades pra fazer essa alteração. Estou disponível para ajudar, só realizar o comentário abaixo.

Por hoje, era isso (esse post foi mais rápido que a minha máquina de café). Até o próximo post!
