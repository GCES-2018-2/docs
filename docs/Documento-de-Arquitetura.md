# Documento de arquitetura

## Histórico de Revisão

| Data       | Responsável          |Versão   | Mudança realizada                                  |  
|------------|----------------------|---|--------------------------------------------------- |
|**29/03/17**|  Bruno Matias Casas     | 0.1  |   Visão de Casos de Uso - Atores                        |  
|**29/03/17**|  Wallacy Braz | 0.2 | Visão Lógica|
|**29/03/17**|  Bruno Matias Casas | 0.3 | Diagrama de caso de uso |
|**29/03/17**| Wallacy Braz | 0.3 | MVC no Ruby on Rails |
|**29/03/17**| Wallacy Braz | 0.4 | Representação da Arquitetura|
|**29/03/17**|  Bruno Matias Casas | 0.5 | Descrição dos Casos de Uso |
|**29/03/17**| Wallacy Braz |0.6| Introdução|
|**02/04/17**| Bruno Matias Casas |0.7| Refatoração - Descrição dos Casos de Uso |
|**04/04/17**| Bruno Matias Casas |1.0| Refatoração - Descrição dos Casos de Uso |
|**08/04/17**| Bruno Matias Casas |1.1| Refatoração - Diagrama e Descrição dos Casos de Uso |
|**15/04/17**| Bruno Matias Casas |1.2| Refatoração - Introdução, Atores, Diagrama e Descrição dos Casos de Uso |
|**28/04/17**| Rodrigo Dadamos e Vinícius Carvalho |1.3| Atualização - Diagrama de Caso de Uso |
-----

[1. Introdução](#1-introdução)<br>
[2. Representação da Arquitetura](#2-representação-da-arquitetura)<br>
[3. Metas e Restrições de Arquitetura](#3-metas-e-restrições-de-arquitetura)<br>
[4. Visão de Casos de Uso](#4-visão-de-casos-de-uso)<br>
[5. Visão Lógica](#5-visão-lógica)<br>

-----
## 1. Introdução

## 1.1   Finalidade

Este documento apresenta uma visão geral da arquitetura do sistema e utiliza uma série de visões arquiteturais diferentes para ilustrar os diversos aspectos do sistema. Sua intenção é capturar e transmitir as decisões significativas do ponto de vista da arquitetura que foram tomadas em relação ao sistema.

## 1.2   Escopo

O presente documento limita-se a fornecer uma visão estrutural segundo a arquitetura que será utilizada pelo sistema. Nele, poderão ser visualizados os seguintes tipos de visões estruturais: A visão de caso de Uso, de Lógica, de Processo, de Implantação e, finalmente, de Implementação.  Além disso, buscará descrever as camadas segundo sua contextualização dentro da estrutura arquitetural.

### 1.3 Definições, Acrônimos e Abreviações

<ul>
	<li>MVC(Model View Controller): Arquitetura de software utilizada em sistemas que desejam separar a modelagem de dados, interface e processamento de requisições em camadas independentes.</li>
	<li>Active View: Biblioteca do framework ruby, responsável por implementar o tratamento de requisições da view.</li>
	<li>Active Controller: Biblioteca do framework ruby que implementa toda a camada Controller.</li>
	<li>Active Record: Biblioteca do framework ruby on rails que implementa operações da camada Model.</li>
</ul>

## 2. Representação da Arquitetura

O referido sistema fará uso do modelo arquitetural MVC. Nele a arquitetura é dividida entre três camadas. A primeira camada, Model, fica responsável pela modelagem de dados e por todas as interações relacionados aos dados. Já a segunda camada, a View, tem por objetivo tornar possível a interface do usuário com o sistema. Por último, a Controller é responsável por tratar as requisições do usuário e passar para as outras camadas, como é possível visualizar no seguinte diagrama:


![MVC Ruby on Rails](https://raw.githubusercontent.com/wiki/fga-gpp-mds/2017.1-SIGS/images/mvc_ruby_on_rails_flowchart.jpg)

## 3.Metas e Restrições da Arquitetura

### Suportabilidade

* O software será suportado pelos principais navegadores web, tais como Mozilla Firefox, Google Chrome,Opera e Microsoft Edge, nas suas versões devidamente atualizadas.  (verificar necessidade de tantos navegadores)

### Usabilidade

* A usabilidade simples e intuitiva do software será garantida por meio de testes feitos utilizando  protótipos de alta e baixa fidelidade.

### Ferramentas de Desenvolvimento

* A linguagem utilizada na aplicação é o Ruby (versão 2.3.1) com a utilização do framework Rails (versão  5.0.2). 

### Confiabilidade

* A confiabilidade é assegurada pela cobertura de teste, mínima, de 90%.


## 4. Visão de Casos de Uso

### 4.1 Atores

### 4.1.1 Coordenador

O Coordenador pode manter sessão de usuário, gerenciar usuário, pode também manter alocação,solicitar alocação em espaço comum,visualizar alocações e gerar relatórios em relação às alocações no sistema.

### 4.1.2 Assistente administrativo

O assistente administrativo pode manter sessão de usuário, aprovar cadastro, Manter alocação, gerenciar solicitações de espaço comum, gerenciar usuário, administrar salas, visualizar alocações e gerar relatórios em relação às alocações no sistema.

### 4.1.3 Usuário comum

O usuário comum pode solicitar um cadastro no sistema.

### 4.1.4 Auxiliar do departamento

O Auxiliar do departamento pode fazer tudo que um coordenador faz no sistema.Com exceção nos casos de solicitar e manter alocação em que o coordenador só fará referente às disciplinas de seu curso, já o auxiliar do departamento faz referente a todas as disciplinas do departamento.

### 4.2   Diagrama de caso de uso

![UFSCar_SAS](https://raw.githubusercontent.com/wiki/fga-gpp-mds/2017.1-SIGS/images/UseCase_Diagrams/UseCase_Diagram19.0.png)

### 4.3  Descrição dos Casos de Uso

<b>UC01 - Gerenciar usuário</b>

Esse caso de uso permite que todos os usuários com cadastro aprovado possam editar, remover e visualizar seus dados, com exceção do assistente administrativo que pode remover e visualizar os dados de todos os usuários.

<b>UC02 - Manter sessão de usuário:</b>

Esse caso de uso permite que todos os usuários com cadastro aprovado possam logar e deslogar do sistema.

<b>UC03 -Solicitar cadastro de usuário:</b>

Esse caso de uso permite ao usuário comum preencher dados de seu cadastro e  solicitar sua aprovação.

<b>UC04 - Aprovar cadastro de usuário:</b>

Esse caso de uso permite que o assistente administrativo possa aprovar uma solicitação de cadastro feita por um usuário comum.

<b>UC05 - Administar salas:</b>

Esse caso de uso permite ao assistente administrativo adicionar, remover e alterar dados de uma sala.

<b>UC06 - Manter turma:</b>
Esse caso de uso permite ao coordenador e auxiliar do departamento cadastrar, editar, visualizar e remover uma turma.

<b>UC07 - Manter alocações:</b>

Esse caso de uso permite que o coordenador e o auxiliar do departamento possam alocar e realocar disciplinas em salas que são ditas do departamento, que pode ser referente ao curso no caso do coordenador.E no caso do assistente administrativo alocar e realocar disciplinas em salas de espaço comum.

<b>UC08 - Visualizar alocação:</b>

Esse caso de uso permite ao assistente administrativo, coordenador e auxiliar do departamento visualizarem as salas já alocadas à uma determinada disciplina e seus respectivos dias e horários.

<b>UC09 - Solicitar alocação em espaço comum:</b>

Esse caso de uso permite ao coordenador e ao auxiliar do departamento solicitarem alocação de disciplinas, onde irão pré-aloca-las a fim de serem aprovadas pelo assistente administrativo e serem organizadas e alocadas em espaço comum.

<b>UC10 - Gerenciar solicitadas de espaço comum:</b>

Esse caso de uso permite  ao assistente administrativo desalocar uma sala de uma disciplina, alocar disciplinas em salas vazias e alterar qualquer instância de alocação, após feita uma solicitação pelo coordenador ou auxiliar do departamento.

<b>UC11 - Gerar relatório:</b>

Esse caso de uso permite ao assistente administrativo, coordenador e auxiliar do departamento,gerarem relatórios referentes à alocação de sala.





<b>UC10 -Administar salas:</b>

Esse caso de uso permite ao assistente administrativo adicionar, remover e alterar dados de uma sala.




## 5. Visão Lógica


### 5.1 Visão Geral

O padrão arquitetural MVC separa a aplicação em três camadas: Model, View e Controller. Dentro da arquitetura essas camadas são implementadas por meio de três pacotes principais, de mesmo nome. Além destes se encontram pacotes de configurações. Nesta arquitetura, tanto a modelagem de dados, a interação do usuário e o processamento de requisições é designada a cada uma das camadas MVC respectivamente. A justificativa em separar a aplicação entre estes pacotes reside na fácil manutenibilidade, de forma que alterações feitas no layout da aplicação não alteram a modelagem de dados, e vice-versa.
A camada Model fica responsável por realizar a modelagem das entidades às quais o sistema deseja guardar dados. Apesar dela possuir todos os recursos relativos à manipulação dos dados, ela não tem autonomia para executá-los.
A View é a camada de interação com o usuário, responsável pela representação visual da Model. O acesso a Model é realizado através da Controller.
A Controller deve fazer a ligação entre a View e a Model, de maneira que receba as requisições do usuário e relacione a uma Model, retornando os dados à uma View. Ela deve tomar decisões de qual Model usar e que pedidos foram solicitados a ela.

### 5.2 MVC no Ruby on Rails

O dado sistema utilizará a arquitetura MVC utilizando o Framework Ruby on Rails. Este framework fornece todas as ferramentas necessárias à produção, manutenção e implementação de uma aplicação web. Ela segue uma hierarquia de pacotes bem determinada e se baseia em três bibliotecas principais: Active Record, Active View e Action Controller.

### 5.2.1 Estrutura de pacotes - Ruby on Rails

Em uma estrutura comum, os pacotes de uma aplicação Ruby on Rails se comportam da seguinte forma:

<ul>
	<li>app: Neste pacote estão os arquivos referentes a aplicação em si. É o pacote mais importante da aplicação, uma vez que guarda os pacotes referentes às camadas da MVC.</li>
	<li>bin: Neste pacote estão as ferramentas utilizadas durante a produção e manutenção da aplicação, como por exemplo a ferramenta rake, que cuida da interface com o Banco de Dados.</li>
	<li>config: Os arquivos de configuração se encontram neste pacote.</li>
	<li>db: Pacote que guarda configurações específicas referentes ao banco de dados.</li>
	<li>log: Arquivos de log.</li>
	<li>test: Essa pacote é responsável por armazenar os arquivos que cuidam dos testes do sistema.
<ul/>
