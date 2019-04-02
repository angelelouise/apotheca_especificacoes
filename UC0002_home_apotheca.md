# Especificação de Caso de Uso: Home

## 1. Descrição do Caso de Uso
Essa funcionalidade é a principal do aplicativo, é responsável por exibir todas as postagens das turmas do usuário.

## 2.Pré-condições
O aluno deve estar logado no aplicativo.

## 3.Pós-condições
Não se apica.

## 4. Fluxo de eventos
### 4.1 Fluxo Principal
#### FP
**Listar postagem**

1. O usuário aciona a funcionalidade de home;
1. Consulta todas as postagens de todas as turmas de todos os vínculos de graduação do bolsista; **[[FA01](#fa01)]**
1. Exibe o perfil do usuário; **[[BD01](#bd01)]**
1. Exibe as postagens ordenadas por turma com um limite máximo de 10 por consulta; **[[BD02](#bd02)]**, **[[FA02](#fa02)]**, **[[FA01](#fa01)]**
1. O caso de uso é encerrado.

### 4.2 Fluxo Alternativo

#### FA01
**Sem nenhuma postagem**

1. Caso a consulta não retorne nenhum objeto, exibe a tela **[[BD04](#bd04)]**;
1. Retorna para o passo 3 do fluxo principal.

#### FA02
**Detalhar postagem**

1. O usuário toca em uma das postagens da lista;
1. Redireciona para a funcionalidade UC004_detalharPostagem_apotheca;
1. Retorna para o passo 5 do fluxo principal.

#### FA03
**Criar postagem**

1. O usuário toca na opção de cadastrar nova postagem;
1. Redireciona para a funcionalidade UC003_criarPostagem_apotheca;
1. Retorna para o passo 5 do fluxo principal.

#### FA04
**Editar postagem**

1. O usuário toca no menu de opções em uma das postagens da lista;
1. Exibe as opções de ações para a postagem indicada; **[[BD03](#bd03)]**, **[[RN01](#rn01)]**
1. O usuário toca na opção de editar postagem;
1. Redireciona para o **[[FA01](#fa01)]** da funcionalidade UC003_criarPostagem_apotheca;
1. Retorna para o passo 5 do fluxo principal.

#### FA05
**Excluir postagem**

1. O usuário toca no menu de opções em uma das postagens da lista;
1. Exibe as opções de ações para a postagem indicada; **[[BD03](#bd03)]**, **[[RN01](#rn01)]**
1. O usuário toca na opção de excluir postagem;
1. Remove a postagem da base de dados;
1. Retorna para o passo 5 do fluxo principal.

### 4.3 Fluxo de Exceções

Não se aplica.

## 5.Bloco de dados
### BD01
**Perfil**

| Campo                        | Tipo         | Obrigatório | Entrada/Saída | Observações                                                            |
|------------------------------|--------------|-------------|---------------|------------------------------------------------------------------------|
| Foto do perfil               | Imagem       | Sim         | S             |                                                                  |
| Nome do usuário              | Alphanuméric | Sim         | S             |                                                                    |

### BD02
**Lista de postagem**

| Campo                        | Tipo         | Obrigatório | Entrada/Saída | Observações                                                            |
|------------------------------|--------------|-------------|---------------|------------------------------------------------------------------------|
| Título                       | Imagem       | Sim         | S             |                                                                        |
| Foto do perfil               | Alphanumérico| Sim         | S             |                                                          |
| Turma                        | Alphanumérico| Sim         | S             |                                                          |
| Tags                         | Alphanumérico| Sim         | S             |                                                          |
| Timeframe                    | Alphanumérico| Sim         | S             |                                                          |
| Menu                         | Imagem       | Sim         | E             | **[[BD03](#bd03)]**, **[[RN01](#rn01)]**                 |

### BD03
**Opções**

| Campo                        | Tipo         | Obrigatório | Entrada/Saída | Observações                                                            |
|------------------------------|--------------|-------------|---------------|------------------------------------------------------------------------|
| Editar                       | Hiperlink    | Sim         | E             |                                                          |
| Excluir                      | Hiperlink    | Sim         | E             |                                                          |

### BD04
**Nenhum resultado**

| Campo                        | Tipo         | Obrigatório | Entrada/Saída | Observações                                                            |
|------------------------------|--------------|-------------|---------------|------------------------------------------------------------------------|
| Não encontramos postagens    | Alphanumérico| Sim         | S             |                                                                        |

## 6. Requisitos Legais
Não se aplica.

## 7. Regras de Negócio

#### RN01
- Só deve ser possível alterar/excluir postagens do próprio usuário logado.

## 8. Documentos Relacionados
Não se aplica.
