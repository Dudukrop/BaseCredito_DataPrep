# Pré-processamento de Dados de Crédito

Este projeto envolve o pré-processamento de um conjunto de dados de crédito para preparar os dados para análise e modelagem de machine learning. O foco é a limpeza, visualização e escalonamento dos dados, que serão utilizados para prever a probabilidade de um cliente não pagar seu empréstimo.

## Visão Geral do Projeto

O conjunto de dados utilizado contém informações sobre clientes, incluindo renda, idade, montante do empréstimo e se o cliente não pagou o empréstimo (`default`). As etapas de pré-processamento abordadas incluem a limpeza de dados, tratamento de valores ausentes e anomalias, e escalonamento de características.

## Etapas do Projeto

### Importação de Bibliotecas e Carregamento de Dados

- Bibliotecas utilizadas: `pandas`, `numpy`, `matplotlib`, `seaborn`, `plotly`, `sklearn`, `pickle`.
- Os dados são carregados de um arquivo CSV e armazenados em um DataFrame do pandas.

### Análise Exploratória de Dados (EDA)

- **Descritiva dos Dados**: Utiliza `describe()` para obter estatísticas básicas sobre os dados.
- **Detecção de Valores Ausentes**: Identificação de valores ausentes, especialmente na coluna `age`, que possui 3 valores faltantes.
- **Visualização de Dados**:
  - `boxplot` para identificar outliers na coluna `age`.
  - `countplot` para visualizar a distribuição da variável alvo `default`.
  - `scatter_matrix` para explorar relações entre `age`, `income` e `loan`.

### Limpeza de Dados

- **Correção de Idade Negativa**: Substituição de valores negativos na coluna `age` pela média das idades válidas.
- **Tratamento de Valores Ausentes**: Preenchimento de valores ausentes na coluna `age` com a mediana das idades.

### Escalonamento de Dados

- **Normalização**: Utilização do `StandardScaler` do `sklearn` para normalizar as variáveis `income`, `age` e `loan`.

### Divisão de Dados

- **Train-Test Split**: Divisão dos dados em conjuntos de treino e teste com 75% para treino e 25% para teste, utilizando `train_test_split`.

### Serialização de Dados

- **Pickle**: Salvamento dos conjuntos de treino e teste em um arquivo `credit.pkl` para uso posterior em modelagem de machine learning.

## Conclusão

O pré-processamento de dados é uma etapa crítica para garantir que o conjunto de dados esteja limpo e pronto para a modelagem. O projeto demonstra a importância de lidar com dados ausentes, normalizar características e preparar os dados para futuras análises.

## Requisitos

- Python 3.x
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Plotly
- Scikit-learn

## Execução do Projeto

1. Certifique-se de que todos os requisitos estão instalados.
2. Execute o script para realizar o pré-processamento dos dados.
3. Utilize o arquivo `credit.pkl` gerado para treinamentos posteriores de modelos de machine learning.

## Referências

- [Pandas Documentation](https://pandas.pydata.org/pandas-docs/stable/)
- [Plotly Documentation](https://plotly.com/python/)
- [Scikit-learn Documentation](https://scikit-learn.org/stable/documentation.html)
