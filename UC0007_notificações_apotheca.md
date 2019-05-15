# Especificação de Caso de Uso: Notificações

## 1. Descrição do Caso de Uso
Essa funcionalidade exibe todas as notificações ligadas ao usuário logado.

## 2.Pré-condições
O aluno deve estar logado no aplicativo.

## 3.Pós-condições
Não se apica.

## 4. Fluxo de eventos
### 4.1 Fluxo Principal
#### FP
1. O usuário aciona a funcionalidade de notificações;
1. Consulta todas as notificações pendentes de visualização;
1. Exibe uma listagem de notificações; **[[BD01](#bd01)]**, **[[FA01](#fa01)]**, **[[FA02](#fa02)]**, **[[FA03](#fa03)]**, **[[FA04](#fa04)]**
1. O caso de uso é encerrado.

### 4.2 Fluxo Alternativo

#### FA01
**Marcar como lida**

1. O usuário desliza uma notificação para a direita;
1. Marca a notificação como lida e oculta da listagem;
1. Retorna para o passo 4 do fluxo principal.

#### FA02
**Visualizar notificações de votos, negativações e comentários**

1. O usuário seleciona uma notificação de voto, negativação ou comentário;
1. Executa a funcionalidade UC004_detalharPostagem_apotheca;
1. Retorna para o passo 4 do fluxo principal.

#### FA03
**Visualizar notificações de ranking**

1. O usuário seleciona uma notificação de ranking;
1. Executa a funcionalidade UC009_perfil_apotheca;
1. Retorna para o passo 4 do fluxo principal.

#### FA04
**Visualizar notificações de reporte**

1. O usuário seleciona uma notificação de reporte;
1. Exibe o motivo para o reporte;
1. Retorna para o passo 4 do fluxo principal.

### 4.3 Fluxo de Exceções

Não se aplica.

## 5.Bloco de dados

### BD01
**Lista de postagem**

| Campo                        | Tipo         | Obrigatório | Entrada/Saída | Observações                                                            |
|------------------------------|--------------|-------------|---------------|------------------------------------------------------------------------|
| Foto do perfil               | Imagem       | Sim         | S             |                                                          |
| Usuário                      | Alphanumérico| Sim         | S             |                                                                        |
| Ação                         | Alphanumérico| Sim         | S             | Apresenta as opções: "[usuário] [Curtiu/Comentou/Negativou] sua postagem", "[usuário] [Curtiu/Negativou] seu comentário", "Seu ranking subiu para [ranking]", "Sua postagem foi reportada, dessa forma, ela foi ocultada do fórum."                                                                        |
| Timeframe                    | Alphanumérico| Sim         | S             | Diferença entre a data do cadastro da postagem em relação a data atual.|

## 6. Requisitos Legais
Não se aplica.

## 7. Regras de Negócio


## 8. Documentos Relacionados
Não se aplica.
