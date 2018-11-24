# SIGS

| Data       | Responsável          | Versão   | Mudança realizada                                 |
| ---------- | -------------------- |:--------:| ------------------------------------------------- |
|**18/04/17**| Rodrigo Dadamos  | 1.0  | Versão inicial do documento |
|**18/04/17**| Rodrigo Dadamos  | 1.1  | RCT4.1 |
|**18/04/17**| Rodrigo Dadamos  | 1.2  | RCT4.2 |
|**18/04/17**| Rodrigo Dadamos  | 1.3  | RCT4.3 |

## Caso de Teste: Aprovar Cadastro

**RCT4.1** - Administrador aprova o cadastro de um usuário comum.

**RCT4.2** - Administrador recusa cadastro de usuário.

**RCT4.3** - Nenhuma solicitação pendente.

|Relatório do Caso de Teste   | Entrada |  Resultados esperados | Resultados obtidos  |Status   |
|:---------------------------:|---------|-----------------------|---------------------|:-------:|
| RCT4.1 | O administrador clica na opção “Usuários” , em seguida clica em “Cadastros Pendentes”, identifica os cadastros solicitados e clica em “Aprovar Cadastro”. | O administrador recebe uma mensagem informando que o cadastro do usuário foi aprovado com sucesso e o usuário agora pode acessar o sistema. | O resultado é alcançado com sucesso. O administrador recebe uma mensagem de sucesso e o usuário pode acessar o sistema. | OK. |
| RCT4.2 | O administrador clica na opção “Usuários” , em seguida clica em “Cadastros Pendentes”, identifica os cadastros solicitados e clica em “Recusar Cadastro”. | O administrador recebe uma mensagem informando que o cadastro do usuário foi recusado com sucesso e o usuário é deletado do sistema. | O resultado é alcançado com sucesso. O administrador recebe uma mensagem de sucesso e o usuário é deletado do sistema. | OK. |
| RCT4.3 | O administrador clica na opção “Usuários” , em seguida clica em “Cadastros Pendentes” e identifica que não há nenhum cadastro solicitado. | O administrador recebe uma mensagem do sistema informando que não há solicitações pendentes. | O resultado é alcançado com sucesso. O administrador recebe uma mensagem do sistema informando que não há solicitações pendentes. | OK. |
