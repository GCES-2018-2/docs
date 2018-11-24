# UC03 - Solicitar Cadastro

### Histórico da Revisão

|    Data    | Versão |                    Descrição                    |              Autor             |
|:----------:|:------:|:-----------------------------------------------:|:------------------------------:|
| 01/04/2017 | 1.0    | Descrição, Atores, Pré-Condição e Pós-Condição. | Carlos Aragon                 |
| 09/04/2017 | 1.1    | Correção dos atores, fluxo principal, fluxos alternativos, mensagens e regra de negócio. | Daniel Marques                 |
| 15/04/2017 | 1.2    | Revisão.                                         | Carlos Aragon                 |

## Descrição:
Realizar a solicitação do cadastro de um usuário no sistema.

## Atores:
* Usuário não cadastrado.

## Precondição:
Não há pré condição.

## Pós-Condição:
Após o usuário enviar o formulário de cadastro, é necessário ter a aprovação do usuário Assistente Administrativo para ter o cadastro concluído com êxito.

## Regra de Negócio (Campos e Validação):

|      Campo      |             Formato             | Obrigatoriedade |                     Valor                    |
|:---------------:|:-------------------------------:|:---------------:|:--------------------------------------------:|
| Nome completo   | String (de 7 a 100 caracteres)         | Sim             | Não                                          |
| CPF             | String (exatamente 11 caracteres)          | Sim             | 00000000000                               |
| Email           | String       | Sim             | exemplo@unb.com                             |
| Tipo de Usuário | Caixas de seleção              | Sim             | Coordenador, Auxiliar de Departamento e Assistente Administrativo |
| Matrícula       | String (7 caracteres) | Sim | 000000000 |
| Curso           | Campo de Droplist               | Somente para Coordenador    | Todos os cursos                              |
| Departamento           | Campo de Droplist               |Somente para Auxiliar de Departamento     | Todos os departamentos   |
| Senha           | Password (de 6 a 20 caracteres) | Sim             | Não                                          |
| Confirmar Senha | Password (de 6 a 20 caracteres) | Sim             | Não                                          |


* [RN01] O CPF deve ser único no banco de dados do sistema.
* [RN02] O campo Curso só estará visível para contas do tipo Coordenador.
* [RN03] O campo Departamento só estará visível para contas do tipo Auxiliar do Departamento.
* [RN04] Não pode haver mais de um usuário do tipo Coordenador do mesmo curso.
* [RN05] A Matrícula deve ser única


## Fluxo Principal:

1. O usuário acessa a página de cadastro do sistema.
2. O sistema solicita ao usuário o preenchimento dos campos.
3. O usuário preenche os campos solicitados [RN01] [RN02] [RN03] [RN04] [RN05].
4. O usuário clica em Solicitar Cadastro.
5. O sistema irá validar os campos preenchidos [FA01] [FA02].
6. O sistema irá validar se há duplicidade de CPF ou matrícula no banco dados [RN02] [FA03] [RN05].
7. O sistema irá cadastrar o usuário no banco de dados.
9. O sistema exibe [M0]
10. O caso de uso é encerrado.


## Fluxo Alternativo:
### [FA01] Usuário não preenche algum campo:
1. O sistema irá detectar que os campos não estão preenchidos.
2. O sistema retorna para o passo 2 do fluxo principal com [M1].

### [FA02] Usuário preenche algum campo incorretamente:
1. O sistema irá detectar que os campos foram preenchidos de forma incorretamente.
2. O sistema retorna para o passo 2 do fluxo principal com [M2].

### [FA03] Usuário informa cpf, email ou matrícula já cadastrado:
1. O sistema irá detectar duplicidade de cpf, email ou matrícula no banco de dados do sistema.
2. O sistema retorna para o passo 2 do fluxo principal com [M3].

## Mensagem:
* [Um campo específico, com identificador das mensagens que serão apresentadas pelo sistema]
* [M0] Solicitação de cadastro enviada com sucesso!
* [M1] Os campos <nomes de cada campo> devem ser preenchidos.
* [M2] Os campos <nomes de cada campo> foram preenchidos de forma incorreta.
* [M3] Os campos <nomes de cada campo> já existem
