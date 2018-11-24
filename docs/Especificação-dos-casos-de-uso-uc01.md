# UC01 - Gerenciar Usuário

### Histórico da Revisão

|    Data    | Versão |                    Descrição                    |              Autor             |
|:----------:|:------:|:-----------------------------------------------:|:------------------------------:|
| 27/03/2017 | 0.1    | Descrição, Atores, Pré-Condição e Pós-Condição. | Daniel Marques                 |
| 28/03/2017 | 0.2    | Regras de Negócio.                              | Daniel Marques                 |
| 28/03/2017 | 0.3    | Fluxo Principal.                                | Daniel Marques e Carlos Aragon |
| 29/03/2017 | 0.4    | Fluxo Alternativo e Mensagens                   | Daniel Marques                 |
| 30/03/2017 | 1.0    | Revisão                                         | Ateldy Brasil                  |
| 01/04/2017 | 1.1    | Fluxo principal cadastro                        | Carlos Aragon                  |
| 01/04/2017 | 1.2    | Alteração das funcionalidades do caso de uso    | Carlos Aragon                  |
| 08/04/2017 | 1.3    | Refatoração do documento                        | Daniel Marques                 |
| 15/04/2017 | 1.4    | Revisão                                         | Carlos Aragon                  |
| 19/04/2017 | 1.5    | Atualização da funcionalidade Exclusão e Regra de Negócio                                         | Daniel Marques                  |
| 29/04/2017 | 1.6    | Revisão | Rodrigo Dadamos e Vinícius Carvalho |

## Descrição:
Realizar as funções de gerenciamento de conta do usuário sendo elas: alteração dos dados, visualização dos dados e  exclusão da conta.

**Alteração:** o usuário pode alterar os dados da sua conta.

**Visualização:** o usuário pode visualizar os dados da sua conta.

**Exclusão:**  o usuário pode excluir sua conta do sistema.

## Atores:
* Coordenador.
* Auxiliar de Departamento
* Assistente Administrativo


## Pre-condição:
Para realizar as operações de gerenciamento de conta é necessário estar cadastrado no banco de dados do sistema.

## Pós-Condição:

**Alteração:** Abrir a página inicial do sistema.

**Exclusão:** Abrir página inicial do sistema.

### Alteração:

|      Campo      |             Formato             | Obrigatoriedade |
|:---------------:|:-------------------------------:|:---------------:|
| Nome completo   | String (de 7 a 100 caracteres)  | Sim             |
| Senha           | Password (de 6 a 20 caracteres) | Sim             |
| Confirmar Senha | Password (de 6 a 20 caracteres) | Sim             |

* [RN01] O campo Nome Completo deve ter somente letras.

### Exclusão:

* [RN02] O Assistente Administrativo só poderá excluir sua conta se houver pelo menos mais um Assistente Administrativo cadastrado no sistema.

## Fluxo Principal:

### Alteração:
1. O usuário acessa o sistema.
2. O usuário clica em "Minha Conta".
3. O sistema solicita ao usuário o preenchimento dos campos.
4. O usuário altera os dados [RN01].
5. O usuário clica em "Salvar".
6. O sistema irá validar os campos do formulário [FA01] [FA02].
7. O sistema salva as alterações no usuário.
8. O sistema redireciona o usuário para a página de usuário.
9. O caso de uso é encerrado.

### Visualização:
1. O usuário acessa o sistema.
2. O usuário clica em "Minha Conta".
3. O usuário visualiza seus dados.
4. O caso de uso é encerrado.


### Exclusão:
1. O usuário acessa o sistema.
2. O usuário clica em "Minha Conta".
3. O usuário clica em "Excluir Conta".
4. O sistema mostra uma mensagem de confirmação [M2].
5. O usuário clica em Confirmar.
6. O sistema irá validar a [RN02] [FA01].
7. O sistema exclui o usuário.
8. O sistema retorna para a página inicial com [M4].
9. O caso de uso é encerrado.

## Fluxo Alternativo:

### Alteração:
#### [FA01] Usuário não preenche algum campo:
1. O sistema irá detectar que os campos não estão preenchidos.
2. O sistema retorna para o passo 2 do fluxo principal com [M1].

#### [FA02] Usuário preenche algum campo incorretamente:
1. O sistema irá detectar que os campos foram preenchidos de forma incorretamente.
2. O sistema retorna para o passo 2 do fluxo principal com [M1].

### Exclusão:
#### [FA01] O Assistente Administrativo tenta excluir a si mesmo, sendo a única conta do tipo Assistente Administrativo:
1. O sistema detecta que há somente uma conta do tipo Assistente Administrativo no banco de dados.
2. O sistema retorna para o passo 2 do fluxo principal com [M3].

## Mensagem:
* [Um campo específico, com identificador das mensagens que serão apresentadas pelo sistema]
* [M1] Os campos <nomes de cada campo> foram preenchidos de forma incorreta.
* [M2] Tem Certeza que Deseja Excluir ?
* [M3] Não é possível excluir o único Assistente Administrativo.
* [M4] Usuário excluido com sucesso.
