---
layout: post
title: 'Como renovar o meu Certificado SSL no Easy Engine'
image: /assets/images/example4.jpg
tags:
  - tag
status: publish
---
# Como renovar o meu Certificado SSL no Easy Engine

[Escrevi um artigo sobre o poder do Easy Engine](https://gabrielcano.com.br/o-poder-do-easy-engine/)  e precisei renovar o certificado SSL, porém tive grandes dificuldades no processo.

Lá na documentação do  [Easy Engine](https://easyengine.io/), parece tudo ser uma maravilha. Vejam:

**Desabilitando o SSL**

ee site update example.com --letsencrypt=off

**Atualizando o SSL**

ee site update example.com --letsencrypt=renew

Mas nem tudo são flores, meus amigos. Tentei executar esses comandos diversas vezes e tive insucesso em todas as tentativas de renovação do meu certificado de SSL.

Fuçando em tudo quanto é artigo e pergunta do Stackoverflow e sem entender muito inglês, achei alguns comandos que resolveram o meu problema.

O primeiro passo foi atualizar um tal de  **nightly.**

Fiz essa atualização com o comando abaixo:

ee cli update --nightly

Com isso consegui executar o comando **ee site ssl-renew**, que não conseguia de forma alguma. Assim, consegui renovar meu certificado SSL 🙏.

Além disso, precisei atualizar o Easy Engine e restartar o Proxy do Nginx. Não sei se todos esses itens são necessários para a resolução do problema, porém seguindo esse passo a passo muito provavelmente conseguirão ter algum sucesso 😍