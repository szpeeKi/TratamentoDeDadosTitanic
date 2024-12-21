# TratamentoDeDadosTitanic
# Projeto: Análise Exploratória de Dados (EDA) e Preparação de Dados

Este projeto tem como objetivo realizar uma análise exploratória de dados (EDA) e preparar o conjunto de dados para modelagem. O dataset utilizado contém informações sobre passageiros do Titanic e é amplamente utilizado para aprendizado em machine learning.

## Etapas do Projeto

### 1. Carregamento dos Dados
- Os dados foram carregados a partir de um arquivo CSV.
- Exibição inicial das primeiras linhas e informações gerais sobre o dataset, como tipos de dados e valores ausentes.

### 2. Limpeza de Dados
- **Remoção de colunas irrelevantes:** Foram descartadas as colunas `PassengerId`, `Ticket` e `Cabin` por não contribuírem diretamente para a análise.
- **Tratamento de valores ausentes:**
  - A coluna `Age` teve valores ausentes preenchidos com a mediana da idade, agrupada por título (`Mr.`, `Mrs.`, etc.) e classe do passageiro (`Pclass`).
  - Valores ausentes em `Fare` foram preenchidos com o valor 7.

### 3. Engenharia de Atributos
- **Extração de títulos:** Criada a coluna `titulo` a partir do nome dos passageiros.
- **Mapeamento de variáveis categóricas:**
  - A coluna `Sex` foi convertida para valores binários: `male` = 1, `female` = 0.
  - A coluna `Embarked` foi codificada usando `OneHotEncoder`.
- **Ordenação de classes:**
  - A coluna `Pclass` foi transformada em uma variável ordinal usando `OrdinalEncoder`, com a ordem definida como 1 > 2 > 3.

### 4. Visualização de Dados
- Um boxplot foi criado para visualizar a distribuição de idades por classe.
- Um heatmap foi gerado para analisar as correlações entre as variáveis numéricas.

### 5. Conversão e Otimização
- As colunas numéricas foram convertidas para tipos de dados mais eficientes para reduzir o consumo de memória.

## Bibliotecas Utilizadas
- **Pandas:** Manipulação de dados.
- **Seaborn e Matplotlib:** Visualização de dados.
- **Scikit-learn:** Codificação de variáveis categóricas.

## Estrutura do Código
- O código foi dividido em células (é compatível com Jupyter Notebook) para facilitar a organização e execução de cada etapa.

## Resultados
- Os dados foram limpos e preparados para análise ou treinamento de modelos de machine learning.
- Foi criado um DataFrame otimizado, sem valores ausentes, e com variáveis adequadas para modelagem.

## Como Executar
1. Certifique-se de ter o Python instalado na sua máquina.
2. Instale as bibliotecas necessárias com o comando:
   ```bash
   pip install pandas seaborn matplotlib scikit-learn
   ```
3. Coloque o arquivo `tested.csv` na pasta `./dados/`.
4. Execute o script no seu ambiente Python ou em um Jupyter Notebook.

## Conclusão
Este projeto demonstrou o processo de limpeza e preparação de dados, que é essencial para qualquer análise ou modelagem preditiva. Com os dados prontos, é possível aplicar algoritmos de machine learning e explorar previsões de forma mais eficaz.

