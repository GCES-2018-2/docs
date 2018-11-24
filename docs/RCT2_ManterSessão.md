# SIGS

## Relatório de Casos de Teste

| Data       | Responsável          | Versão   | Mudança realizada                                 |
| ---------- | -------------------- |:--------:| ------------------------------------------------- |
|**18/04/17**| Bruno Matias Casas  | 1.0  | Versão inicial do documento                         |
|**19/04/17**| Bruno Matias Casas  | 1.1  | Refatoração -  2.1 a 2.4 - Deletado 2.5 a 2.10   |

## Caso de Teste: Manter sessão

RCT2.1 - Criar sessão com um usuário válido

RCT2.2 - Erro ao criar sessão com dados de usuário invalido

RCT2.3 -  Notificação ao logar usuário com conta não ativa

RCT2.4 - Destruir Sessão



|Relatório do Caso de Teste   |Entrada   |  Resultados esperados | Resultados obtidos  |Status   |
|-----------------------------|----------|-----------------------|---------------------|---------|
|RCT2.1   |Acessar a página de login da aplicação.Preencher o text field de "E-mail" com o dado "Wallacy@unb.br".Preencher o password field de "Senha" com o dado "123456" Clicar no botão "Entrar"   |O sistema redireciona para a página inicial com a mensagem "Login realizado com sucesso".   |O sistema redirecionou corretamente para a página inicial, logando o usuário no sistema.   |OK.   |
|RCT2.2   |Acessar a página de login da aplicação.Preencher o text field de "E-mail" com o dado "Wallacy@unb.br". Preencher o password field de "Senha" com “1231234” Clicar no botão "Entrar".   |A página de login é recarregada com a mensagem "E-mail ou senha inválidos".   |A página foi recarregada corretamente com a mensagem de erro.   |OK.   |
|RCT2.3   |Acessar a página de login da aplicação.Preencher o text field de "E-mail" com o dado "joao@unb.br".Preencher o password field de "Senha" com o dado "1234544" Clicar no botão "Entrar"   | A página de login é recarregada com a mensagem "Sua conta não está ativa".  | A página  foi recarregada corretamente com a mensagem de notificação.  |OK.   |
|RCT2.4   |Se logar no sistema.Já na tela inicial clicar no link de “logout”   |O sistema redireciona para a página inicial com a mensagem "Usuário deslogado com sucesso".   |O sistema redirecionou corretamente para a página inicial, deslogando o usuário do sistema.   |OK.   |