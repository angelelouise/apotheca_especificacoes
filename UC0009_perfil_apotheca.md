# Especificação de Caso de Uso: Perfil

## 1. Descrição do Caso de Uso
Essa funcionalidade é responsável por exibir os detalhes da conta do usuário.

## 2.Pré-condições
O aluno deve estar logado no aplicativo.

## 3.Pós-condições
Não se apica.

## 4. Fluxo de eventos
### 4.1 Fluxo Principal
#### FP
1. O usuário aciona a funcionalidade de perfil;
1. Exibe os detalhes da conta; **[[BD01](#bd01)]**, **[[BD02](#bd02)]**, **[[FA01](#fa01)]**
1. O caso de uso é encerrado;

### 4.2 Fluxo Alternativo

#### FA01
**Atualizar dados**
1. O usuário aciona a opção de editar dados;
1. Exibe os detalhes da conta com os campos editáveis; **[[BD01](#bd01)]**
1. Retorna para o passo 3 do fluxo principal.

### 4.3 Fluxo de Exceções

Não se aplica.

## 5.Bloco de dados

### BD01
**Perfil**

| Campo                        | Tipo         | Obrigatório | Entrada/Saída | Observações                                                            |
|------------------------------|--------------|-------------|---------------|------------------------------------------------------------------------|
| Foto do perfil               | Imagem       | Sim         | E/S           | É editável.                                                                 |
| Nome do usuário              |Alphanumérico | Sim         | S             | Não é editável.                                                                   |
| Cursos                       |Alphanumérico | Sim         | S             | Não é editável.                                                                  |
| Sobre mim...                 |Alphanumérico | Sim         | E/S           | É editável.                                                                   |
| Editar                       |Imagem        | Não         | E             | **[[FA01](#fa01)]**                                                                   |

### BD02
**Ranking**

| Campo                        | Tipo         | Obrigatório | Entrada/Saída | Observações                                                            |
|------------------------------|--------------|-------------|---------------|------------------------------------------------------------------------|
| Posts                        |Numérico      | Sim         | S             | Contador de posts.                                                                  |
| Rank                         |Numérico      | Sim         | S             | **[[RN01](#rn01)]**, **[[RN02](#rn02)]**, **[[RN03](#rn03)]**, **[[RN04](#rn04)]**, **[[RN05](#rn05)]**                                                                  |
| Pontos                       |Numérico      | Sim         | S             | Contador de pontos.                                                                  |


## 6. Requisitos Legais
Não se aplica.

## 7. Regras de Negócio

#### RN01
- Pontos entre 0 e 200 classificam no rank "Calouro de CeT".

#### RN02
- Pontos entre 200 e 400 classificam no rank "Universitário Inocente".

#### RN03
- Pontos entre 400 e 600 classificam no rank "Veterano Sofrido".

#### RN04
- Pontos entre 600 e 800 classificam no rank "Master nos Paranauê".

#### RN05
- Pontos a partir de 800  classificam no rank "Expert Master Blaster".

## 8. Documentos Relacionados
Não se aplica.
