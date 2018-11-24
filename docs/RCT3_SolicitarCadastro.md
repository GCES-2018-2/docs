# SIGS

| Data       | Responsável          | Versão   | Mudança realizada                                 |
| ---------- | -------------------- |:--------:| ------------------------------------------------- |
|**19/04/17**| Daniel Marques  | 1.0  | Versão inicial do documento                         |

## Caso de Teste: Solicitar Cadastro

**RCT3.1** - O usuário visitante tenta solicitar cadastro com os todos os campos vazio.

**RCT3.2** - O usuário visitante tenta solicitar cadastro com algum dado incorreto.

**RCT3.3** - O usuário visitante tenta solicitar cadastro com todos os dados corretos.

**RCT3.4** - O usuário visitante tenta solicitar cadastro com todos os dados corretos, porém já existe um usuário cadastrado com esses dados

|Relatório do Caso de Teste   | Entrada |  Resultados esperados | Resultados obtidos  |Status   |
|:---------------------------:|---------|-----------------------|---------------------|:-------:|
| RCT3.1 | O usuário clica em “Solicitar Cadastro” e em seguida sem preencher nenhum campo ele clica  em “Enviar”.  | O usuário recebe uma mensagem informando que os campos não foram preenchidos corretamente e quais são as exigências de cada campo. | O usuário não consegue solicitar um cadastro no sistema. | OK. |
| RCT3.2 | O usuário clica em “Solicitar Cadastro”, em seguida preenche os campos com os seguintes dados:<br>Nome: Paula<br> E-mail: daniel<br> CPF: 123<br> Registro UnB: 1234<br> Senha: 123<br> Confirmar Senha: 321<br> e por ultimo clica em “Enviar”. | O usuário recebe uma lista de mensagens informando os erros de cada campo. | O usuário não consegue solicitar um cadastro no sistema. | OK. |
| RCT3.3 | O usuário clica em “Entrar” e em seguida em “Cadastrar” e preenche cada campo com os seguintes dados:<br> Nome: João Silva<br> E-mail: joaosilva@unb.br<br> CPF: 05601407380<br> Registro UnB: 11006101<br> Senha: 123456<br> Confirmar Senha: 123456<br> e por último clica em “Enviar”. | O usuário recebe uma mensagem informando que a solicitação foi enviada com sucesso. | O usuário consegue se cadastrar no sistema. | OK. |
| RCT3.4 | O usuário clica em “Entrar” e em seguida em “Cadastrar” e preenche cada campo com os seguintes dados:<br> Nome: João Silva<br> E-mail: joaosilva@unb.br<br> CPF: 05601407380<br> Registro UnB: 11006101<br> Senha: 123456<br> Confirmar Senha: 123456<br> e por último clica em “Enviar”. | O usuário recebe uma mensagem informando que os dados já estão registrados no sistema. | O usuário não consegue solicitar um cadastro no sistema. | OK. |
