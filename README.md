# Previsão de Preços de Imóveis no Airbnb do Rio de Janeiro

### Contexto

No Airbnb, qualquer pessoa que tenha um quarto ou um imóvel de qualquer tipo (apartamento, casa, chalé, pousada, etc.) pode ofertar o seu imóvel para ser alugado por diária.

Você cria o seu perfil de host (pessoa que disponibiliza um imóvel para aluguel por diária) e cria o anúncio do seu imóvel.

Nesse anúncio, o host deve descrever as características do imóvel da forma mais completa possível, de forma a ajudar os locadores/viajantes a escolherem o melhor imóvel para eles (e de forma a tornar o seu anúncio mais atrativo)

Existem dezenas de personalizações possíveis no seu anúncio, desde quantidade mínima de diária, preço, quantidade de quartos, até regras de cancelamento, taxa extra para hóspedes extras, exigência de verificação de identidade do locador, etc.

### Nosso objetivo

Construir um modelo de previsão de preço que permita uma pessoa comum que possui um imóvel possa saber quanto deve cobrar pela diária do seu imóvel.

Ou ainda, para o locador comum, dado o imóvel que ele está buscando, ajudar a saber se aquele imóvel está com preço atrativo (abaixo da média para imóveis com as mesmas características) ou não.

### O que temos disponível, inspirações e créditos

As bases de dados foram retiradas do site kaggle: https://www.kaggle.com/allanbruno/airbnb-rio-de-janeiro

## Sumário

- [Contexto](#contexto)
- [Estrutura do Projeto](#estrutura-do-projeto)
- [Bibliotecas Utilizadas](#bibliotecas-utilizadas)
- [Como Executar o Projeto](#como-executar-o-projeto)
- [Detalhes do Modelo](#detalhes-do-modelo)
- [Contribuição](#contribuição)
- [Licença](#licença)



## Estrutura do Projeto

- `deployprojeto.py`: Script principal que implementa a interface de previsão utilizando o Streamlit.
- `modelo.joblib`: Arquivo contendo o modelo treinado (ExtraTreesRegressor).
- `dados.csv`: Conjunto de dados utilizado para treinamento e teste do modelo.
- `README.md`: Documento de explicação do projeto.

## Bibliotecas Utilizadas

As seguintes bibliotecas Python foram utilizadas para a construção deste projeto:

- `pandas`: Manipulação e análise de dados.
- `pathlib`: Manipulação de caminhos de arquivos e diretórios.
- `numpy`: Computação numérica.
- `seaborn`: Visualização de dados baseada no matplotlib.
- `matplotlib`: Biblioteca de plotagem para criar gráficos estáticos, animados e interativos.
- `plotly`: Biblioteca de visualização gráfica interativa.
- `scikit-learn`: Ferramentas de machine learning para análise de dados e modelagem preditiva.
- `gc`: Interface para coleta de lixo (garbage collection) no Python.
- `streamlit`: Framework para criação de aplicações web interativas para Data Science.

## Como Executar o Projeto

### Pré-requisitos

- Python 3.x
- Instalar as bibliotecas necessárias:

```bash
pip install pandas numpy seaborn matplotlib plotly scikit-learn streamlit joblib```
Detalhes do Modelo
O modelo utilizado para a previsão de preços é o ExtraTreesRegressor, que foi treinado com os dados disponíveis em dados.csv. As características do imóvel, como latitude, longitude, número de quartos, tipo de imóvel, entre outras, são utilizadas como input para o modelo.

Métricas de Avaliação
O desempenho do modelo foi avaliado utilizando as seguintes métricas:

R² (R-Squared): Métrica que indica o quão bem o modelo se ajusta aos dados observados.
RMSE (Root Mean Squared Error): Mede a diferença média entre os valores previstos e os valores observados.



