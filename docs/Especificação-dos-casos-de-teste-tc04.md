# Caso de Teste TC04 - Aprovar Cadastro

## Histórico de Revisão
Data       | Responsável          |Versão   | Mudança realizada                                  |  
|------------|----------------------|---|--------------------------------------------------- |
| 01/04/2017 | Daniel Marques | 0.1 | TC04-1 Administrador aceita cadastro de usuário |
| 01/04/2017 | Daniel Marques | 0.2 | TC04-2 Administrador recusa cadastro de usuário |
| 01/04/2017 | Daniel Marques | 1.0 | TC04-3 Nenhuma solicitação pendente |
| 16/04/2017 | Iasmin Mendes | 1.1 | Revisão |

## TC04-1 : Administrador aprova o cadastro de um usuário comum

### Descrição

Testa condição na qual Assistente Administrativo aceita solicitação de cadastro de um usuário comum.

### Pré-condições

O Assistente Administrativo deve estar logado no sistema,estar na página Gerenciar Usuários na aba Solicitações Pendentes, além de estar com uma solicitação pendente aberta.

### Inputs do teste

Administrador clica em aceitar solicitação.


### Resultados esperados

O Assistente Administrativo recebe uma mensagem o notificando de que a solicitação foi aceita com sucesso.

### Pós-condições

O Assistente Administrativo é redirecionado para a página de Solicitações Pendentes

## TC04-2 : Administrador recusa cadastro de usuário

### Descrição

Testa condição na qual o  Assistente Administrativo recusa a solicitação de cadastro do usuário.

### Pré-condições

O Assistente Administrativo deve estar logado no sistema, estar na página Gerenciar Usuários na aba Solicitações Pendentes, além de estar com uma solicitação pendente aberta.

### Inputs do teste

O Assistente Administrativo clica em Recusar e logo em seguida escreve a justificativa de recusa para ser enviada ao usuário que solicitou o cadastro.

### Resultados esperados

O usuário que solicitou o cadastro é notificado que a solicitação foi recusada junto com uma mensagem com a justificativa da recusa.

### Pós-condições

O Assistente Administrativo está na página de solicitações pendentes.

## TC04-3 : Nenhuma solicitação pendente

### Descrição

Testa condição na qual o sistema não apresenta solicitações de cadastro no banco.

### Pré-condições

O Assistente Administrativo deve estar logado no sistema e estar na página Gerenciar Usuários.

### Inputs do teste

O Assistente Administrativo deve selecionar a opção gerenciar usuários com solicitações cadastrais pendentes.

### Resultados esperados

O Assistente Administrativo recebe uma mensagem o notificando de que não há cadastros pendentes.


### Pós-condições

O Assistente Administrativo permanece na página de gerenciamento de usuários.
