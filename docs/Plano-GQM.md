### Histórico de Revisão

| Data | Versão | Descrição | Autor(es) |
| :---: | :---: | --- | :---: |
| **02/04/2017** | 1.0 | Elaboração do Documento | Vinícius Carvalho |
| **05/04/2017** | 1.1 | Justificativa de Métricas | Vinícius Carvalho |
| **05/04/2017** | 1.2 | Contextualização das Questões | Vinícius Carvalho |
| **07/04/2017** | 1.3 | Revisão | Vinícius Carvalho |
| **17/04/2017** | 1.4 | Alteração da rastreabilidade GQM | Vinícius Carvalho |

# GQM (_Goal, Question, Metric_)

## OBJETIVOS ESTRATÉGICOS

O.1 - Qualidade do produto

<p align="justify">Dado que o sistema proposto deverá abranger as localidades da Universidade de Brasília e seus funcionários deverão utilizar posteriormente. O _software_ em produção será mantido pela equipe do CPD - Centro de Informática da UnB, e existe a necessidade de fazê-lo com alta manutenibilidade, para que o cliente não tenha problemas em preservá-lo. Isto é, um produto de software documentado, altamente padronizado e com bons indicadores de orientação a objeto. Maior foco será na parte de padronização de código (Folha de estilo) e bons indicadores de orientação a objeto, que serão evidenciados neste plano. Desta forma, o objetivo do GQM é:</p>

|**Analisar**|código|
|:---:|:---:|
|**Com o propósito de**|melhorar|
|**Com respeito a**    |Manutenibilidade do _software_|
|**Sobre o ponto de vista do**|desenvolvedor|
|**No contexto do**   |projeto SIGS|
------------------------------------

## QUESTÕES
<p align="justify">A questão anuncia a necessidade de se obter informações em
uma linguagem natural, podendo-se formular uma ou mais questões para
cada categoria de questões; quanto à resposta, deve estar de acordo com
o objetivo.</p>
<p align="justify">
O abstraction sheet facilita a comunicação entre a equipe de GQM e a equipe de projeto
durante o processo e a revisão do plano GQM representando uma visão simplificada do plano.</p>

|||
|:---:|:---:|
|**Foco na qualidade** <br/> **- Q.1.1** O produto apresenta uma boa manutenibilidade? <br/>|**Fatores de variação** <br/> - A produtividade não atender a expectativa; <br/> - Conhecimento da equipe limitado;|
|**Hipótese de baseline** <br/> - 30% de cobertura de teste até a primeira _release_; <br/> - 90% de cobertura de teste até a segunda _release_;|**Impacto das hipóteses de _baseline_**<br/> - Baixa qualidade do produto de _softwar_e;<br/> - Baixa manutenibilidade.|

## MÉTRICAS

<p align="justify">Essa seção descreve as métricas que serão aplicadas ao projeto como padrão de qualidade.<br/>Para cada métrica será dada uma descrição do que é a métrica, seus respectivos indicadores interpretativos, os resultados esperados para o projeto e as melhorias propostas para reverter quadros desfavoráveis, isto é, possíveis medidas que a equipe deve tomar para obter índices positivos quando estes estiverem comprometidos.
</p>

![Rastreabilidade GQM](https://raw.githubusercontent.com/wiki/fga-gpp-mds/Grupo---7-GPP-MDS/images/rastreabilidadeGQM2.png)

|Métrica|M.1.1.1 - Cobertura de teste|
|---|---|
|**Objetivo da Medição**|Garantir que o _software_ não contenha erros de lógica ou digitação, assim tendo uma garantia de qualidade.|
|**Descrição**|A cobertura de teste é dada pela proporção entre linhas testadas e a quantidade total de linhas de código. A cobertura de código é importante para acompanhar o andamento dos desenvolvimento dos testes. Testes estes que garantem a qualidade e quantidades mínimas de erros de desenvolvimento.|
|**Fórmula**|Cobertura = Linhas testadas / Linhas totais|
|**Escala da Medição**|Racional|
|**Coleta**|Responsável: Equipe de gerência.<br/> Periodicidade ou Evento: A cada iteração.<br/>Ferramenta: _**SimpleCov**_|
|**Procedimentos**| Será feito o uso da ferramenta no último _commit_ para obter os dados. Será mantido junto com as outras métricas em uma tabela para acompanhar o software.|
|**Análise**| Primeira _release_:<br/> “Dentro do esperado” dado por CoberturaTeste > 30%<br/>“Fora do planejado” dado por CoberturaTeste < 30% <br/> Segunda _release_: <br/> “Dentro do esperado” dado por CoberturaTeste > 90%<br/>“Fora do planejado” dado por CoberturaTeste < 90%|
|**Providências**| Caso a métrica esteja abaixo do esperado na primeira _release_, em qualquer uma das iterações que envolvam desenvolvimento, a equipe de gerência deve ser alertada e a coach (Monitora) deve ser procurada em caso de dificuldades.<br/> Caso a métrica esteja abaixo do esperado na segunda _release_, na primeira semana a equipe de desenvolvimento deve ser alertada apontada para possíveis materiais de ajuda. Se continuar por uma segunda semana, a equipe de gerência deve interferir, participando do desenvolvimento de testes.|

|Métrica|M.1.1.2 - Complexidade ciclomática (Flog)|
|---|---|
|**Objetivo da Medição**|Verificar a quantidade de caminhos de execução independentes.|
|**Descrição**|Complexidade ciclomática é o número de caminhos independentes dentro do grafo de nós dentro do sistema. Cada nó é um bloco de código sequencial do sistema.<br/>De forma resumida e sucinta, complexidade ciclomática equivale ao número de desvios (ou estruturas condicionais) mais 1. Como a coleta consiste em contar o número de condicionais, a métrica também é chamada de complexidade condicional. Ela indica o número de testes que o fragmento de software precisa ter para cobrir todos caminhos linearmente independentes de execução.|
|**Fórmula**|V(G) = e - n + p<br/>Onde V(G) é a complexidade ciclomática, n = vértice, e = aresta, p = componentes conectados<br/> A média é feita, M(V(G)), dando a complexidade ciclomática média.|
|**Escala da Medição**|Racional|
|**Coleta**|Responsável: Equipe de gerência.<br/> Periodicidade ou Evento: A cada iteração. <br/>Ferramenta: _**Rubycritic**_|
|**Procedimentos**| Será feito o uso da ferramenta no último _commit_ para obter os dados. Será mantido junto com as outras métricas em uma tabela para acompanhar o _softwar_e.|
|**Análise**|De acordo com a ferramenta, baseado em conhecimentos empíricos: <br/> 0 a 25 - Nível aceitável <br/> 26 a 60 - Refatoração de método <br/>61 e acima - Muito complexa (perigo)  |
|**Providências**|Como a métrica de complexidade ciclomática verifica o número de caminhos independentes no código, é necessário diminuir o número de estruturas que causem isso. Loops, Condicionais e recursividades. Caso a métrica esteja acima do esperado, na primeira semana a equipe de desenvolvimento deve ser alertada e apontada para possíveis materiais de ajuda. Se continuar por uma segunda semana, a equipe de gerência de interferir, participando da manutenção do código.|

|Métrica|M.1.1.3 - Duplicações de Código (Flay)|
|---|---|
|**Objetivo da Medição**| Garantir o reaproveitamento de código, reduzindo duplicação de código idêntico ou semelhante.|
|**Descrição**| A análise estática também pode identificar código idêntico e semelhante. A ferramenta procura árvores de sintaxe grandes e idênticas e também usa correspondência fuzzy para detectar código que difere apenas pelos identificadores e constantes específicos usados.|
|**Fórmula**|Quantidade de sintaxes idênticas ou semelhantes presentes no código.|
|**Escala da Medição**|Racional|
|**Coleta**|Responsável: Equipe de gerência.<br/> Periodicidade ou Evento: A cada iteração. <br/>Ferramenta: _**Rubycritic**_|
|**Procedimentos**| Será feito o uso da ferramenta no último _commit_ da iteração para obter os dados. Será mantido junto com as outras métricas em uma tabela para acompanhar a evolução do _software_.|
|**Análise dos indicadores**| Os resultados devem apresentar índices abaixo de 25, o que indica um código com pouquíssima duplicação de código e potencialmente manutenível.|
|**Providências**| Como a métrica de conexões aferente se refere a acoplamento, então esta deve ser tratada diminuindo o número de classes que conversão com a classe em questão. Talvez isso se dê por uma falta de coesão, ou seja, informações que deveriam estar juntas estão em lugares diferentes. Caso a métrica esteja acima do esperado, na primeira semana a equipe de desenvolvimento deve ser alertada e apontada para possíveis materiais de ajuda. Se continuar por uma segunda semana, a equipe de gerência de interferir, participando da manutenção do código.|

|Métrica|M.1.1.4 - Quantidade de Alterações (Churn)|
|---|---|
|**Objetivo da Medição**|Monitorar alterações de arquivos de origem.|
|**Descrição**| Contagem do número de vezes que uma classe foi modificada no seu histórico de controle de versão. |
|**Fórmula**|Número de alterações no arquivo.|
|**Escala da Medição**|Racional|
|**Coleta**|Responsável: Equipe de gerência.<br/> Periodicidade ou Evento: A cada iteração. <br/>Ferramenta: _**Rubycritic**_|
|**Procedimentos**| Será feito o uso da ferramenta no último _commit_ para obter os dados. Será mantido junto com as outras métricas numa tabela para acompanhar o _software_.|
|**Análise**| Verificada no indicador I.1|

|Métrica|M.1.1.5 - Checkstyle|
|---|---|
|**Objetivo da Medição**|Garantir a manutenibilidade do código.|
|**Descrição**|Analisador estático de código para checar se o código fonte está de acordo com as regras de codificação na linguagem especificada. Auxilia nas boas práticas de programação na qual melhora-se a qualidade do código, reusabilidade, clareza, entre outros fatores.|
|**Fórmula**|Não se aplica|
|**Escala da Medição**|Racional|
|**Coleta**|Responsável: Equipe de gerência.<br/>Periodicidade ou Evento: A cada iteração.<br/> Ferramenta: _**Rubocop**_|
|**Procedimentos**| Será feito o uso da ferramenta no último _commit_ para obter os dados. Será mantido junto com as outras métricas numa tabela para acompanhar o _software_.|
|**Análise dos indicadores**|Indicação de trechos não condizentes com a convenção da linguagem.|
|**Providências**|  Refatoração do código com o objetivo de seguir as regras e a convenção da linguagem.|

|Métrica|M.1.2.1 - Falhas de Segurança |
|---|---|
|**Objetivo da Medição**| Garantir a segurança do software. Contribuir para redução de vulnerabilidades em sistemas complexos.|
|**Descrição**| Esta medição atuará sobre a vulnerabilidade de código. A ferramenta auxilia a analisar esteticamente o código do aplicativo Rails para encontrar problemas de segurança em qualquer estágio de desenvolvimento.|
|**Fórmula**|Não se aplica|
|**Escala da Medição**|Racional|
|**Coleta**|Responsável: Equipe de gerência.<br/> Periodicidade ou Evento: A cada iteração. <br/>Ferramenta: _**Brakeman**_|
|**Procedimentos**| Será feito o uso da ferramenta no último _commit_ para obter os dados. Será apresentado um relatório de todos os problemas de segurança encontrados pela ferramenta.|
|**Análise e indicadores**| A ferramenta _Brakeman_ oferece as seguintes diretrizes:<br/><br/> **Alto**: Muito provável que a entrada do usuário seja usada de forma insegura. <br/> **Médio**:Uso inseguro de uma variável, podendo ou não ser entrada do usuário. <br/>**Fraca**:Normalmente significa que a entrada do usuário foi indiretamente usada de uma maneira potencialmente insegura. <br/><br/> O considerado ideal para este projeto é o indicador **Alta**. |
|**Providências**| Mitigação de vulnerabilidades.|

## INDICADORES
---------------------------------
|Indicador|I.1 - Turbulência |
|---|---|
|**Objetivo**| Verificar partes de código que necessitam de refatoração.|
|**Descrição**| A relação de _Churn_ e Complexidade nos apresenta os arquivos que estão gerando mais dificuldades para o projeto e para os desenvolvedores.|
|**Fórmula**|_Churn_ x Complexidade|
|**Escala da Medição**|Racional|
|**Coleta**|Responsável: Equipe de gerência.<br/> Periodicidade ou Evento: A cada iteração. <br/>Ferramenta: _**Rubycritic*_|
|**Procedimentos**| Será feito o uso da ferramenta no último _commit_ para obter os dados. Será apresentado um relatório de todos os problemas de segurança encontrados pela ferramenta.|
|**Análise e indicadores**| A ferramenta oferece um gráfico, e a partir da análise dessa figura, utiliza-se as seguintes diretrizes:<br/><br/>**Superior direito** - Classes com alta complexidade e alto _churn_. Essas são boas prioridades para a refatoração pois seus problemas de manutenção estão afetando os desenvolvedores em uma base regular.<br/>**Superior esquerdo** - Classes com alta complexidade e baixo _churn_. Possui menor prioridade de refatoração, porém possui código com necessidade de depuração.<br/>**Inferior esquerdo** - Classes com baixo _churn_ e baixa complexidade. O melhor tipo de resultado a ter. A maior parte do código deve estar neste quadrante.<br/>**Inferior direito** - Classes com baixa complexidade e alto _churn_. Pode ser justificada por refatorações constantes, não há muito o que refatorar neste caso. |
|**Providências**| Refatoração do código.|
