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

Obs.: Código para geração do banco de dados



CREATE TABLE EmpresasParceiras 
( 
 ID INT PRIMARY KEY AUTO_INCREMENT,  
 NomeEmpresa INT NOT NULL,  
 SetorAtuacao INT NOT NULL,  
 Endereco INT NOT NULL,  
 Contato INT NOT NULL,  
); 

CREATE TABLE Colaboradores 
( 
 ID INT PRIMARY KEY AUTO_INCREMENT,  
 NomeColaborador INT NOT NULL,  
 Cargo INT NOT NULL,  
 Email INT NOT NULL,  
 Telefone VARCHAR(n) NOT NULL,  
 IDEmpresaParceira INT NOT NULL,  
 IDTarefas INT NOT NULL,  
); 

CREATE TABLE Projetos 
( 
 ID INT PRIMARY KEY AUTO_INCREMENT,  
 NomeProjeto INT NOT NULL,  
 Descricao INT,  
 DataInicio DATE NOT NULL,  
 DataTermino DATE NOT NULL,  
 IDCliente INT,  
); 

CREATE TABLE Servicos 
( 
 ID INT PRIMARY KEY AUTO_INCREMENT,  
 DescricaoServico INT NOT NULL,  
 Valor FLOAT NOT NULL,  
 IDCliente INT NOT NULL,  
); 

CREATE TABLE Clientes 
( 
 ID INT PRIMARY KEY AUTO_INCREMENT,  
 NomeCliente INT NOT NULL,  
 Setor INT NOT NULL,  
 Contato INT NOT NULL,  
); 

CREATE TABLE Equipes 
( 
 ID INT PRIMARY KEY AUTO_INCREMENT,  
 NomeEquipe INT NOT NULL,  
 IDProjeto VARCHAR(n) NOT NULL,  
); 

CREATE TABLE Tarefas 
( 
 ID INT PRIMARY KEY AUTO_INCREMENT,  
 DescricaoTarefa INT NOT NULL,  
 DataInicio DATE NOT NULL,  
 DateTermino DATE NOT NULL,  
 IDProjeto INT,  
 IDEquipe INT NOT NULL,  
); 

ALTER TABLE Colaboradores ADD FOREIGN KEY(IDEmpresaParceira) REFERENCES EmpresasParceiras (IDEmpresaParceira)
ALTER TABLE Colaboradores ADD FOREIGN KEY(IDTarefas) REFERENCES Tarefas (IDTarefas)
ALTER TABLE Servicos ADD FOREIGN KEY(IDCliente) REFERENCES EmpresasParceiras (IDCliente)
ALTER TABLE Equipes ADD FOREIGN KEY(IDProjeto) REFERENCES Projetos (IDProjeto)
ALTER TABLE Tarefas ADD FOREIGN KEY(IDProjeto) REFERENCES EmpresasParceiras (IDProjeto)
ALTER TABLE Tarefas ADD FOREIGN KEY(IDEquipe) REFERENCES EmpresasParceiras (IDEquipe)


## Contribuição

Contribuições são bem-vindas! Se você tiver sugestões de melhorias no modelo de banco de dados ou encontrar algum problema, por favor, abra uma issue neste repositório.

