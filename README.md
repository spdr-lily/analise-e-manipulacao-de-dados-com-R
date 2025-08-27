# Análise de Dados de Viagens Aéreas (1958–1960) em R

## Introdução

Este relatório apresenta a análise de um conjunto de dados contendo o número de passageiros de viagens aéreas mensais nos anos de **1958, 1959 e 1960**. O objetivo é compreender **tendências sazonais** e **médias mensais**, utilizando a linguagem **R** e o ecossistema **tidyverse**, que oferece ferramentas para manipulação, transformação e visualização de dados.

## Metodologia

### Carregamento de pacotes
- Utilização das bibliotecas do **tidyverse**, que incluem funções para manipulação e visualização de dados.

### Importação dos dados
- Os dados foram carregados a partir de um arquivo **CSV** disponível em link público.
- O arquivo contém a **quantidade de passageiros por mês** ao longo dos três anos considerados.
- As primeiras linhas do *data frame* foram inspecionadas para validação.

### Transformação dos dados
- Criação da variável `Average_Passengers` com a função `mutate()`, armazenando a **média mensal de passageiros** entre 1958 e 1960.
- O cálculo foi realizado com `rowMeans()`, desconsiderando a coluna de meses, permitindo observar uma **tendência geral**.

### Reformulação para análise
- Utilização de `pivot_longer()` para converter as colunas referentes a cada ano para o **formato longo**, com duas variáveis principais:
  - `Year` (ano)
  - `Passengers` (número de passageiros)
- Esse formato é mais adequado para **visualizações comparativas**.

### Visualização dos dados
- Utilização do pacote **ggplot2** para criar um **gráfico de linhas**, comparando a variação do número de passageiros ao longo dos meses para cada ano.
- `geom_line()` traçou as linhas correspondentes aos anos.
- O eixo **x** representou os **meses** e o eixo **y** o **número de passageiros**.
- Cores distintas foram aplicadas para diferenciar os anos.
- Foi adotado o **tema minimalista** para maior clareza visual.

## Resultados

- O gráfico gerado possibilitou a **comparação clara** entre os anos de **1958, 1959 e 1960**.
- Observou-se um **crescimento consistente** no número de passageiros, além de **padrões sazonais recorrentes** ao longo dos meses.
- A coluna `Average_Passengers` forneceu uma **visão consolidada da média mensal**, auxiliando na identificação das **tendências gerais**.

## Conclusão

A análise, embora simples, permitiu identificar **padrões sazonais** e **crescimento ao longo dos anos**.  
O uso de funções do **tidyverse** demonstrou eficiência na **manipulação e transformação dos dados**, enquanto o **ggplot2** possibilitou uma **visualização clara e objetiva**.  
Esse fluxo — **importação, transformação e visualização** — ilustra bem as etapas fundamentais de um **processo de análise de dados em R**.
