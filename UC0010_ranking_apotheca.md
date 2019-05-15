# Especificação de Caso de Uso: Ranking

## 1. Descrição do Caso de Uso
Essa funcionalidade é responsável por controlar a quantidade de pontos que o usuário recebe por ação.

## 2.Pré-condições
Uma ação de postagem, voto e negativação deve ser previamente executada.

## 3.Pós-condições
Não se apica.

## 4. Fluxo de eventos
### 4.1 Fluxo Principal
#### FP
**Cadastro de postagem**

1. O usuário aciona a funcionalidade de ranking. **[[FA01](#fa01)]**, **[[FA02](#fa02)]**
1. O usuário cadastra uma nova postagem;
1. Adiciona 2 pontos ao seu ranking;
1. O caso de uso é encerrado.

### 4.2 Fluxo Alternativo

#### FA01
**Voto**

1. O usuário vota em uma postagem ou comentário;
1. Adiciona 10 pontos ao ranking do autor da postagem;
1. Retorna para o passo 4 do fluxo principal.

#### FA02
**Negativação**

1. O usuário negativa uma postagem ou comentário;
1. Diminui 10 pontos do ranking do autor da postagem;
1. Retorna para o passo 4 do fluxo principal.

#### FA02
**Reporte**

1. O usuário reporta uma postagem;
1. Diminui 10 pontos do ranking do autor da postagem;
1. Retorna para o passo 4 do fluxo principal.

### 4.3 Fluxo de Exceções
Não se aplica.

## 5.Bloco de dados
Não se aplica.

## 6. Requisitos Legais
Não se aplica.

## 7. Regras de Negócio


## 8. Documentos Relacionados
Não se aplica.
