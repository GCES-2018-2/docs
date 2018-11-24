

# SIGS

Relatório de Casos de Teste

| Data | Versão | Descrição | Autor |
| --- | --- | --- | --- |
| 18/04/2017 | 1.0 | Versão inicial do documento | Wallacy Braz |
| 27/04/2017 | 1.1 | Revisão e especificação das entradas | Rodrigo Dadamos e Vinícius Carvalho |



## Caso de teste:  Gerenciar Usuário


**Precondição:**  **O usuário com cadastro válido e com sessão devidamente ativa, seja ele assistente administrativo, coordenador ou auxiliar de departamento.**

**RCT1.1**  **-  O usuário tenta visualizar seus dados.**

**RCT1.2**  **- O usuário tenta editar seus dados.**

**RCT1.3 - O usuário tenta editar seus dados com dados inválidos.**

**RCT1.4 - O usuário tenta excluir seu cadastro.**



| Relatório do Caso de Teste | Entrada | Resultados esperados | Resultados obtidos | Status |
| --- | --- | --- | --- | --- |
| RCT1.1 | O usuário clica em "Minha Conta". | O sistema direciona para a página com dados do usuário exibidos para visualização. | O usuário teve seus dados foi direcionado para a página de visualização de seus dados. | ok |
| RCT1.2 | O usuário clica em "Minha Conta" e depois entra com os dados que deseja editar: <br>Nome: Paula da Silva<br> Senha: 123456<br> Confirmar Senha: 123456<br> e por ultimo clica em “Salvar”. | O usuário é notificado de que a atualização dos dados foi bem sucedida e é redirecionado para sua página de visualização | Os dados foram validados com sucesso e o foi obtida a notificação e o redirecionamento completo. | ok |
| RCT1.3 | O usuário clica em "Minha Conta" e depois entra com os dados que deseja editar: <br>Nome: Paula<br> Senha: 123<br> Confirmar Senha: 321<br> e por ultimo clica em “Salvar”. | O usuário recebe uma lista de mensagens informando os erros de cada campo e os dados não devem ser alterados. | Os dados não foram atualizados e o usuário recebe uma lista de mensagens com os  erros de cada campo e continua na mesma página. | ok |
| RCT1.4 | O usuário clica em "Minha Conta" e depois clica em "Excluir Conta" e depois clica em "Confirmar". | A conta do usuário deve ser excluída, o usuário deve ser notificado e redirecionado para a página de log\_in. | A conta do usuário foi excluída, o usuário foi notificado e redirecionado para a página de log\_in. | ok |
