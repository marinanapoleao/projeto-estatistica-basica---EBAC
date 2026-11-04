# Projeto Estatística Básica

<img width="1797" height="592" alt="Estatistica Basica" src="https://github.com/user-attachments/assets/d82e6715-882f-46e8-8aba-1820646886c9" />

## 📌 Sobre o Projeto

Projeto de análise exploratória de dados de produtos de um supermercado localizado no Chile, utilizando conceitos de estatística descritiva e visualização de dados.

O trabalho investiga o comportamento dos preços dos produtos por categoria, a dispersão dos valores, a presença de outliers e a distribuição dos descontos aplicados por categoria e marca.

## 🎯 Objetivo

Analisar os preços e descontos dos produtos de um supermercado, identificando padrões de distribuição, variações entre categorias e diferenças nos descontos praticados pelas marcas.

## 💻​ Problema de Negócio / Pergunta de Pesquisa

O projeto busca responder a perguntas relacionadas à estrutura de preços e às políticas de desconto do supermercado:
- Quais categorias apresentam maiores e menores preços médios?
- Como os preços se distribuem dentro de cada categoria?
- Quais categorias apresentam maior variação de preços?
- Existem produtos com preços muito diferentes dos demais (outliers)?
- Quais categorias apresentam maiores médias de descontos?
- Como os descontos se distribuem entre diferentes marcas e categorias?
  
## 📊 Fonte de Dados

Base de dados de produtos de um supermercado do Chile, contendo 1.107 registros e 7 colunas.

Variável -----	Descrição

Title -----	Nome do produto

Marca -----	Marca do produto

Preco_Normal -----	Preço habitual do produto

Preco_Desconto -----	Preço após aplicação de desconto

Preco_Anterior -----	Preço praticado antes do desconto

Desconto -----	Valor do desconto aplicado

Categoria -----	Categoria do produto

*As categorias estão identificadas em espanhol.*


## 🛠️ LINGUAGENS E BIBLIOTECAS

- Python: linguagem de programação.

- Pandas: manipulação e análise de dados.

- NumPy: operações numéricas.

- SciPy: identificação de outliers utilizando Z-score.

- Plotly Express: construção de gráficos interativos.

- Matplotlib: biblioteca importada para visualizações.

## 🔍 Metodologia

*1. Análise de preços por categoria*
- Cálculo da média e mediana da variável Preco_Normal.
- Agrupamento dos produtos por categoria.
- Comparação entre média e mediana para identificar diferenças na distribuição dos preços.

*2. Análise da dispersão dos preços*
- Cálculo do desvio padrão por categoria.
- Identificação das categorias com maior e menor dispersão.
- Comparação entre média, mediana e desvio padrão.

*3. Identificação de outliers*
- Construção de boxplot para investigar a distribuição dos preços.
- Aplicação do método Z-score para identificar valores extremos.

*4. Análise dos descontos por categoria*
- Agrupamento dos produtos por categoria.
- Cálculo da média da variável Desconto.
- Construção de gráfico de barras para comparar os descontos médios.

*5. Análise de descontos por categoria e marca*
- Agrupamento dos registros por categoria e marca.
- Construção de treemaps interativos para visualizar a distribuição dos descontos.

## 📈  Resultados e Métricas

#### *Estatísticas gerais dos preços*

Indicador ———————————— Resultado

Quantidade de produtos —————— 1.107

Preço normal médio ———————— 2.070,99

Preço normal mediano ——————— 1.269,00

Desvio padrão do preço normal ——— 2.961,26

Preço normal mínimo ———————— 0

Preço normal máximo ———————— 19.788

#### *Média e mediana dos preços por categoria*

Categoria  ———————— Média ————— Mediana

Comidas preparadas ———— 3.095,04 ———— 3.290,00

Laticínios ————————— 2.385,22 ———— 989,00

Congelados ———————— 2.108,04 ———— 1.519,00

Beleza e cuidados pessoais — 1.783,56 ———— 1.569,00

Frutas —————————— 1.724,47 ———— 1.195,00

Verduras ————————— 1.343,30 ———— 1.180,00

Instantâneos e sopas ———— 765,49 ———— 439,00


#### *Desvio padrão por categoria*

Categoria ———————— Desvio padrão

Laticínios ————————— 3.925,82

Beleza e cuidados pessoais —— 2.210,04

Congelados ———————— 2.111,54

Comidas preparadas ————— 2.019,91

Frutas —————————— 1.639,15

Instantâneos e sopas ——— 1.170,23

Verduras ————————— 1.012,70

#### *Média da variável Desconto por categoria*

Categoria ————————— Média de desconto

Congelados ———————————— 154,03

Beleza e cuidados pessoais ————— 123,08

Comidas preparadas ———————— 43,48

Laticínios ————————————— 17,41

Frutas ——————————————— 0

Instantâneos e sopas ———————— 0

Verduras —————————————— 0

#### *Análise de outliers*

O notebook apresenta a aplicação de Z-score considerando valores absolutos iguais ou superiores a 3.

Entretanto, existe uma divergência: a anotação do projeto registra 8 outliers (índices 53 a 60), enquanto a saída da execução salva apresenta uma relação com 32 registros. Essa quantidade precisa ser conferida.

## 💡 Principais Insights e Implicações

#### *1. Diferença na distribuição dos preços entre categorias*

- A categoria de comidas preparadas apresenta média inferior à mediana (3.095,04 contra 3.290,00). Nas demais categorias, a média é superior à mediana.

- Isso indica que a distribuição dos preços apresenta comportamentos diferentes entre as categorias.

- Implicação para o negócio: utilizar média e mediana em conjunto para compreender melhor a estrutura de preços, evitando que produtos de valores elevados distorçam a percepção do preço habitual de uma categoria.

#### *2. Grande dispersão de preços em laticínios*

- Laticínios apresentam o maior desvio padrão (3.925,82), além de uma média de 2.385,22 e mediana de 989,00.

- Implicação para o negócio: investigar a variedade de produtos e marcas dessa categoria, identificando diferenças relevantes de posicionamento de preço.

#### *3. Maior estabilidade de preços em verduras*

- Verduras apresentam o menor desvio padrão (1.012,70), além de média e mediana relativamente baixas.

- Implicação para o negócio: acompanhar a estabilidade dos preços dessa categoria e utilizá-la como referência comparativa para outras categorias com maior variação.

#### *4. Diferenças nos descontos entre categorias*

- Congelados e produtos de beleza e cuidados pessoais apresentam as maiores médias na variável Desconto.

- Frutas, verduras e instantâneos e sopas apresentam médias iguais a zero.

- Implicação para o negócio: investigar as estratégias promocionais adotadas para cada categoria e avaliar oportunidades de campanhas de desconto.

#### *5. Diferenças entre marcas*

- O treemap por categoria e marca permite visualizar a distribuição da variável Desconto entre os diferentes fabricantes.

- Implicação para o negócio: utilizar essa visualização para comparar as práticas promocionais entre marcas e identificar quais apresentam maiores valores médios de desconto.

## ⚠️​ Pontos de atenção na documentação: 

o código do boxplot apresenta uma inconsistência: a categoria é filtrada como Lacteos, mas aparece como lacteos na base. Além disso, o gráfico utiliza o dataframe completo, e não o dataframe filtrado. Portanto, o boxplot salvo não representa exclusivamente os laticínios.

## 👩‍💻 Sobre a Autora

Desenvolvido por Marina Napoleão — Cientista de Dados / Analista de Dados. 
### LinkedIn <https://www.linkedin.com/in/marina-napoleao/>
### GitHub <https://github.com/marinanapoleao> 
