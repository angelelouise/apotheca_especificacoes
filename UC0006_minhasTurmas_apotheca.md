# Especificação de Caso de Uso: Minhas Turmas

## 1. Descrição do Caso de Uso
Essa funcionalidade permite listar todas as turmas ligadas aos vínculos de graduação do aluno.

## 2.Pré-condições
O aluno deve estar logado no aplicativo.

## 3.Pós-condições
Não se apica.

## 4. Fluxo de eventos
### 4.1 Fluxo Principal
#### FP
1. O usuário aciona a funcionalidade de consultar minhas turmas;
1. Consulta todas as turmas de todos os vínculos do usuário; **[[RN01](#rn01)]**
1. Exibe a listagem com as turmas; **[[BD01](#bd01)]**
1. O usuário seleciona uma das turmas da lista;
1. Executa a funcionalidade UC003_criarPostagem_apotheca, enviando a turma selecionada;
1. O caso de uso é encerrado.

### 4.2 Fluxo Alternativo
Não se aplica.

### 4.3 Fluxo de Exceções
Não se aplica.

## 5.Bloco de dados

### BD01
**Minhas turmas**
| Campo                        | Tipo         | Obrigatório | Entrada/Saída | Observações                                                            |
|------------------------------|--------------|-------------|---------------|------------------------------------------------------------------------|
| (Código da turma) - Nome da Turma | Alphanumérico| Sim         | E             |                                                                        |


## 6. Requisitos Legais
Não se aplica.

## 7. Regras de Negócio

#### RN01
- Serão consultadas turmas de todos os vínculos, mesmo que inativos.

## 8. Documentos Relacionados
Não se aplica.
