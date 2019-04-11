# Especificação de Caso de Uso: Cadastrar Postagem

## 1. Descrição do Caso de Uso
Essa funcionalidade permite que o usuário cadastre uma postagem em alguma turma que ele participe.

## 2.Pré-condições
Ter turmas vinculados ao usuário.
## 3.Pós-condições
Uma postagem é criada.

## 4. Fluxo de eventos
### 4.1 Fluxo Principal
#### FP
**Cadastrar postagem**

1. O usuário acessa a funcionalidade cadastrar postagem;
1. Apresenta o formulário de cadastro;**[[BD01](#bd01)]**,**[[FA01](#fa01)]**
1. O usuário preenche as informações necessárias e aciona a opção de cadastrar;**[[FE01](#fe01)]**
1. Persiste as informações no banco local;
1. Verifica se há conexão com a internet; **[[FA02](#fa02)]**
1. Envia as informações para a API da apotheca, caso tenha conexão;
1. Aciona a funcionalidade UC00XX_ranking_apotheca;
1. O caso de uso é finalizado.

### 4.2 Fluxo Alternativo

#### FA01
**Editar postagem**

1. Apresenta o formulário com as informações da postagem que foram previamente cadastradas;
1. O usuário edita as informações que deseja e aciona a opção de atualizar;
1. Atualiza as informações modificadas;
1. Retorna para o passo 5 do fluxo principal.

#### FA02
**Sincronizar postagem**

1. Caso não haja conexão com a internet, guarda a informação para ser sincronizada de forma assíncrona;
1. Retorna para o passo 6 do fluxo principal.

### 4.3 Fluxo de Exceções

#### FE01
**Campos obrigatórios em branco**

1. Verifica se os campos obrigatórios foram preenchidos;
1. Caso não estejam, exibe uma mensagem de erro;
1. O caso de uso é encerrado.

## 5.Bloco de dados
### BD01
**Formulário**

| Campo                        | Tipo         | Obrigatório | Entrada/Saída | Observações                                                            |
|------------------------------|--------------|-------------|---------------|------------------------------------------------------------------------|
| Título                       | Alphanumérico| Sim         | E             |                                                                        |
| Descrição                    | Alphanumérico| Sim         | E             |                                                                        |
| Turma                        | Seleção única| Sim         | E             | Exibe as turmas vinculadas aos vínculos do usuário.                    |
| Tags                         | Autocomplete | Não         | E             | Exibe as tags já existentes no sistema, caso não exista um correspondente cadastra uma nova.|
| Anexos                       | Arquivo      | Sim         | E             | Abre a activity nativa de adicionar arquivos.                                 |

## 6. Requisitos Legais
Não se aplica.

## 7. Regras de Negócio
Não se aplica.

## 8. Documentos Relacionados
Não se aplica.
