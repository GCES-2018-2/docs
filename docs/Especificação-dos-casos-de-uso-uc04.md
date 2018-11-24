# UC04 - Aprovar cadastro

### Histórico da Revisão

|    Data    | Versão |                    Descrição                    |              Autor             |
|:----------:|:------:|:-----------------------------------------------:|:------------------------------:|
| 01/04/2017 | 1.0    | Revisão | Carlos Aragon                 |
| 09/04/2017 | 1.1    | Correção dos atores, fluxo principal, fluxos alternativos, mensagens e regra de negócio | Daniel Marques                 |
| 15/04/2017 | 1.2    | Revisão | Carlos Aragon                 |

## Descrição:
Aprovar solicitações de cadastro no sistema.

## Atores:
* Assistente Administrativo.

## Precondição:
* A funcionalidade Solicitar Cadastro deve ter sido executado antes por algum visitante ao site.
* O usuário do tipo Assistente Administrativo deve estar logado no sistema.

## Pós-Condição:
O usuário solicitante que possuir seu cadastro aprovado pelo usuário Administrador, passa a possuir acesso ao sistema de acordo com os privilégios associados pelo seu tipo de usuário definido no momento da aprovação.

## Fluxo Principal:
1. O usuário do tipo Assistente Administrativo acessa a página de cadastro pendentes [FA01] .
2. O sistema mostra as solicitações pendentes.
3. O usuário do tipo Assistente Administrativo clica em Aprovar [M1] [FA02].
4. O sistema libera as funcionalidades para o usuário com o cadastro aprovado.
5. Caso de uso encerrado.

## Fluxo Alternativo:
### [FA01] Não há nenhuma solicitação pendente:
1. O sistema mostra uma mensagem dizendo que não há nenhuma solicitação pendente.
2. O sistema vai para o passo 5 do fluxo principal.

### [FA02] O usuário clica em Recusar:
2. O sistema notifica o usuário da solicitação que houve a recusa de seu cadastro [M2].
3. O sistema vai para o passo 9 do fluxo principal.

## Mensagem:
* [Um campo específico, com identificador das mensagens que serão apresentadas pelo sistema]
* [M1] A solicitação foi aprovada com sucesso.
* [M2] A solicitação foi recusada.
