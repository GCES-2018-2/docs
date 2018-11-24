# Caso de teste TC01 - Alterar, Visualizar e Excluir Usuário

## Histórico de Revisão
Data       | Responsável          |Versão   | Mudança realizada                                  |  
|------------|----------------------|---|--------------------------------------------------- |
|30/03/2017| Wallacy  Braz | 0.1 | TC01-1 Formulário de cadastro correto adicionado|
|30/03/2017| Wallacy Braz | 0.2 | TC01-2 Campos inválidos|
|30/03/2017| Wallacy Braz | 0.3 | TC01-3 Alteração correta nos dados |
|30/03/2017| Wallacy Braz | 0.3 | TC01-4 Entrada inválida de dados - alteração |
|30/03/2017| Wallacy Braz | 0.4 | TC01-5 Visualização de dados |
|30/03/2017| Wallacy Braz | 0.5 | TC01-6 Exclusão de cadastro |
|01/04/2017| Wallacy Braz | 1.0 | Refatoração |
|16/04/2017| Iasmin Mendes | 1.1 | Revisão |



## TC01-1 : Alteração de Usuário com dados válidos

### Descrição

Testa condição no qual o usuário tenta fazer alteração de seus dados e preenche o formulário com dados válidos.

### Pré-condições

Usuário se encontra na página de alteração de cadastro.

### Inputs do Teste

Usuário altera os campos nome, e-mail, senha e confirmar senha de forma correta, e confima o alteração.

### Resultados esperados

Uma mensagem de alteração bem sucedida é mostrada ao usuário além de redireciona-lo à página inicial do sistema.

### Pós-condições

O usuário é redirecionado para a página inicial do sistema.


## TC01-2 : Usuário digita dados inválidos na alteração de cadastro

### Descrição

Testa condição na qual o usuário tenta alterar seus dados fornecendo uma entrada inválida, nula, ou redundante.

### Pré-condições

Usuário se encontra na página de alteração de cadastro.

### Inputs do Teste

O usuário insere nenhum ou deixa pelo menos um campo em branco, ou insere dados inválidos ou tenta inserir um dado que já existe em seu cadastro, confimando as alterações no final.

### Resultados esperados

Uma notificação adjacente ao campo inválido ou nulo ou redundante é mostrada ao usuário, fornecendo detalhes da invalidez e como corrigi-la.

### Pós-condições

O usuário permanece na página de alteração de cadastro. Os campos inválidos estão com as notificações e os campos válidos permanecem preenchidos.


## TC01-3 : Usuário visualiza seus dados

### Descrição

Testa condição na qual o usuário tenta visualizar seus dados.

### Pré-condições

Usuário está na página inicial do sistema.

### Inputs do Teste

Usuário seleciona opção "Minha Conta" na página inicial.

### Resultados esperados

Usuário é redirecionado para uma página com a relação dos seus dados cadastrados no sistema.

### Pós-condições

O usuário permanece na página para realizar outras ações.

## TC01-4 : Usuário exclui cadastro

### Descrição

Testa condição na qual usuário tenta excluir seu cadastro.

### Pré-condições

Usuário se encontra na página com suas informações pessoais.

### Inputs do Teste

Usuário seleciona a opção de excluir seu cadastro do sistema, e confirma exclusão.

### Resultados esperados

Uma mensagem de confirmação de exclusão é mostrada ao usuário.

### Pós-condições

O usuário é redirecionado para a página de login do sistema.
