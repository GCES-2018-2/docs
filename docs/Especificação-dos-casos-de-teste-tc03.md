# Caso de Teste TC03 - Solicitar Cadastro

## Histórico de Revisão

Data       | Responsável          |Versão   | Mudança realizada                                  |  
|------------|----------------------|---|--------------------------------------------------- |
| 01/04/2017 | Daniel Marques | 0.1 | TC03-1 Formulário de cadastro correto |
| 01/04/2017 | Daniel Marques | 0.2 | TC03-2 Formulário possui campos inválidos ou vazios |
| 01/04/2017 | Daniel Marques | 1.0 | TC03-3 Formulário possui campos chaves redundantes |
| 16/04/2017 | Iasmin Mendes | 1.1 |  Atualização dos Inputs e Revisão |

## TC03-1 : Formulário de cadastro correto

### Descrição

Testa a condição na qual o usuário insere dados válidos durante o processo de cadastro

### Pré-condições

O usuário deve estar na página de cadastro.

### Inputs do teste

O usuário entra com nome completo, CPF, e-mail, registro UnB, tipo de conta, senha, confirmar senha e, se necessário, curso e departamento. Logo em seguida clica em confirmar cadastro.

### Resultados esperados

É mostrada uma mensagem ao usuário dizendo que ele deve aguardar a confirmação do seu cadastro pelo administrador do sistema.

### Pós-condições

O usuário é redirecionado para a página de logon do sistema.


## TC03-2 : Formulário possui campos inválidos ou vazios.

### Descrição

Testa a condição na qual o usuário insere dados inválidos ou deixa campo vazios.

### Pré-condições

O usuário deve estar na página de cadastro.

### Inputs do Teste

O usuário deixa de preencher pelo menos um campo obrigatório dentre eles o nome completo, CPF, e-mail, registro, tipo de conta, curso, senha, confirmar senha ou preenche os mesmos dados de forma inválida e logo em seguida submete o formulário.

### Resultados esperados

O sistema exibe uma mensagem notificando ao usuário de qual campo ele preencheu incorreto ou deixou vazio.

### Pós-condições

O usuário permanece na página de preenchimento do formulário de cadastro.

## TC03-3 : Formulário possui campos chaves redundantes

### Descrição

Testa condição na qual usuário tenta enviar o formulário de cadastro com um CPF, registro, ou email já cadastrado no banco de dados.

### Pré-condições

O usuário deve estar na página de cadastro.

###  Inputs do teste

O usuário preenche todos os campos obrigatórios dentre eles o nome completo, CPF, e-mail, tipo de conta, curso, senha e confirmar senha de forma válida, mas com algum dado - CPF, Registro ou e-mail - já cadastrado no sistema.

### Resultados esperados

O usuário recebe uma notificação o alertando o dado informado já consta no banco de dados.

### Pós condições

O usuário permanece na página de cadastro.
