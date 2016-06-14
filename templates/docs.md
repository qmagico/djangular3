# Desafio de Backend
A idéia deste desafio é nos permitir avaliar melhor as habilidades de candidatos à vagas de programador, de vários níveis.

Este desafio deve ser feito por você em sua casa. Dentro do prazo oferecido a você via email.

## Instruções de entrega do desafio
1. Faça um clone deste repositório em seu local para servir de base para o seu projeto. (Evite forkar o projeto para não tornar suas alterações públicas para os outros candidatos).
  * Essa base em Django+AngularJS é opcional, caso você não esteja familiarizado com a linguagem, você tem liberdade de começar um projeto do zero utilizando qualquer outro stack. 
1. Em seguida, implemente o projeto tal qual descrito abaixo.
1. Por fim, envie via email um arquivo patch para rh@qmagico.com.br com o assunto: 'Desafio QMágico Backend - Seu Nome'

## Descrição do projeto

Você deve criar aplicação web que apresente uma thread de fórum.

Existem dois perfis de usuários que podem interagir com esse fórum: Estudante e Administrador.

Um Estudante pode editar e apagar suas próprias mensagens e um Administrador, além disso, pode apagar mensagens de Estudantes.

Uma página de cadastro é necessária para criar os usuários que vão interagir com o fórum. 
Por simplicidade, já no cadastro o usuário escolhe o seu perfil (Estudante ou Administrador)

Somente usuários logados tem acesso ao fórum.

Resumindo, sua aplicação web deve:

1. Possuir uma tela de cadastro (possibilidade de 2 perfis)
1. Possuir uma tela com uma thread de Fórum (acessível somente para usuários logados)
1. Apresentar perfis de Estudante e Administrador, com permissões diferentes.
1. Ser simples de configurar e rodar, funcionando em ambiente compatível com Unix (Linux ou Mac OS X). Ela deve utilizar apenas linguagens e bibliotecas livres ou gratuitas.

Sua aplicação web não precisa:

1. Ter uma aparência bonita.
1. Possibilitar respostas aninhadas.
1. Ser feita a partir de um clone deste projeto, até mesmo não utilizando Django+AngularJS.

## Avaliação
Seu projeto será avaliado de acordo com os seguintes critérios. 

1. Sua aplicação preenche os requerimentos básicos?
1. Documentação das dependências do projeto, se adicionadas.
1. Qualidade do código e familiarização com a linguagem utilizada e boas práticas.
1. Cumprimento do prazo.