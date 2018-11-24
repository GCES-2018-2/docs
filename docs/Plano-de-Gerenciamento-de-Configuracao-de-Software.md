## Histórico de Revisão

| Data       | Responsável          |Versão   | Mudança realizada                            |  
|------------|----------------------|---|--------------------------------------------------- |
|**16/03/17**|  Vinícius Carvalho   | 0.1  | Criação do Documento de Configuração de Software|
|**18/03/17**|  Vinícius Carvalho   | 0.2  | Inserção dos subtópicos "Visão Geral","Finalidade" e "Escopo"|
|**18/03/17**|  Vinícius Carvalho   | 0.3  | Inserção do tópico "Ambiente"                   |
|**25/03/17**|  Lucas Andrade       | 1.0  | Finalização do Plano de GCS                     |
|**09/04/17**|  Vinicius Pinheiro   | 1.1  | Revisão geral                                   |
|**27/04/17**|  Vinícius Carvalho e Rodrigo Dadamos | 1.2  | Inserção de como realizar commit com mais de um colaborador|

## 1 Introdução
O Plano de Gerência de Configuração do SIGS (Sistema Inteligente de Gestão de Salas) apresenta todas as tarefas do Gerenciamento de configuração e mudanças no projeto, para garantir a sua integridade e manter o domínio das mudanças ocorridas durante o desenvolvimento. Neste documento detalha-se toda a infraestrutura utilizada nesse projeto. São definidos itens como: uma padronização para os documentos, uma ferramenta de controle da instalação da aplicação, preparo do ambiente de desenvolvimento de forma otimizada, integração ferramenta de controle de testes e por fim relatar os resultados da implantação da gerência de configuração de software. Para isso, devem ser seguidas diretrizes apresentadas em tópicos pelo plano de gerência.

### 1.1 Resultados esperados
Com a implantação deste plano espera-se diminuir as ocorrências de problemas na configuração da aplicação em outros ambientes, além de garantir maior qualidade no desenvolvimento de testes da aplicação, assegurando que as entregas de software aceitas estejam no nível aceitável definido pela equipe de gerência.

### 1.4 Definições, Acrônimos e Abreviações
|Termo   |Significado                                                                             |
|--------|----------------------------------------------------------------------------------------|  
|_Baseline_|Conjunto de itens de configuração que conseguiram um estado comprovado de estabilidade. |                 
|GCS     |Gerência de Configuração de _Software_                                                    |
|CR      |Solicitação de Mudança (_Change Request_)                                               |  


## 2 Organização

### 2.1 Identificação dos documentos
Todos os artefatos produzidos devem manter o nome seguindo o título do artefato sem abreviação.
Ex:`Plano de Gerência de Configuração`.
Os únicos artefatos que podem ter abreviação são os `Casos de Uso`. Neste caso, o nome do artefato deverá ser: `UC<Número> - <Nome do caso de uso>`.

### 2.2 Localização dos Artefatos
Todos os artefatos devem estar localizados nesta wiki e dentro de sua categoria. As categorias são:
* 1 - Gerenciamento de Projeto
* 2 - Desenvolvimento de Software
Dentro dos respectivos períodos para entrega de uma versão estável e executável do software, divididas em _Release_ 1 e _Release_ 2.

### 2.3 Versão dos Artefatos
O versionamento dos artefatos será feito por tabela de Histórico de Versão no próprio documento. Os artefatos podem ser desenvolvidos na ferramenta Google Drive, ou diretamente na wiki deste GitHub.

### 2.4 _Baseline_ do Projeto

A baseline será gerada a cada fim de iteração do projeto, tendo assim um incremento no número da versão do sistema `1.0`, no caso de atualizações e correções de erros em versões passadas, deve-se utilizar o código da versão anterior sendo que o dígito após o "ponto" deve ser acrescido um `1.1`.

### 2.5 _Branches_
Essa seção determina as políticas de _branches_ utilizada no processo.
* Haverão duas _branches_ principais, a **master** e a **development**;
* A master manterá a versão entregável do projeto;
* A _development_ será utilizada para a equipe de gestão avaliar os _commits_ e coletar as métricas;
* O incremento à master, ocorrerá através de _pull request_ advindo da _branch development_ e será de responsabilidade exclusiva da equipe de gestão;
* O incremento à _development_ ocorrerá através de _pull request_ advindo das _branches_ de desenvolvimento, onde a aceitação ou recusa do _pull request_ será de responsabilidade da equipe de gestão;
* Só poderão ser criadas _branches_ de desenvolvimento apenas se forem relacionadas a casos de usos à serem implementados ou para mudanças no sistema;
* O nome das _branches_ de desenvolvimento devem seguir o modelo `uc<número do caso de uso em dois dígitos>_<nome do caso de uso>` ou `cr<número da _milestone_>_<número da issue>_<nome da _issue_>`.
Obs.: Se o nome do caso de uso/mudanças no sistema conter espaços, estes devem ser substituídos por `underline` e todas as letras devem ser minúsculas.


## 3. Controle de Mudança

### 3.1 Milestones
As solicitações de mudanças devem ser criadas através de _issues_ disponibilizadas neste repositório. Deve ser criada uma _milestone_ com o título `<CRXX>`, a descrição deve conter a informação de quais casos de uso essa _milestone_ irá afetar e deve haver uma data limite para conclusão.

### 3.2 Issues
Após a criação da _milestone_, deve ser criado uma _issue_ para cada solicitação de alteração. Cada _issue_ deve ter um título simples que dite a mudança. Na descrição deve haver:
* Data da Solicitação;
* Data da Aprovação;
* Quem aprovou a alteração;
* Especificação da alteração.

A _issue_ deve ser ligada a sua _milestone_. O uso da _milestone_ é para agrupar algumas solicitações em um pacote de alterações com prazo de entrega.

## 4. Commits

### 4.1 Comentário do _commit_
Os nomes dos commits devem ser relevantes ao conteúdo inserido ou retirado do repositório. Devem ser inscritos em língua Inglesa e conteúdo significativo, suficiente para identificação do que e onde houve alteração de código.
> Exemplo: ` git commit -m "Added first list of mailing lists in manage subscriptions"`

### 4.2 Política de Commits
Quando houver pareamento em um _commit_ deve-se usar:
> Exemplo: ` git commit --author user_name`

Em que o *user_name* é o nome do usuário com o qual está pareando.
> Exemplo: ` git commit --author vinisilvacar`

O commit deverá estar associado diretamente a um membro da equipe. No caso de pareamento, o commit deve possuir a assinatura de ambos. O _commit_ deverá ter uma descrição para indicar o que foi solucionado.

Outra forma de editar um _commit_ seria o uso do comando:
> Exemplo: ` git commit -s`

Este comando abrirá o editor de texto e deverá seguir o seguinte padrão:
O título para o commit, o nome da tarefa em desenvolvimento, uma breve descrição para o que foi feito naquele commit e o `Signed-off-by: "Nome do Usuario" example@email.com` mesmo se o commit foi dado apenas por uma pessoa. Ao fazer pareamento ou dojo deve haver o Signed-off-by com todos os contribuidores.

![Editor de Texto com comando -s](https://raw.githubusercontent.com/wiki/fga-gpp-mds/2017.1-SIGS/images/comandoGitCommitS.png)

### 4.3 Solicitação de Mudanças
Deve seguir o tópico 4.1 e no conteúdo do _commit_ e deve haver o código da _issue_ gerado pelo Github.
> Exemplo: ` git commit -m "issue #X Added first list of mailing lists in manage subscriptions"`

## 5. Ambiente
### 5.1 Vagrant
O Vagrant é uma ferramenta para a construção de ambientes de desenvolvimento completo, permite a criação rápida de ambientes virtuais auxiliando a criação da infraestrutura para a realização de testes, desenvolvimento ou provisionamento de ambientes utilizando uma das soluções de virtualização mais comuns, o Virtualbox, no caso desse trabalho.

Acesse o [Tutorial de Instalação do ambiente](https://github.com/fga-gpp-mds/Grupo---7-GPP-MDS/wiki/Comandos-de-Instala%C3%A7%C3%A3o-do-Ambiente).

### 5.2 Puppet
É uma ferramenta livre que usa uma linguagem declarativa para configurar sistemas operacionais. Ele automatiza o processo de entrega de software, permitindo o provisionamento de máquinas físicas ou virtuais, a orquestração, a emissão de relatórios, ou ainda a distribuição de códigos em fase inicial de desenvolvimento, testes, lançamentos ou atualizações.

A automatização da instalação de pacotes foi realizada através do provisionador Puppet, os comandos deste provisionador são escritos em arquivos chamados ''manifests'', com uma linguagem baseada no Ruby. O ''manifest'' utilizado no projeto está exemplificado a seguir, nele é executado um ''update'' do sistema e são instaladas as seguintes dependências: ...

O puppet na declaração de suas classes tem alguns comandos que podem ser utilizados, os usados aqui foram o exec{}(executa shell code), o package{}(gerencia pacotes), file{}(gerencia arquivos) e service{}(gerencia serviços)

## 6. Ferramentas
A tabela abaixo descreve as ferramentas que serão utilizadas no desenvolvimento do projeto SIGS.

|Ferramenta   |Descrição                                                                             |
|-------------|--------------------------------------------------------------------------------------|  
|Travis CI    | Integração Contínua                                                                  |
|Git          | Controle de Versão                                                                   |
|Github       | Serviço Web Hosting Compartilhado                                                    |
|Heroku       | Deploy contínuo                                                                      |

### 6.1 TravisCI
O Travis CI proporciona um ambiente de build padrão e um conjunto padrão de etapas para cada linguagem de programação. É possível personalizar qualquer passo neste processo através do arquivo ''.travis.yml''. O Travis CI usa o arquivo .travis.yml na raiz do repositório para tomar conhecimento sobre o projeto e como  a build deve ser executada. O travis.yml pode ser escrito de forma minimalista ou detalhado. Alguns exemplos de que tipo de informação o arquivo .travis.yml pode ter:
* Que linguagem de programação o projeto usa;
* Quais comandos ou scripts devem ser executados antes de cada compilação (por exemplo, para instalar ou clonar as dependências do projeto);
* Qual comando é usado para executar o conjunto de testes.

#### 6.1.1 Motivação
As principais motivações para a escolha do Travis CI foram:
* Ele é gratuito para repositórios públicos;
* Ser um serviço de Integração Contínua na nuvem que pode ser conectado a repositórios no GitHub;
* Notifica o usuário (por e-mail) sobre resultados da build;
* Vasta documentação;
* Rápida curva de aprendizado.

##### Acesse [Travis-CI](https://travis-ci.org/) para acompanhar o status do build.

## 7. Deployment
Ao longo do desenvolvimento a aplicação ficará hospedada no [heroku](https://www.heroku.com/). Após a conclusão do desenvolvimento do projeto e a  entrega final para o cliente o sistema deverá ser hospedado em algum servidor da UnB
