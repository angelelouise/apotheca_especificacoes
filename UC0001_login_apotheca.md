# Especificação de Caso de Uso: Login

## 1. Descrição do Caso de Uso
Funcionalidade responsável pela autenticação do aluno com a API da SINFO.

## 2.Pré-condições
O aluno deve possuir vínculo de graduação ativo ou inativo na UFRN.

## 3.Pós-condições
Uma conta na apotheca é criada para o discente.

## 4. Fluxo de eventos
### 4.1 Fluxo Principal
#### FP
**Criação de usuário**

1. O usuário acessa a funcionalidade de login;
1. Exibe os campos **[[BD01](#bd01)]**;
1. O usuário preenche os dados e aciona a opção de autenticar;
1. Exibe a página de autenticação com a API da UFRN;
1. O usuário preenche as informações de login e senha da UFRN e autoriza o uso dos dados pela aplicação; **[[FE01](#fe01)]**
1. Consulta os dados do usuário na API da UFRN;
1. Verifica se esses dados já estão na base de dados;
1. Caso os dados não estejam na base de dados, adiciona o registro do usuário;  **[[FA01](#fa01)]**
1. O caso de uso é encerrado.

### 4.2 Fluxo Alternativo
#### FA01
**Login com usuário já existente**

1. Caso os dados estejam na base de dados, verifica se não há alterações nas informações do usuário;
1. Caso haja alterações, atualiza as informações;
1. Retorna para o passo 9 do fluxo principal.

### 4.3 Fluxo de Exceções

#### FE01
**Usuário não possui vínculo com a UFRN**

 1. Caso a autenticação com API da SINFO falhe, exibe uma mensagem de erro;
 1. O caso de uso é encerrado.


## 5.Bloco de dados
### BD01
**Login**

| Campo                        | Tipo   | Obrigatório | Entrada/Saída | Observações                                                            |
|------------------------------|--------|-------------|---------------|------------------------------------------------------------------------|
| CPF                          | Alphanumérico | Sim         | E         | Usuário do SIGAA.                                                     |
| Autenticar                   | Button | Sim         | E         |                                                    |

## 6. Requisitos Legais
Não se aplica.

## 7. Regras de Negócio

#### RN01

## 8. Documentos Relacionados
Não se aplica.
