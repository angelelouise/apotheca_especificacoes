# Especificação de Caso de Uso: Buscar postagem

## 1. Descrição do Caso de Uso
Essa funcionalidade é responsável por consultar postagens de acordo com os filtros apresentados.

## 2.Pré-condições
O aluno deve estar logado no aplicativo.

## 3.Pós-condições
Não se apica.

## 4. Fluxo de eventos
### 4.1 Fluxo Principal
#### FP
1. O usuário aciona a funcionalidade de busca de postagem;
1. Exibe o formulário de pesquisa;**[[BD01](#bd01)]**
1. O usuário realiza uma pesquisa;
1. Exibe uma listagem de resultados; **[[BD02](#bd02)]**
1. O usuário seleciona uma das postagens;
1. Executa a funcionalidade UC004_detalharPostagem_apotheca;
1. O caso de uso é encerrado;

### 4.2 Fluxo Alternativo
Não se aplica.

### 4.3 Fluxo de Exceções

Não se aplica.

## 5.Bloco de dados

### BD01
**Formulário de Busca**

| Campo                        | Tipo         | Obrigatório | Entrada/Saída | Observações                                                            |
|------------------------------|--------------|-------------|---------------|------------------------------------------------------------------------|
| Título                       | Alphanumérico| Sim         | E             |                                                                        |
| Descrição                    | Alphanumérico| Sim         | E             |                                                                        |
| Turma                        | Autocomplete | Sim         | E             |                    |
| Tags                         | Autocomplete | Sim         | E             | |

### BD02
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
Não se aplica.

## 8. Documentos Relacionados
Não se aplica.
