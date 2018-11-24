# Caso de teste TC02 - Manter sessão

## Histórico de Revisão
Data       | Responsável          |Versão   | Mudança realizada                                  |  
|------------|----------------------|---|--------------------------------------------------- |
|30/03/2017| Bruno Matias Casas | 0.1 | TC02-1 Formulário de login correto |
|30/03/2017| Bruno Matias Casas | 0.2 | TC02-2 Formulário possui campos incorretos |
|30/03/2017| Bruno Matias Casas | 0.3 | TC02-3 Cadastro ainda não validado |
|30/03/2017| Bruno Matias Casas | 0.4 | TC02-4 Usuário desloga do sistema |
|01/04/2017| Wallacy Braz | 1.0 | Refatoração |
|16/04/2017| Iasmin Mendes | 1.1 | Revisão |


## TC02-1 : Formulário de login correto

### Descrição

Testa condição na qual o usuário insere dados válidos na página de login.

### Pré-condições

O usuário deve estar na página de login e com o cadastro validado pelo administrador.

### Inputs do teste

O usuário entra com e-mail e senha, logo em seguida clica em entrar.

### Resultados esperados

É mostrado uma mensagem ao usuário dizendo que ele foi logado com sucesso.

### Pós-condições

O usuário é redirecionado para a página inicial do sistema.


## TC02-2 : Formulário possui campos incorretos

### Descrição

Testa a condição na qual o usuário insere dados incorretos durante o preenchimento do formulário.

### Pré-condições

O usuário deve estar na página de login e com o cadastro validado pelo administrador.

### Inputs do teste

O usuário entra ou com e-mail ou senha incorretos, logo em seguida clica em entrar.

### Resultados esperados

É mostrado uma mensagem ao usuário informando que os dados inseridos estão incorretos.

### Pós-condições

O usuário permanece na página de login.


## TC02-3 : Cadastro ainda não aprovado

### Descrição

Testa a condição na qual o usuário insere dados de login referentes à um usuário que já solicitou cadastro mas ainda não obteve confirmação do administrador.

### Pré-condições

O usuário deve estar na página de login.

### Inputs do teste

O usuário entra com e-mail e senha de acordo com seu cadastro parcial, logo em seguida clica em entrar.

### Resultados esperados

É mostrado uma mensagem ao usuário dizendo que sua solicitação de cadastro ainda está em avaliação.

### Pós-condições

O usuário permanece na página de login.


## TC02-4 : Usuário desloga do sistema

### Descrição

Testa a condição na qual o usuário desloga do sistema.

### Pré-condições

O usuário deve estar logado, independente da página que esteja no sistema.

### Inputs do teste

O usuário clica em Logout.

### Resultados esperados

É mostrado uma mensagem ao usuário dizendo que ele foi deslogado com sucesso.

### Pós-condições

O usuário é redirecionado para a página de login.
