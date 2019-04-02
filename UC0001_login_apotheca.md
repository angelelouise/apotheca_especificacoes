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
1. O usuário preenche os dados e aciona a opção de logar;
1. Verifica se já possui conta na base de dados; **[[FE02](#fe02)]**
1. Caso o login indicado não esteja na base de dados, faz a autenticação com a API da UFRN;  **[[FA01](#fa01)]**
 **[[FE01](#fe01)]**
1. Cria uma conta para o usuário na API da apotheca;
1. O caso de uso é encerrado.

### 4.2 Fluxo Alternativo
#### FA01
**Login com usuário já existente**

1. Caso possua conta na base de dados, faz o login na conta;
1. Retorna para o passo 7 do fluxo principal.

### 4.3 Fluxo de Exceções

#### FE01
**Usuário não possui vínculo com a UFRN**

 1. Caso a autenticação com API da SINFO falhe, exibe uma mensagem de erro;
 1. O caso de uso é encerrado.

#### FE02
**Senha não compatíveis com a do SIGAA**

1. Caso o usuário esteja na base de dados, verifica se a senha indicada corresponde à do banco.
1. Caso não sejam iguais, exibe uma mensagem de erro;
1. O caso de uso é encerrado.

## 5.Bloco de dados
### BD01
**Login**

| Campo                        | Tipo   | Obrigatório | Entrada/Saída | Observações                                                            |
|------------------------------|--------|-------------|---------------|------------------------------------------------------------------------|
| Usuário                      | Alphanumérico    | Sim         | E         | Usuário do SIGAA.                                                     |
| Senha                        | Alphanumérico    | Sim         | E         | Senha do SIGAA.                                                                   |
## 6. Requisitos Legais
Não se aplica.

## 7. Regras de Negócio

#### RN01

## 8. Documentos Relacionados
Não se aplica.
