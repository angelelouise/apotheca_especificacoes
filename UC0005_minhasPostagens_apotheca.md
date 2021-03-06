# Especificação de Caso de Uso: Minhas Postagens

## 1. Descrição do Caso de Uso
Essa funcionalidade é responsável por exibir todas as postagens feitas pelo usuário.

## 2.Pré-condições
O aluno deve estar logado no aplicativo.

## 3.Pós-condições
Não se apica.

## 4. Fluxo de eventos
### 4.1 Fluxo Principal
#### FP
**Listar postagem**

1. O usuário aciona a funcionalidade de home;
1. Consulta todas as postagens em que o autor é o usuário; **[[FA01](#fa01)]**
1. Exibe as postagens ordenadas por turma com um limite máximo de 10 por consulta; **[[BD01](#bd01)]**, **[[FA02](#fa02)]**, **[[FA03](#fa03)]**, **[[FA04](#fa04)]**, **[[FA05](#fa05)]**
1. O caso de uso é encerrado.

### 4.2 Fluxo Alternativo

#### FA01
**Sem nenhuma postagem**

1. Caso a consulta não retorne nenhum objeto, exibe a tela **[[BD04](#bd04)]**;
1. Retorna para o passo 4 do fluxo principal.

#### FA02
**Detalhar postagem**

1. O usuário seleciona uma das postagens da lista;
1. Redireciona para a funcionalidade UC004_detalharPostagem_apotheca;
1. Retorna para o passo 4 do fluxo principal.

#### FA03
**Criar postagem**

1. O usuário aciona a opção de cadastrar nova postagem;
1. Redireciona para a funcionalidade UC003_criarPostagem_apotheca;
1. Retorna para o passo 4 do fluxo principal.

#### FA04
**Editar postagem**

1. O usuário aciona o menu de opções em uma das postagens da lista;
1. Exibe as opções de ações para a postagem indicada; **[[BD03](#bd03)]**, **[[RN01](#rn01)]**
1. O usuário aciona a opção de editar postagem;
1. Redireciona para o **[[FA01](#fa01)]** da funcionalidade UC003_criarPostagem_apotheca;
1. Retorna para o passo 4 do fluxo principal.

#### FA05
**Excluir postagem**

1. O usuário aciona o menu de opções em uma das postagens da lista;
1. Exibe as opções de ações para a postagem indicada; **[[BD03](#bd03)]**, **[[RN01](#rn01)]**
1. O usuário aciona a opção de excluir postagem;
1. Remove a postagem da base de dados;
1. Retorna para o passo 4 do fluxo principal.

### 4.3 Fluxo de Exceções

Não se aplica.

## 5.Bloco de dados

### BD01
**Lista de postagem**

| Campo                        | Tipo         | Obrigatório | Entrada/Saída | Observações                                                            |
|------------------------------|--------------|-------------|---------------|------------------------------------------------------------------------|
| Título                       | Alphanumérico| Sim         | S             |                                                                        |
| Foto do perfil               | Imagem       | Sim         | S             |                                                          |
| Turma                        | Alphanumérico| Sim         | S             |                                                          |
| Tags                         | Alphanumérico| Sim         | S             |                                                          |
| Timeframe                    | Alphanumérico| Sim         | S             | Diferença entre a data do cadastro da postagem em relação a data atual.|
| Menu                         | Imagem       | Sim         | E             | **[[BD03](#bd03)]**, **[[RN01](#rn01)]**                 |

## 6. Requisitos Legais
Não se aplica.

## 7. Regras de Negócio

#### RN01
- Só deve ser possível alterar/excluir postagens do próprio usuário logado.

## 8. Documentos Relacionados
Não se aplica.
