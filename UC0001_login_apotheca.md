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

### 4.2 Fluxo Alternativo
Não se aplica.

### 4.3 Fluxo de Exceções

#### FE01
**Usuário não possui vínculo com a UFRN**

#### FE02
**Senha não é compatível com a do SIGAA**

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
