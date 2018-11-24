| Data       | Responsável          |Versão   | Mudança realizada                            |  
|------------|----------------------|---|--------------------------------------------------- |
|**08/05/17**| Vinícius Pinheiro    | 0.1  | Criação   |
|**08/05/17**| Vinícius Pinheiro    | 0.2  | Adicionando Histórias Técnicas   |

# 1. Backlog do Produto

Abaixo se encontram as histórias de usuário elicitadas para a Release 2 do projeto SIGS. O backlog pode ter seu desenvolvimento acompanhado em nosso [KanBan](https://github.com/fga-gpp-mds/2017.1-SIGS/projects/1)

## 1.1 User Stories
<table>
<tr>
<th>Épicos</th>
<th>Features</th>
<th>User Stóries</th>
<th>Pontos</th>
</tr>
<tr>
  <td rowspan="20">EP01 - Coordenação de alocação</td>
  <td rowspan="8">FE01 - Gerenciar alocações</td>
  <td>US01 - Realizar/Confirmar alocação</td>
  <td>8pt</td>
</tr>
<tr>
  <td>US02 - Visualizar alocação</td>
  <td>3pt</td>
</tr>
<tr>
  <td>US03 - Alterar alocação</td>
  <td>8pt</td>
</tr>
<tr>
  <td>US04 - Excluir alocação</td>
  <td>3pt</td>
</tr>
<tr>
  <td>US05 - Solicitar alocação de sala</td>
  <td>13pt</td>
</tr>
<tr>
  <td>US06 - Aprovar solicitação de alocação</td>
  <td>2pt</td>
</tr>
<tr>
  <td>US07 - Negar solicitação de alocação</td>
  <td>2pt</td>
</tr>
<tr>
  <td>US08 - Visualizar solicitações de alocação</td>
  <td>2pt</td>
</tr>
<tr>
  <td rowspan="4">FE02 - Manter Turma</td>
  <td>US09 - Criar turma</td>
  <td>8pt</td>
</tr>
<tr>
  <td>US10 - Visualizar turma</td>
  <td>3pt</td>
</tr>
<tr>
  <td>US11 - Alterar turma</td>
  <td>5pt</td>
</tr>
<tr>
  <td>US12 - Excluir turma</td>
  <td>3pt</td>
</tr>
<tr>
  <td rowspan="4">FE03 - Gerar relatório</td>
  <td>US13 - Gerar relatórios de alocação por departamento</td>
  <td>5pt</td>
</tr>
<tr>
  <td>US14 - Gerar relatórios de alocação por disciplina</td>
  <td>3pt</td>
</tr>
<tr>
  <td>US15 - Gerar relatórios de alocação por prédio</td>
  <td>3pt</td>
</tr>
<tr>
  <td>US16 - Gerar relatórios de alocação por sala</td>
  <td>3pt</td>
</tr>
<tr>
  <td rowspan="4">FE04 - Gerenciar salas</td>
  <td>US17 - Visualizar sala</td>
  <td>2pt</td>
</tr>
<tr>
  <td>US18 - Alterar sala</td>
  <td>3pt</td>
</tr>
<tr>
  <td>US19 - Excluir sala</td>
  <td>2pt</td>
</tr>
<tr>
  <td>US25 - Visualizar local da sala no mapa</td>
  <td>21pt</td>
</tr>

<tr>
  <td rowspan="5">EP02 - Disponibilizar os dados</td>
  <td rowspan="5">FE05 - Fazer API</td>
  <td>US20 - Gerar autenticação (tokens) para API</td>
  <td>21pt</td>
</tr>
<tr>
  <td>US21 - Gerar relatórios de alocação por departamento API</td>
  <td>5pt</td>
</tr>
<tr>
  <td>US22 - Gerar relatórios de alocação por disciplina API</td>
  <td>5pt</td>
</tr>
<tr>
  <td>US23 -  Gerar relatórios de alocação por prédio API</td>
  <td>5pt</td>
</tr>
<tr>
  <td>US24 -  Gerar relatórios de alocação por sala API</td>
  <td>5pt</td>
</tr>
<tr>
<td colspan="3" align="right"><b>Total:</b></td>
<td>143</td>
</tr>

</table>

## Technical Stories

<table>
<tr>
<th>Features</th>
<th>User Stóries</th>
<th>Especificação</th>
<th>Pontos</th>
</tr>
<tr>
  <td rowspan="7">FE06 - Pendências Técnicas Release 1</td>
  <td>TS01 - Fazer Testes de Aceitação</td>
  <td>Eu, como desenvolvedor, desejo concluir os testes de aceitação, para garantir a qualidade do código.</td>
  <td>5pt</td>
</tr>
<tr>
  <td>TS02 - Fazer Testes Unitários</td>
  <td>Eu, como desenvolvedor, desejo concluir os testes unitários, para garantir a qualidade do código.</td>
  <td>8pt</td>
</tr>
<tr>
  <td>TS03 - Refatorar Docs</td>
  <td>Eu, como desenvolvedor, desejo corrigir os documentos, para manter a visão alinhada do projeto.</td>
  <td>2pt</td>
</tr>
<tr>
  <td>TS04 - Refatorar Folha de Estilo</td>
  <td>Eu, como desenvolvedor, desejo adequar o projeto à folha de estilo, para manter a padronização do código.</td>
  <td>13pt</td>
</tr>
<tr>
  <td>TS05 - Refatorar "Smells"</td>
  <td>Eu, como desenvolvedor, desejo corrigir as smells do código, para manter a padronização do código. </td>
  <td>13pt</td>
</tr>
<tr>
  <td>TS06 - Refatorar duplicações de código das controllers</td>
  <td>Eu, como desenvolvedor, desejo reduzir as duplicações de código das controllers, para garantir a qualidade do código.</td>
  <td>3pt</td>
</tr>
<tr>
  <td>TS07 - Refatorar duplicações de código das models/helpers</td>
  <td>Eu, como desenvolvedor,    desejo reduzir as duplicações de código das models/helpers, para garantir a qualidade do código.</td>
  <td>3pt</td>
</tr>
<tr>
<td colspan="3" align="right"><b>Total:</b></td>
<td>47</td>
</tr>


</table>

As _Technical_ _Stories_ foram pontuadas com a finalidade de planejamento, tendo em vista que ao planejar as _sprints_ levamos em consideração o _velocity_ da equipe.

Com esses dados temos <b>143 pontos</b> que agregam valor ao cliente e <b>190 pontos</b> planejados para serem implementados na Release
