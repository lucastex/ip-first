# Intelipost - Case técnico

## Descrição

Primeira solução para o case técnico apresentado pela Intelipost.

Nesta abordagem, a solução apresentada foi de utilizar um Identity/Authentication Provider externo a aplicação. Diversos players no mercado hoje oferecem esta solução, como AWS Cognito, Google Firebase Auth, Auth0 dentre outros.

Para este exemplo, utilizei o Google Firebase Auth, para aproveitar também um outro recurso da plataforma, o Google Firebase Realtime Database, um storage NoSQL online que permite o armazenamento e sincronismo das informações entre todos os clientes em realtime.

## Acessando a aplicação

A solução é extremamente simples, e está disponível online para utilização no link: [https://intelipost-first.firebaseapp.com](https://intelipost-first.firebaseapp.com). Ao fazer o registro, um novo usuário será criado, porém sem perfil default atribuído (em um cenário real, tarefa para a aplicação backend realizar).

Para se logar com um usuário já com perfil atribuído, utilizar as credenciais:

    perfil: admin
    login: lucastex@gmail.com
    senha: 123456

    perfil: sales
    login: lucas@moskitcrm.com
    senha: 123456

A estrutura de itens do menu lateral virá diretamente do Database Realtime e será montada na tela para o usuário dependendo do perfil logado.

## Novo deploy

Deve-se criar um novo projeto no Firebase na conta desejada e alterar as credenciais do projeto nos arquivos `index.html` e `dashboard.html` . Para o deploy, instalar o CLI do firebase e executar o comando:

`firebase deploy` 
