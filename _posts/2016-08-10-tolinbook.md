---
layout: post
title: "Tolinbook | Java SE"
date: 2015-08-10 16:05:03
image: '/assets/img/'
description: 'Desenvolvimento de Software'
tags:
- projetos  
categories:
- Projetos
twitter_text: 'Conheça o Tolinbook!'
---

Tolinbook é um sistema para gerenciamento de biblioteca. Esse eu desenvolvi por conta própria, afinal, não podemos ficar parados. Bem, o sistema tem dois tipos de acesso: o administrador (bibliotecário) e os usuários comuns.

O Tolinbook seria instalado no computadores da própria instituição. Imagine a seguinte situação: você precisa de um livro, logo, precisa saber se a biblioteca tem ele e se há quantidade disponível. Você chega na biblioteca e faz o quê? E é aí que entra o Tolinbook entra nessa história.

"Ah, Robson. Hoje em dia os sistemas são tudo web" **CERTO! Mas e se por algum motivo você estiver sem acesso a internet, sem o seu computador ou celular? Devemos pensar em todas as probabilidades.**

"Se eu for em um computador da biblioteca, vou ter acesso a internet, logo, vou conseguir acessar um sistema web, tornando o Tolinbook inútil". **Os computadores da biblioteca teriam acesso apenas ao sistema, ou seja, tudo que o usuário/aluno pode fazer no computador é usar o Tolinbook.**

<blockquote>E óbvio, poderia ter versões Web e Mobile.</blockquote>

Entendido? Bora explicar o sistema...

Bem, a tela de login é única para os dois tipos de usuários. Nela, há um botão de registro.

O seu ID é o seu CPF. Por quê CPF e não matrícula? O Tolinbook pode ser usado por vários tipos de bibliotecas, e "matrícula" nem sempre iria se encaixar no contexto, um exemplo disso são as bibliotecas municipais, que são destinadas a todos cidadões e não apenas "alunos". E cá entre nós, CPF É FÁCIL DE LEMBRAR.

Vou começar explicando a tela principal do bibiliotecário(a).

+ Deslogar: volta para a tela de login (UAU!).
+ Livros: CRUD (Create, Read, Update, Delete) em livros, ou seja, o bibliotecário pode ver todos os livros cadastrados, adicionar mais, atualizar e excluir.
+ Autores: Adicionar e excluir (não faz sentido "atualizar" um autor).
+ Entrega: Confirmar a devolução de um livro.
+ Empréstimo: Confirmar empréstimo de um livro.
+ Usuários: Bloquear e desbloquear usuários.
+ Créditos: adicionar créditos para o usuário (explico mais pra frente).

Tela principal do usuário:
 
+ Deslogar.
+ Livros: ver todos os livros cadastrados e reservar.
+ Relatórios: todas as operações já realizadas no Tolinbook (cancelamento, reservas, empréstimos, multas, etc).
+ Meu Perfil: editar dados pessoais e ver algumas informações da conta, como créditos e multas.
 
Algumas regras: a única forma do usuário pegar um livro emprestado
é reservando. 

Condição para a reserva: ele só consegue reservar um livro se não conter multas pendentes, tiver menos que 3 livros reservados E 3 livros emprestados.

Após reservar um livro, ele tem 24 horas para confirmar o empréstimo. Se ele perder o prazo de confirmação do empréstimo, será cobrado R$3 por dia de atraso. Ele também poderá cancelar a reserva, mas se tiver em atraso, a multa será cobrada de qualquer forma.

A regra para a entrega do livro funciona da mesma forma. Após confirmar o empréstimo ele tem 6 dias para a entrega do livro. Perdendo esse prazo, será cobrado R$4 por dia de atraso (culpe o capitalismo).

Lembra que antes eu disse da tela de créditos? Então... O usuário vai precisar adicionar créditos a sua conta para pagar as multas e conseguir reservar livros novamente. O usuário paga o bibliotecário e o bibliotecário adiciona créditos a sua conta.

Bem, acho que não me esqueci de nada. 

<blockquote>Por mais que a aplicação seja em Swing, o visual do Tolinbook é bem "diferentão", isso foi graças ao JTattoo, um pacote Look And Feel.</blockquote>

*Em todo o post, eu citei o Tolinbook com um sentido de comercializar, MAS NÃO, é apenas mais um projeto de estudos, com o objetivo de cada vez aprender (e aprimorar) mais a programação. E mesmo sendo um projeto de estudos, sempre devemos desenvolver uma aplicação pensando no mundo real, no seu ciclo de vida.*

Assim como os meus outros projetos, esse também está [disponível no GitHub][tolinbook]. Baixe, experimente e dê um retorno (é importante).

Conforme eu ir aprendendo mais coisas, vou ir atualizando o sistema. E talvez até saia uma versão Web e Mobile.

<!-- Segue algumas fotos do sistema. -->

Uffa! Chegamos ao fim do post. Agradeço sua atenção. Para ver meus outros projetos, clique aqui.

Dúvidas e Feedback, só comentar. Resposta em 48hrs, ou um café pago (com direito a bala de café). Até!

[tolinbook]: https://github.com/AbreuNaWeb/tolinbook