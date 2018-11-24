# UC02 - Manter Sessão

### Histórico da Revisão

|    Data    | Versão |                  Descrição                 |      Autor      |
|:----------:|:------:|:------------------------------------------:|:---------------:|
| 27/03/2017 | 0.1    | Documento inicial                          | Rodrigo Dadamos |
| 27/03/2017 | 0.2    | Fluxo de Eventos                           | Rodrigo Dadamos |
| 27/03/2017 | 0.3    | Requisitos Especiais e Condições Prévias   | Rodrigo Dadamos |
| 27/03/2017 | 0.4    | Condições Posteriores e Pontos de Extensão | Rodrigo Dadamos |
| 30/03/2017 | 1.0    | Revisão                                    | Ateldy Brasil   |
| 08/04/2017 | 1.1    | Revisão                                    | Rodrigo Dadamos |
| 08/04/2017 | 1.2    | Revisão Markdown                           | Rodrigo Dadamos |
| 14/04/2017 | 1.3    | Desmembramento dos Fluxos                  | Rodrigo Dadamos |
| 16/04/2017 | 1.4    | Fluxos de Exceção                          | Iasmin Mendes |

## Descrição:
<p align='justify'>Essa especificação de caso de uso trata sobre a ação de logar em uma sessão no sistema. Para utilizar o sistema os usuários deverão efetuar o login no mesmo, ou seja, os usuários devem se identificar com o seu nome de usuário e senha previamente cadastrados. Dessa forma o sistema valida a autenticação do usuário.</p>

<p align='justify'>Os usuários, previamente cadastrados, devem acessar o sistema pelo endereço eletrônico (url) em um navegador de um computador com acesso à internet. Então os usuários devem identificar a área de login no sistema e preencher os campos nome de usuário e senha corretamente para que possam logar no sistema. Após ocorrer a verificação pelo sistema dos dados informados pelo usuário e, estando correta as informações, o usuário é logado no sistema sendo encaminhado para a tela principal do mesmo onde uma mensagem de boas-vindas é exibida. É possível também acessar a área restrita de visualização de salas.</p>

## Atores:

* Coordenador
* Auxiliar do Departamento
* Assistente Administrativo


## Pré-condição:
Acessar o sistema por um navegador web de um computador com acesso a internet. Para se logar o usuário deverá estar cadastrado no sistema.

## Pós-Condição:
O sistema define o estado do usuário como logado e o redireciona para a tela principal do sistema emitindo uma mensagem de boas-vindas.

## Regra de Negócio (Campos e Validação):

|     Campo     |             Formato             | Obrigatoriedade | Valor |
|:-------------:|:-------------------------------:|:---------------:|:-----:|
| E-mail | String (de 3 a 50 caracteres)         | Sim             | Não   |
| Senha         | Password (de 6 a 20 caracteres) | Sim             | Não   |


## Fluxo Principal:

1. O usuário acessa o sistema.
2. O usuário identifica a área de login [FA01].
3. O usuário preenche os campos Nome de Usuário e Senha corretamente [FE01] [FE03].
4. O usuário clica em Logar.
5. O sistema verifica se os dados informados correspondem aos cadastrados no sistema, e se o usuário consta como ativo. [FE02]
6. O sistema encaminha o usuário logado para a tela principal.
8. O caso de uso é encerrado.

## Fluxo de Exceção

### [FE01] Usuário informa Nome e/ou Senha incorreta(s)
1. O usuário preenche os campos Nome de Usuário e/ou Senha incorretamente.
2. O usuário clica em Logar.
3. O sistema não efetua o login mantendo o usuário na mesma tela.
4. O sistema emite [M1].

### [FE02] Usuário informa Nome e Senha corretos mas está inativo no sistema
1. O sistema verifica que o usuários está inativo no sitema.
1. O sistema não efetua o login mantendo o usuário na mesma tela.
3. O sistema emite [M4].

### [FE03] Usuário não preenche Nome e/ou Senha
1. O usuário não preenche os campos Nome de Usuário e/ou Senha.
2. O usuário clica em Logar.
3. O sistema não efetua o login mantendo o usuário na mesma tela.
4. O sistema emite [M2].

## Mensagem:
* [Um campo específico, com identificador das mensagens que serão apresentadas pelo sistema]
* [M1] Usuário e/ou senha desconhecido(s).
* [M2] Por favor, preencha os campos Nome de Usuário e Senha corretamente.
* [M3] Usuário não cadastrado.
* [M4] Acesso negado. Seu cadastro ainda não foi confirmado.
