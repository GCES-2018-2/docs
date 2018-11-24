# Plano de Gerenciamento de Riscos

## Histórico de Revisão

| Data       | Responsável          |Versão   | Mudança realizada                            |  
|------------|----------------------|---|--------------------------------------------------- |
|**25/03/17**|  Lucas Andrade | 0.1  | Introdução e estrutura do Documento |
|**29/03/17**|  Lucas Andrade | 0.2  | Processo de gerenciamento de riscos |
|**30/03/17**|  Lucas Andrade | 0.3  | SWOT                   |
|**31/03/17**|  Lucas Andrade | 0.4  | Descrição e tabela Crawford Slip |
|**10/04/17**|  Lucas Andrade | 1.0  | Análise qualitativa e quantitativa.  Categorizando os riscos, respostas aos riscos e EAR |
|**15/04/17**|  Lucas Andrade | 1.1  | Revisão Geral do documento |
|**18/04/17**|  Lucas Andrade | 1.2  | Corrigindo de acordo com a revisão da monitoria |

## 1.0 Introdução
Este documento tem como objetivo identificar os possíveis riscos do projeto, descrever e entender os mesmos, bem como apresentar estratégias que a equipe pretende usar para contornar cada um deles seguindo o processo de gerenciamento de riscos elaborado pelo time de GPP. Também estão descritos os riscos negativos e positivos para o projeto. 
###### *GPP: gestão de de portfólio e projetos de software*

## 2.0 Processo de gerenciamento dos riscos
O processo de gerenciamento dos riscos segue o fluxo de atividades listado abaixo, e deve ser seguido em ordem de acordo com a numeração de 01 até 05

![Processo de gerenciamento dos riscos](https://raw.githubusercontent.com/wiki/fga-gpp-mds/Grupo---7-GPP-MDS/images/riscos/processo_riscos.png)


**Identificar os riscos:** consiste em determinar quais são os riscos que podem afetar o projeto e descrevê-los.

**Análise qualitativa:** Permite o gerente de projetos atribuir a cada risco uma probabilidade referente a possibilidade ocorrência de impacto e assim priorizar os riscos de acordo com a chance desse risco se tornar real. 
Técnica: matriz de probabilidade e impacto

**Análise quantitativa:** É uma análise numérica dos efeitos dos riscos nos objetivos do projeto, com isso o gerente de projetos tem uma facilidade maior durante a tomada de decisões reduzindo o grau de incerteza a respeito dos riscos no projeto.
	Técnica: Análise de Sensibilidade

**Elaborar Respostas:** Consiste em planejar respostas e ações para reduzir as ameaças que cada risco tem no projeto, isso é feito escolhendo os riscos de maior prioridade e adequando o planejamento e o cronograma caso esses riscos se tornem reais.
Técnica: Elaborar estratégias para os principais riscos positivos e negativos do projeto.

**Controlar e Monitorar:** Essa é a atividade de implementação das respostas aos riscos. A equipe de gerenciamento deve monitorar os riscos a fim de abordá-los ao longo de todo o projeto otimizando a aplicação das respostas sobre os mesmos.

## 3.0 Identificação dos riscos
### 3.1 SWOT
A identificação dos riscos foi feita usando um template de *SWOT* (forças, fraquezas, oportunidades e ameaças) que elucida de forma simples e objetiva os principais riscos presentes no projeto

![SWOT](https://raw.githubusercontent.com/wiki/fga-gpp-mds/Grupo---7-GPP-MDS/images/riscos/swot_v01.png)

### 3.2 Crawford Slip
Para um detalhamento melhor dos riscos a equipe usou da técnica [Crawford Slip](http://www.gestaodeprojetos.com.pt/index.php/risco-todos-os-artigos/122-crawford-slip-method-na-identificacao-de-riscos), que é basicamente um brainstorm que tem como premissas ser rápido e simples, seguindo a ideia do KISS (Keep It Short and Simple). Nessa técnica os membros da equipe listam e descrevem os riscos identificados por cada um. Em seguida cada um apresenta sua lista e ao final é gerado um pequeno relatório com os principais riscos do projeto de forma mais detalhada.
Essa técnica foi escolhida pois ela permite levantar um grande número de riscos em um curto período de tempo, além de promover uma integração maior da equipe pois ela considera e valoriza a opinião de todos os membros.

| ID  | Descrição                                                                      | Causa                                                                                                 | Afeta                                                                               | Tipo     |
|-----|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|----------|
| R01 | Possível greve na UNB, tendo em vista os recentes protestos dos sindicatos.| Mudanças drásticas no cronograma e no planejamento | Afeta a equipe e todo o processo de desenvolvimento | Negativo |
| R02 | Falta de dados digitalizados (lista com todas as salas e disciplinas do darcy) | Uma mudança no cronograma e um atraso no projeto | Afeta o projeto e compromete a base de dados do projeto | Negativo |
| R03 | Atraso nas atividades  | Sobrecarrega alguns integrantes do grupo e compromete a entrega dentro do prazo                       | Afeta o resultado final do projeto  | Negativo |
| R04 | Erro de estimativa do planejamento do projeto                                  | Mudanças no cronograma                                                                                | Afeta as entregas previstas no projeto                                              | Negativo |
| R05 | Saída de membros  | Mudança no planejamento como um todo | Afeta o tempo de trabalho estimado para cada membro da equipe                       | Negativo         |
| R06 | Falta de informações por parte do cliente                                      | Constante mudanças no planejamento do projeto e no escopo do mesmo                                    | Afeta a estimativa de custos e da execução das atividades                           | Negativo |
| R07 | Desmotivação da equipe                                                         | Membros desmotivados, ou seja, baixa produtividade                                                    | Afeta as entregas dentro de seus respectivos prazos atrasando o projeto             | Negativo |
| R08 | Cliente Indeciso                                                               | Constante mudanças no projeto, retrabalho e refatoração                                               | Afeta os custos do projeto, o valor planejado e as entregas planejadas               | Negativo |
| R09 | Código sem técnicas de boas práticas de programação | Custo maior caso necessite de uma refatoração                                                         | Afeta a qualidade do projeto e as entregas previstas.                       | Negativo |
| R10 | Inexperiência da equipe                   | Maior custo com treinamentos               | Afeta o planejamento                      | Negativo |
| R11 | Relacionamento entre os membros da equipe | Causa execução “desregular” das atividades | Afeta a divisão e execução das atividades | Negativo |
| R12 | Entregas dentro do planejado                                                   | Consistência no projeto                                                                               | Afeta o planejamento de certa forma                                                                                | Positivo |
| R13 | Equipe motivada a continuar o projeto                                          | Continuação no projeto, ou seja, elaboração de novas atividades de gerenciamento e de desenvolvimento | Afeta a experiência da equipe e a satisfação do cliente com o resultado do projeto. | Positivo |

## 4.0 Análise dos riscos
Para uma análise completa dos riscos é necessário primeiro atribuir um valor a cada um dos riscos (análise qualitativa) e em seguida realizar uma análise sobre os riscos de acordo com seus respectivos valores (análise quantitativa).

### 4.1 Análise Qualitativa
É uma análise entre probabilidade e impacto de forma qualitativa, ou seja, apenas entre valores baixo, médio e alto (probabilidade relativa). Assim é possível priorizar os riscos para em seguida atribuir um valor em porcentagem sobre a probabilidade (análise quantitativa) e impacto de cada um deles.
(página 328 - 329 PMBOK 5º edição português)

#### 4.1.1 Definindo valores de acordo com a probabilidade

| Probabilidade | Peso |
|---------------|------|
| Muito Baixa   | 1    |
| Baixa         | 2    |
| Moderada      | 3    |
| Alta          | 4    |
| Muito Alta    | 5    |

#### 4.1.2 Definindo valores de acordo com o impacto no projeto

| Impacto     | Descrição                                                                                           | Representação |
|-------------|-----------------------------------------------------------------------------------------------------|---------------|
| Muito baixo | Impacto com poucos danos no projeto                                                                 | 1             |
| Baixo       | Impacto com danos minimamente relativos no projeto                                                  | 2             |
| Moderado    | Impacto com dados consideráveis no projeto, porém passível de recuperação                           | 3             |
| Alto        | Impacto com dados mais significativos no projeto com uma recuperação complicada (fora do orçamento) | 4             |
| Muito Alto  | Impacto que impede a conclusão do projeto                                                           | 5             |

#### 4.1.3 Prioridade
Prioridade de acordo com os os valores usados na matriz de probabilidade e impacto.

| Prioridade | Intervalo |
|------------|-----------|
| Baixa      | 1-5       |
| Média      | 6-15      |
| Alta       | 16-25     |

#### 4.1.4 Matriz de probabilidade de impacto

| Impacto \ Probabilidade | Muito baixo | Baixo        | Moderado      | Alto | Muito Alto |
|-------------------------|-------------|--------------|---------------|------|------------|
| Muito baixo             | 1           | 2            | 3             | 4    | 5          |
| Baixo                   | 2           | 4 (R07)      | 6 (R03)       | 8    | 10         |
| Moderado                | 3 (R13)     | 6 (R09, R11)      | 9 (R04, R12)  | 12   | 15         |
| Alto                    | 4           | 8 (R05, R08, R10) | 12 (R02, R06) | 16   | 20         |
| Muito Alto              | 5           | 10 (R01)     | 15            | 20   | 25         |

### 4.2 Análise Quantitativa
Com os riscos já priorizados, abaixo temos uma análise quantitativa estabelecendo um valor mais real sobre a chance daquele risco acontecer. Abaixo temos uma tabela com a probabilidade em porcentagem de acordo com a probabilidade relativa.

| Probabilidade | Valor                      |
|---------------|----------------------------|
| Muito baixa   | 0% <= P < 20% média = 10%  |
| Baixa         | 20% <= P < 40% média = 30% |
| Moderada      | 40% <= P < 60% média = 50% |
| Alta          | 60% <= P < 80% média = 70% |
| Muito alta    | 80%<= P < 100% média = 90% |

Abaixo temos uma tabela que mostra o impacto no projeto, indicando quantos membros da equipe vão ter que trabalhar uma semana (12 horas) para resolver pendências/problemas sobre o impacto do projeto caso o risco se torne real. 
Preço por hora: R$ 15,30

| Impacto     | Membros / Tempo (semana) | Custo Total |
|-------------|--------------------------|-------------|
| Muito baixo | 1 / 1 semana             | R$ 183,60   |
| Baixo       | 2 / 1 semana             | R$ 367,20   |
| Moderado    | 3 / 1 semana             | R$ 550,80   |
| Alto        | 4 / 1 semana             | R$ 734,40   |
| Muito Alto  | 5 / 1 semana             | R$ 918,00   |

#### 4.2.1 Valor monetário esperado (VME)
O valor monetário esperado tem o objetivo de mostrar uma estimativa de custo com base no impacto do risco sobre o projeto e na probabilidade do mesmo acontecer. O VME é calculado pela multiplicação da probabilidade do risco pela sua estimativa de custo. Assim temos que: VME = % Risco * Custo estimado do risco. 

| ID  | Descrição                                                                      | Probabilidade (%) | Impacto (R$) | Valor Esperado (R$) |
|-----|--------------------------------------------------------------------------------|-------------------|--------------|---------------------|
| R01 | Possível greve na UNB, tendo em vista os recentes protestos dos sindicatos.    | 30%               | 918          | 275,4               |
| R02 | Falta de dados digitalizados (lista com todas as salas e disciplinas do darcy) | 50%               | 734,4        | 367,2               |
| R03 | Atraso nas atividades                                                          | 50%               | 367,2        | 183,6               |
| R04 | Erro de estimativa do planejamento do projeto                                  | 50%               | 550,8        | 275,4               |
| R05 | Saída de membros                                                               | 30%               | 734,4        | 220,32              |
| R06 | Falta de informações por parte do cliente                                      | 50%               | 734,4        | 367,2               |
| R07 | Desmotivação da equipe                                                         | 30%               | 367,2        | 110,16              |
| R08 | Cliente indeciso                                                               | 30%               | 734,4        | 220,32              |
| R09 | Código mal feito                                                               | 30%               | 550,8        | 165,24              |
| R10 | Inexperiência da equipe | 30% | 734,4 | 220,32 |
| R11 | Relacionamento entre os membros da equipe | 30% | 550,8 | 165,24 |

## 5.0 Categorizando os riscos
A EAR (estrutura analítica de riscos) permite identificar a área de atuação de cada risco, assim a equipe de gerenciamento pode determinar quais áreas do projeto necessitam de mais atenção
Além disso a categorização dos riscos ajuda a organizar os riscos de acordo com sua área de possível atuação, assim fica mais fácil deseguinar um responsável por aquele risco

![EAR - Estrutura analítica de riscos](https://raw.githubusercontent.com/wiki/fga-gpp-mds/Grupo---7-GPP-MDS/images/riscos/ear.png)


## 6.0 Monitoramento e controle
Com o objetivo de mitigar ou até mesmo de evitar que um risco de torne real, foi definida uma prioridade para cada um dos riscos, bem como um responsável pelo risco e uma resposta/ação caso ele venha a acontecer. Essas medidas permitem que os responsáveis pelos riscos consigam determinar uma estratégia e realizar o monitoramento e controle dos mesmos.

| ID  | Prioridade | Responsável       | Resposta                                                                           |
|-----|------------|-------------------|--------------------------------------------------------------------------------------|
| R01 | 10 (média) | Lucas             | Prevenir - Replanejamento do plano de gerenciamento e do cronograma                  |
| R02 | 12 (média) | Gesiel            | Prevenir - Procurar bases de dados que possam contribuir com arquivos                |
| R03 | 6 (média)  | Vinícius Carvalho | Mitigar - Replanejamento do cronograma                                               |
| R04 | 9 (média)  | Vinícius Pinheiro | Mitigar - Adequar futuras estimativas as estimativas reais                           |
| R05 | 8 (média)  | Gesiel            | Mitigar - Redistribuir atividades e responsabilidades                                |
| R06 | 12 (média) | Lucas             | Mitigar - Marcar novas entrevistas com o cliente                                     |
| R07 | 4 (baixa)  | João Bush         | Mitigar - Aumentar a cobrança e promover maior integração entre os membros da equipe |
| R08 | 8 (média)  | Jõao Bush         | Prevenir - Usar técnicas de elicitação de requisitos mais objetivas                  |
| R09 | 6 (média)  | Vinícius Carvalho | Prevevir - Promover mais treinamentos sobre qualidade de código, aumentar cobrança   |
| R10 | (média)   | Vinícius Carvalho | Prevenir - Promover mais treinamentos sobre a tecnologia usada (front-end e back-end) |
| R11 | 6 (média) | Caio              | Prevenir - Promover a integração da equipe a incentivar o trabalho em equipe          |
| R12 | 9 (média)  | Lucas             | Explorar - Incentivar a equipe a manter o desempenho                                 |
| R13 | 3 (baixa)  | Lucas             | Aproveitar - Aproveitar oportunidades                                                |


## 7.0 Referências
PMBOK 5º EDIÇÃO, página 324, 11.2.2 Identificar os riscos: ferramentas e técnicas
PMBOK 5º EDIÇÃO, página 329, 11.3.1 Realizar a análise qualitativa dos riscos: entradas
PMBOK 5º EDIÇÃO, página 335, 11.4.1 Realizar a análise quantitativa dos riscos: entradas
PMBOK 5º EDIÇÃO, página 339, 11.4.2.2 Técnicas de modelagem e análise quantitativa dos riscos, Análise do valor monetário esperado
PMBOK 5º EDIÇÃO, página 341, 11.4.3 Realizar a análise quantitativa dos riscos: saídas
PMBOK 5º EDIÇÃO, página 342,11.5.1 Planejar as respostas aos riscos: entradas
PMBOK 5º EDIÇÃO, página 344, 11.5.2.1 Estratégias para riscos negativos ou ameaças
PMBOK 5º EDIÇÃO, página 345, 11.5.2.2 Estratégias para riscos positivos ou oportunidades