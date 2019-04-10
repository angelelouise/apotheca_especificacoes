# Especificação de Caso de Uso: Detalhar Postagem

## 1. Descrição do Caso de Uso
Essa funcionalidade permite que usuários visualizem a postagem em detalhes, também permitindo comentários, postagem e, caso necessário, denunciar a postagem.

## 2.Pré-condições
Ter uma postagem previamente cadastrada.

## 3.Pós-condições
Não se aplica.

## 4. Fluxo de eventos
### 4.1 Fluxo Principal
#### FP
**Detalhar postagem**

1. O usuário aciona a funcionalidade de detalhar postagem;
1. Exibe os detalhes da postagem selecionada;  **[[BD01](#bd01)]**, **[[FA02](#fa02)]**, **[[FA03](#fa03)]**, **[[FA04](#fa04)]**, **[[FA05](#fa05)]**, **[[FA06](#fa06)]**, **[[FA07](#fa07)]**
1. Exibe a listagem de comentários; **[[BD02](#bd02)]**, **[[FA01](#fa01)]**
1. O caso de uso é finalizado;
### 4.2 Fluxo Alternativo

#### FA01
**Comentar postagem**

1. O usuário escreve um comentário e aciona a opção de enviar;
1. Persiste o comentário vinculado à postagem;
1. Retorna para o passo 4 do fluxo principal.

#### FA02
**Votar na postagem**

1. O usuário aciona a opção de votar na postagem;
1. Soma o contador de votos;
1. Aciona a funcionalidade UC00XX_ranking_apotheca;
1. Envia uma notificação para o criador da postagem;
1. Retorna para o passo 4 do fluxo principal.

#### FA03
**Negativar postagem**

1. O usuário aciona a opção de negativar a postagem;
1. Soma o contador de votos negativos;
1. Aciona a funcionalidade UC00XX_ranking_apotheca;
1. Envia uma notificação para o criador da postagem;
1. Retorna para o passo 4 do fluxo principal.

#### FA04
**Reportar postagem**

1. O usuário aciona a opção de reportar a postagem;
1. Exibe o formulário para descrição do motivo do reporte; **[[BD03](#bd03)]**
1. O usuário preenche as informações necessárias e aciona a opção de enviar;
1. Inativa a postagem;
1. Envia uma notificação para o criador da postagem;
1. Retorna para o passo 4 do fluxo principal.

#### FA05
**Editar postagem**

1. O usuário aciona a opção de editar postagem;
1. Redireciona para o **[[FA01](#fa01)]** da funcionalidade UC003_criarPostagem_apotheca;
1. Retorna para o passo 4 do fluxo principal.

#### FA06
**Excluir postagem**

1. O usuário aciona a opção de excluir postagem;
1. Remove a postagem da base de dados;
1. Retorna para o passo 4 do fluxo principal.

#### FA07
**Compartilhar postagem**
1. O usuário aciona a opção de compartilhar a postagem;
1. Aciona a funcionalidade UC00XX_compartilharPost_apotheca;
1. Retorna para o passo 4 do fluxo principal.

### 4.3 Fluxo de Exceções

Não se aplica.

## 5.Bloco de dados
### BD01
**Postagem**

| Campo                        | Tipo         | Obrigatório | Entrada/Saída | Observações                                                            |
|------------------------------|--------------|-------------|---------------|------------------------------------------------------------------------|
| Título                       | N/A          | Sim         | S             |                                                                        |
| Descrição                    | N/A          | Sim         | S             |                                                                        |
| Turma                        | N/A          | Sim         | S             |                                                                        |
| Tags                         | N/A          | Não         | S             |                                                                        |
| Anexos                       | Imagem       | Sim         | S             |                                                                        |
| Votar                        | Imagem       | Sim         | E             | **[[FA02](#fa02)]**, não deve ser exibido para o usuário que cadastrou a postagem.                                                    |
| Negativar                    | Imagem       | Sim         | E             | **[[FA03](#fa03)]**, não deve ser exibido para o usuário que cadastrou a postagem.                                                    |
| Compartilhar                 | Imagem       | Sim         | E             | **[[FA07](#fa07)]**                                                    |
| Reportar                     | Imagem       | Sim         | E             | **[[FA04](#fa04)]**, não deve ser exibido para o usuário que cadastrou a postagem.                                                   |
| Editar                       | Imagem       | Não         | E             | **[[FA05](#fa05)]**, só deve ser exibido para o usuário que cadastrou a postagem.                                                    |
| Excluir                      | Imagem       | Não         | E             | **[[FA06](#fa06)]**, só deve ser exibido para o usuário que cadastrou a postagem.                                                    |

### BD02
**Comentários**

| Campo                        | Tipo         | Obrigatório | Entrada/Saída | Observações                                                            |
|------------------------------|--------------|-------------|---------------|------------------------------------------------------------------------|
| Foto do perfil               | Imagem       | Sim         | S             |                                                          |
| Adicione um comentário       | Alphanumérico| Não         | E             | Não deve ser exibido para o usuário que cadastrou a postagem.          |
| Descrição do comentário      | Alphanumérico| Sim         | S             |                                                                        |

### BD03
**Formulário de reporte**
| Campo                        | Tipo         | Obrigatório | Entrada/Saída | Observações                                                            |
|------------------------------|--------------|-------------|---------------|------------------------------------------------------------------------|
| Motivo para o reporte        | Alphanumérico| Sim         | E             |                                                                        |

## 6. Requisitos Legais
Não se aplica.

## 7. Regras de Negócio
Não se aplica.

## 8. Documentos Relacionados
Não se aplica.
