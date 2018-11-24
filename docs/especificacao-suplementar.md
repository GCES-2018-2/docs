# Especificação Suplementar

## Histórico de Revisão
|    Data    | Versão |                                       Descrição                                       |     Autor     |
|:----------:|:------:|:-------------------------------------------------------------------------------------:|:-------------:|
| 06/04/2017 | 0.1    | Introdução, Funcionalidade, Usabilidade, Confiabilidade, Desempenho e Suportabilidade | Ateldy Brasil |
| 08/04/2017 | 1.0    | Restrições de Design, Padrões Aplicáveis                                              | Ateldy Brasil |
| 19/04/2017 | 1.1    | Refatoração e Requisitos de Licenciamento                                             | Ateldy Brasil |
-----

[1. Introdução](#1-introdução)  
[2. Funcionalidade](#2-funcionalidade)  
[3. Usabilidade](#3-usabilidade)  
[4. Confiabilidade](#4-confiabilidade)   
[5. Desempenho](#5-desempenho)   
[6. Suportabilidade](#6-suportabilidade)  
[7. Restrições de Design](#7-restrições-de-design)  
[8. Requisitos de Licenciamento](#8-requisitos-de-licenciamento)

-----
## 1. Introdução
### 1.1 Finalidade
A Especificação Suplementar tem o objetivo de definir requisitos do sistema. Neste documento estão listados os requisitos que não estão relacionados aos Casos de Uso. A Especificação Suplementar associado com o modelo de casos de uso formam uma visão geral dos requisitos do projeto.

### 1.2 Escopo
Essa especificação define os requisitos não-funcionais associados ao ‘SIGS’, que será desenvolvido por alunos das disciplinas de Métodos de Desenvolvimento de Software e Gestão de Portfólio e Projeto, da Faculdade UnB Gama. A proposta tem o objetivo de simplificar a operação de alocação de salas na UnB, que hoje é feita de forma manual.

### 1.3 Definições, Acrônimos e Abreviações
* SIGS: Sistema Inteligente de Gestão de Salas
* MVC: referente ao padrão de arquitetura Model-view-controller

### 1.4 Referências
* [Documento de Visão](https://github.com/fga-gpp-mds/Grupo---7-GPP-MDS/wiki/Documento-de-Vis%C3%A3o)
* [Documento de Arquitetura](https://github.com/fga-gpp-mds/Grupo---7-GPP-MDS/wiki/Documento-de-Arquitetura)

## 2. Funcionalidade
Os requisitos funcionais podem ser listados através do [Diagrama de Casos de uso](https://github.com/fga-gpp-mds/2017.1-SIGS/wiki/Documento-de-Arquitetura#4-vis%C3%A3o-de-casos-de-uso), localizado no [Documento de Arquitetura](https://github.com/fga-gpp-mds/Grupo---7-GPP-MDS/wiki/Documento-de-Arquitetura), além do [Documento de Visão](https://github.com/fga-gpp-mds/2017.1-SIGS/wiki/Documento-de-Vis%C3%A3o#5-requisitos-funcionais).

## 3. Usabilidade
### 3.1 Facilidade de uso
O usuário não necessitará de um treinamento para que consiga utilizá-lo. O sistema será simples para que não seja exigido um conhecimento prévio, apenas será exigido que ele saiba utilizar um navegador da Web.

## 4. Confiabilidade
### 4.1 Disponibilidade
O sistema deverá estar disponível 24 horas por dia, 7 dias por semana.

### 4.2 Exatidão
As informações disponibilizadas sobre salas, deverão estar de acordo com informações disponibilizadas pela instituição, além dos dados inseridos pelo administrador do sistema.

### 4.1 Segurança
A solicitação de cadastro deve ser aprovada pelo Assistente Administrativo, de forma que somente um usuário aprovado poderá desfrutar das funcionalidades do sistema.

## 5. Desempenho
O Desempenho estará diretamente relacionado com a qualidade da conexão de internet do usuário e com o navegador que será utilizado.

## 6. Suportabilidade
### 6.1 Ferramentas
* Linguagem de programação: Ruby (versão 2.3.1)
* Framework Rails (versão  5.0.2)

### 6.2 Web para usuários
O usuário será capaz de usar o sistema através de navegadores como Google Chrome, Mozilla Firefox e Internet Explorer que são compatíveis com HTML5, CSS3 e JavaScript.

## 7. Restrições de Design
### 7.1 Responsividade
O sistema deve se ajustar de forma responsiva, ou seja, ajustando todo o conteúdo da tela à plataforma que o usuário estiver utilizando.

## 8. Requisitos de Licenciamento
É utilizado a [Licença MIT](http://www.jclark.com/xml/copying.txt) para o licenciamento do Software. É uma licença permissiva que possibilita a reutilização de software licenciado em programas livres ou proprietários.



