# Modelo de Banco de Dados para Sistema RESILIADATA

Este repositório contém o modelo de banco de dados proposto para o sistema RESILIADATA, desenvolvido como parte de um projeto de banco de dados.

## Descrição do Modelo

O modelo de banco de dados foi projetado para armazenar informações sobre empresas parceiras, seus projetos, colaboradores, clientes, tarefas, equipes e serviços. Ele visa auxiliar na avaliação das tecnologias utilizadas pelas empresas parceiras e no gerenciamento de seus projetos e colaboradores.

### Entidades:

- Empresas Parceiras
- Projetos
- Tarefas
- Equipes
- Clientes
- Serviços
- Colaboradores

### Relacionamentos:

- Empresas Parceiras (1:N) Projetos
- Empresas Parceiras (1:N) Colaboradores
- Projetos (1:N) Tarefas
- Projetos (1:1) Equipes
- Clientes (1:N) Projetos
- Clientes (1:N) Serviços
- Colaboradores (1:N) Tarefas

## Arquivos no Repositório

- `mod111`: imagem que representa o modelo de banco de dados.
- `mod1`: propostas de respostas baseados nas perguntas pedidas na elabiração da atividade.
- `README.md`: este arquivo README.

## Exemplo de Utilização

O modelo de banco de dados pode ser implementado em um sistema de gerenciamento de projetos como o RESILIADATA. Os campos e tipos de dados são detalhados no arquivo README.

Obs.: Código para geração do banco de dados está no arquivo TXT "criacao"





## Contribuição

Contribuições são bem-vindas! Se você tiver sugestões de melhorias no modelo de banco de dados ou encontrar algum problema, por favor, abra uma issue neste repositório.

