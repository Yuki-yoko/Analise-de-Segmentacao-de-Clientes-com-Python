# Análise de Segmentação de Clientes com Python

Análise exploratória de dados de clientes com o objetivo de identificar características e padrões entre os diferentes segmentos (**A, B, C e D**). O projeto cobre limpeza, organização, exploração e visualização dos dados, buscando entender melhor o perfil e o comportamento de cada grupo.

## Dataset

- **Fonte:** [Customer Segmentation – Kaggle](https://www.kaggle.com/datasets/vetrirah/customer?select=Train.csv)
- **Arquivo utilizado:** `train.csv`
- **Tamanho original:** 8.068 linhas e 11 colunas

| Coluna | Descrição |
|---|---|
| `ID` | Identificador do cliente |
| `Gender` | Gênero (Male / Female) |
| `Ever_Married` | Se o cliente já foi casado (Yes / No) |
| `Age` | Idade |
| `Graduated` | Se o cliente é graduado (Yes / No) |
| `Profession` | Profissão |
| `Work_Experience` | Anos de experiência profissional |
| `Spending_Score` | Nível de gastos (Low / Average / High) |
| `Family_Size` | Tamanho da família |
| `Var_1` | Categoria anônima do cliente |
| `Segmentation` | Segmento do cliente (A, B, C ou D) |

## Tratamento dos Dados

- Verificação de tipos, valores ausentes e duplicados (nenhuma linha duplicada encontrada).
- Preenchimento de valores ausentes:
  - **Moda:** `Ever_Married`, `Graduated` e `Profession`.
  - **Mediana:** `Work_Experience` e `Family_Size`.
- Remoção das linhas com `Var_1` ou `Graduated` vazios.
- Base final com **7.992 clientes** e nenhum valor nulo.

## Análises Realizadas

**Análise geral dos clientes**

- Idade mínima, máxima e mediana.
- Distribuição por gênero, estado civil e formação.
- Profissões mais e menos frequentes.
- Distribuição do Spending Score e do tamanho das famílias.
- Experiência profissional (mínimo, máximo, mais comum e média).

**Análise por segmento**

- Quantidade e percentual de clientes em cada segmento.
- Idade média por segmento.
- Gênero, estado civil, profissão e Spending Score dentro de cada segmento.

## Gráficos Desenvolvidos

Foram criados **3 gráficos** com a biblioteca **Matplotlib** para visualizar os resultados da análise.

### 1. Gráfico de Barras: Quantidade de Clientes por Segmento

Mostra quantos clientes existem em cada segmento (A, B, C e D), facilitando a comparação do tamanho de cada grupo. O segmento **D** é o maior e o **B** o menor.


### 2. Gráfico de Pizza: Proporção de Gênero dos Clientes

Exibe o percentual de homens e mulheres na base: **54,8% homens** e **45,2% mulheres**.


### 3. Gráfico de Barras Empilhadas: Spending Score por Segmento

Mostra como o nível de gastos (*Low*, *Average* e *High*) se distribui dentro de cada segmento. Nele é possível ver que os segmentos **A**, **B** e **D** têm predominância de gasto *Low*, enquanto o **C** concentra mais clientes de gasto *Average*.


## Principais Resultados

- **Gênero:** 54,83% homens e 45,17% mulheres; os homens predominam em todos os segmentos.
- **Segmentos:** o **D** é o maior (28,09%) e o **B** é o menor (23,09%).
- **Idade média:** o **C** tem os clientes mais velhos (~49 anos) e o **D** os mais novos (~33 anos).
- **Estado civil:** nos segmentos A, B e C predominam clientes que já casaram; no D predominam os que nunca casaram.
- **Profissão:** *Artist* é a mais comum na base e nos segmentos A, B e C; no D predomina *Healthcare*.
- **Spending Score:** 60,42% dos clientes têm gasto *Low*; o segmento **C** concentra mais clientes de gasto *Average* e *High*, enquanto o **D** concentra o gasto *Low*.

## Tecnologias Utilizadas

- Python 
- Pandas
- Matplotlib
- Jupyter Notebook

## 📂 Estrutura do Projeto

```
├── Customer_Segmentation.ipynb   # Notebook com toda a análise
├── train.csv                     # Dataset
├── imagens/                      # Prints dos gráficos
│   ├── grafico_barras_segmento.png
│   ├── grafico_pizza_genero.png
│   └── grafico_empilhado_spending_score.png
└── README.md                     # Documentação do projeto
```

## Autor
Cristina Yuki Yokomizo

Projeto desenvolvido para fins de estudo e construção de portfólio na área de Análise de Dados.
