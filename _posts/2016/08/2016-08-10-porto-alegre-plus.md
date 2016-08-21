---
layout: post
title: "PortoAlegre+ | ASP NET MVC 5"
date: 2016-08-10 16:05:03
image: '/assets/img/'
description: 'Desenvolvimento de Website | ASP NET MVC 5 + Entity Framework'
tags:
- projetos
- asp.net  
categories:
- Projetos
twitter_text: 'Conheça o PortoAlegre+'
---

<figure>
	<img src="{{site.baseurl}}/assets/img/2016/08/porto-alegre-plus/1.png" alt="Tela inicial do PortoAlegre+">
</figure>

**PortoAlegre+ (Porto Alegre Plus) é um site de reclamação pública para os moradores de Porto Alegre denunciar os problemas da cidade.** O site contém diversas categorias, entre elas, Buracos, Segurança e Transporte Público. O projeto foi o trabalho final para o curso de Desenvolvimento Web do <a class="externalLink" href="http://www.centrodeinovacao.org.br/StudentToBusiness/Apresentacao" target="_blank">S2B</a>.

Vamos lá...

O site tem três tipos de acesso: administrador, usuários com conta oficiais e usuários comuns. Os usuários comuns são os que contribuem para uma cidade melhor. Eles podem abrir qualquer tipo de reclamação, comentar e ajudar marcando como "Resolvida". 

<figure>
	<img src="{{site.baseurl}}/assets/img/2016/08/porto-alegre-plus/2.png" alt="Tela de login do PortoAlegre+">
</figure>

Para abrir uma reclamação, o usuário deve informar o título, categoria, descrição, data, bairro e endereço. A imagem é opcional.

As reclamações são controladas por usuários com conta oficiais. E quem são eles? São funcionários que fazem parte de secretarias, departamentos e serviços de Porto Alegre, como EPTC, DMAE, SMOV, etc.

Os usuários com contas oficiais devem controlar as reclamações de sua categoria. Por exemplo, a EPTC controla apenas "Trânsito / Transporte Público", DMAE apenas "Água e Esgoto", e assim por diante. Eles podem comentar e encerrar uma reclamação. Observação: após uma reclamação ser encerrada, seu status é alterado e ela não pode mais ser editada, nem comentada.

E por fim chegamos ao administrador, que seria o dono do site.

O administrador pode: 

+ Remover qualquer reclamação do site (em casos de uma reclamação falsa ou SPAM).
+ Criar e remover categorias.
+ Criar novos grupos de usuários.
+ Gerenciar grupos de usuários (adicionar um usuário a um grupo, ver que grupos ele pertence ou remover o usuário de um grupo). 

Essa função foi criada para casos em que o órgão municipal queira se juntar com o site. Por exemplo, a SMAM resolveu apoiar o site, então o administrador pode adicionar um funcionário deles para o grupo de "Contas Oficiais".

+ Gerar relatório por categoria, bairro, data e status. O relatório mostra a porcentagem de reclamação, a média de comentários e a quantidade.

<figure>
	<img src="{{site.baseurl}}/assets/img/2016/08/porto-alegre-plus/3.png" alt="Tela de controle do PortoAlegre+">
</figure>  

É importante lembrar que o projeto não possui nenhum vínculo com os órgãos públicos de Porto Alegre. Certo?

O foco do projeto não era o front-end, e sim o back. Algumas funcionalidades que eu citei acima foram dados como requisito, o resto (como criar novos grupos de usuários e gerenciar) foi um "plus" nosso.

<figure>
	<img src="{{site.baseurl}}/assets/img/2016/08/porto-alegre-plus/4.png" alt="Tela de reclamação do PortoAlegre+">
</figure>  

Requisitos cumpridos e certificado na mão. 

Observação: era para o projeto se chamar "Olho Na Cidade", inclusive, foi apresentado com esse nome, mas depois descubri que o nome já existia e tive que mudar.

Não te esquece, esse e os meus demais projetos estão disponíveis no <a class="externalLink" href="https://github.com/AbreuNaWeb/porto-alegre-plus" target="_blank">GitHub.</a> Baixe, experimente, modifique, melhore e principalmente, dê um feedback. Até mais!