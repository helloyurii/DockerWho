    Bem vindos! 

// Esse repositório serve para armazenar minhas pesquisas e aprendizados a fim de memorização e se possível ajudar outras pessoas a estudarem. Fique a vontade para argumentar alguma coisa.

* Primeiro estudo - Docker: Esse negócio ou te ajuda ou te mata

// As palavras Docker, Images, Dockerfile, Docker-compose viraram palavras populares que ninguém sabe exatamente seus significados, tipo "Cacilda". Um dos primeiros cursos que fiz desse assunto me trouxeram uma visão geral e entendimento do Docker em si, mas mesmo assim saber o que é exatamente um Imagem, um container e como eles magicamente vão pra internet, foi o que mais me doeu para aprender e por isso quero dividir aqui.

    Press Start!

*Importância do Docker:

// O Docker possibilita o encapsulamento de todo um ambiente de desenvolvimento, isso diminui drasticamente o tempo de deploy da sua aplicação do ambiente de desenvolvimento para produção. Como o ambiente é sempre o mesmo, você não precisa fazer ajustes, essa é a grande maravilha do Docker.

* O que é uma imagem? 

Na opnião, deveriam ter colocado outra palavra pra isso, pois esse nome confunde muito nossa cabeça. Pra fazer uma analogia, imagem é a preparação de um solo para fazer uma plantação. No linguagem dos códigos eu faria analogia a uma classe. 

Bem, digamos que eu precise de requisitos para plantar Milho e também uma maneira adequada de solo (muitos areada, compactada, reta, inclinada, etc). Um agricultor manda seu funcionário buscar todo esse material e preparar tudo. Esse funcionário no mundo Docker nada mais é do que o Dockerfile.

Vamos entender agora o que é um Dockerfile:

Imagens é a nossa base para construção de uma aplicação, as Images são criadas lendo as instruções que estão contidas no Dockerfile. O site do DockerHun contem vários dockerfiles, ou seja, se criarmos eles teremos diversas imagens. 
Ai entra outro nó que passava pela minha cabeça. Como que nas aplicações da minha empresa tem um Dockerfile se já existem diversas no Dockerhub? 

Vamos chegar na resposta, primeiro é necessário saber que existem imagens oficiais e não oficiais. As imagens oficiais são mantidas pela empresa docker. Geralmente apresentam os nomes: “ubuntu:16.04″, "python:3", e assim por diante. O objetivo das imagens oficiais é prover um ambiente básico (ex. debian, alpine, ruby, python) que serve de ponto de partida para criação de imagens pelos usuários. No DockerHub as pessoas podem enviar suas "receitas de imagens", mas viriam como nome “joarez/ubuntu”. Essa segunda imagem é mantida pelo usuário joarez, que mantém muitas outras imagens não oficiais.

A resposta da minha pergunta é que buscamos uma imagem base através de um comando FROM no meu dockerfile e esse dockerfile criado por mim ao ser construído me dará uma imagem.

O dockerfile não só possui essa imagem base, mas podemos definir mais ainda o ambiente que queremos, podemos por a porta que será exposto, quais comandos serão executados nesse ambiente para efetuar as mudanças necessárias na infraestrutura do sistema, onde nossos arquivos de memório ficarão e etc. Ele realmente busca tudo e prepara o terreno para nossa plantação acontecer!

Depois de ler tudo isso, tende entender essa imagem base de Python que está disponível no DockerHub https://github.com/docker-library/python/blob/8601079d1f70b03c01408377716a3243ce75cec9/3.7/windows/windowsservercore-1709/Dockerfile 

Podemos ver um trenzinho onde um puxa imagem base de uma outra coisa :)

