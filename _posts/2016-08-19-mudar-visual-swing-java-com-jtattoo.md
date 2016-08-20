---
layout: post
title: "Como mudar o visual de aplicações Swing (Java) com JTattoo."
date: 2015-08-19 23:40:00
image: '/assets/img/'
description: 'Conheça JTattoo, um pacote Look and Feel para aplicações Swing.'
tags:
- jtattoo
- java 
categories:
twitter_text: 'Mude o visual de aplicações Swing (Java)'
---

Fazer um programa com o visual diferente é uma das maiores dúvidas e dificuldades para quem está começando a desenvolver aplicações desktop no Java (e usa Swing). Nesse tutorial eu vou ensinar você passo a passo a mudar radicalmente a aparência de sua aplicação com o JTattoo. Bora?

IDE utilizada no tutorial: Netbeans 8.1

O primeiro passo é desenvolver uma aplicação. Se você já tem um projeto pronto, poderá seguir para o segundo passo, mas recomendo criar um projeto “teste” porque depois será mais fácil implementar no seu projeto original.

Este foi o projetinho para o tutorial, algo bem simples:

<figure>
	<img src="{{site.baseurl}}/assets/img/mudar-visual-swing-java-com-jtattoo/1.png" alt="Exemplo de sistema feito com Swing">
</figure>

## Entendendo o Look and Feel

O segundo passo é entender o termo “Look and Feel”, que resumidamente falando, é a aparência e o comportamento de sua aplicação. Você poderá ver uma explicação mais completa <a href="https://pt.wikipedia.org/wiki/Look_and_Feel" target="_blank">aqui.</a>

Certo, agora que já sabemos o que é L&F (Look and Feel), vamos verificar quais estão instalados no seu sistema. Vá ao código da primeira tela do seu programa, ou seja, a tela inicial e adicione o código abaixo:

{% highlight java %}
private void verificarLAFs() {
       for (LookAndFeelInfo LAF : UIManager.getInstalledLookAndFeels()) {

            System.out.println(LAF.getName());
        }
}
{% endhighlight %}

Veja, é um método que será chamado logo no início da aplicação:

<figure>
	<img src="{{site.baseurl}}/assets/img/mudar-visual-swing-java-com-jtattoo/2.png" alt="Exemplo de sistema feito com Swing">
</figure>

É importante lembrar que estamos utilizando esse código apenas para ver os L&F instalados no seu sistema, ou seja, mais tarde vamos remover ele.

Rodou a aplicação? Certo! Para mim mostrou 5 L&F instalados, são eles: Metal, Nimbus, CDE/Motif, Windows, Windows Classic.

O L&F padrão é o “Nimbus” (que foi adicionado no JAVA SE 6). Agora vamos alterar a aparência. Para isso, vá ao método Main(), no IF do try-catch troque o “Nimbus” por um dos L&F’s instalados no seu sistema.  Eu coloquei o “CDE/Motif”.

<figure>
	<img src="{{site.baseurl}}/assets/img/mudar-visual-swing-java-com-jtattoo/3.png" alt="Exemplo de sistema feito com Swing">
</figure>


E a minha aplicação ficou assim:

<figure>
	<img src="{{site.baseurl}}/assets/img/mudar-visual-swing-java-com-jtattoo/4.png" alt="Exemplo de sistema feito com Swing">
</figure>


Você percebeu a diferença? Conseguiu entender melhor o termo L&F (Look and Feel)?

Agora o método verificarLAFs() pode ser removido. Vamos para o objetivo do tutorial...

## JTattoo

Vou definir o JTattoo em uma frase: uma coleções de pacotes Look and Feel.

Vamos baixar o .jar do JTattoo <a href="http://www.jtattoo.net/Download.html" target="_blank">(clique aqui)</a>  e adicionar ao projeto: Libraries (Bibliotecas) > Add JAR/Folder (Adicionar JAR/Pasta) > vá ao local onde foi realizado o download > selecione o .jar > Open (abrir). Feito, biblioteca adicionada ao projeto.

Se você expandir a biblioteca do JTattoo, verá vários pacotes. A organização dele é assim:

com.jtattoo.plaf.nomeLookAndFeel

Na versão que eu baixei, há 13 L&Fs:

<figure>
	<img src="{{site.baseurl}}/assets/img/mudar-visual-swing-java-com-jtattoo/5.png" alt="Exemplo de sistema feito com Swing">
</figure>


Ainda no método Main(), apague todo o FOR do try-catch e adicione o seguinte código:

{% highlight java %}
UIManager.setLookAndFeel("com.jtattoo.plaf.hifi.HiFiLookAndFeel");
{% endhighlight %}

O código acima faz mais ou menos isso: “Java, vai lá na biblioteca do JTattoo, pega o tema “Hifi” para mim e altera”.

Execute a aplicação. Esse foi o resultado para mim:

<figure>
	<img src="{{site.baseurl}}/assets/img/mudar-visual-swing-java-com-jtattoo/6.png" alt="Exemplo de sistema feito com Swing">
</figure>

PRONTO! Agora você pode testar todos os L&F do JTattoo e escolher o melhor. Para isso, basta alterar “hifi” pelo o nome do L&F que você quer:

O que pouca gente sabe é que todos os temas do JTattoo podem ser personalizados, cores, tamanhos, fontes, etc.

Se você utilizou um JMenuBar em seu projeto, verá que ficou com o nome “JTattoo” na lateral, relaxa! Isso pode ser removido. Para o tutorial não ficar muito grande, vou fazer outro falando sobre a personalização dos temas do JTattoo e como resolver esse problema.

Gostou do tutorial? Teve alguma dificuldade? Conhece outros pacotes de L&F’s? Tchê, perde a timidez e comenta.

O projeto deste tutorial está disponível no meu GitHub.