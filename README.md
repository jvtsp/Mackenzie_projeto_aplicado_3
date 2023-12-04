# Sistema de Recomendação

Este repositório contém um sistema de recomendação baseado no conjunto de dados MovieLens. O sistema utiliza a medida de distância Euclidiana para calcular a similaridade entre usuários e itens, e fornece recomendações com base na filtragem colaborativa por usuário.


## Visão Geral
O sistema de recomendação implementado neste repositório tem como objetivo fornecer recomendações de filmes aos usuários com base em suas preferências e nas preferências de usuários semelhantes. O sistema utiliza o conjunto de dados do MovieLens, que contém avaliações de usuários para uma grande quantidade de filmes.

As principais funcionalidades do sistema incluem:

Cálculo da similaridade entre usuários com base na medida de distância Euclidiana
Geração de recomendações por usuário
Cálculo da similaridade entre itens com base nas avaliações dos usuários

# Fonte dos Dados
Os dados utilizados neste projeto foram obtidos a partir do Kaggle: https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata/download?datasetVersionNumber=2

## Tecnologias Utilizadas
• os: é uma biblioteca nativa do Python que oferece funções para interagir com o 
sistema operacional. É útil para executar comandos de terminal, manipular arquivos 
e pastas, entre outras tarefas.
• numpy: é uma biblioteca fundamental para computação científica em Python, 
fornecendo suporte para arrays multidimensionais e funções matemáticas 
avançadas.
• matplotlib: é uma biblioteca para visualização de dados em Python, que oferece 
uma ampla variedade de gráficos e personalização de suas características.
• As bibliotecas adicionais necessárias para a análise de preferências do público são:
• mysql.connector: é uma biblioteca para conectar-se a bancos de dados MySQL. É 
necessária para acessar os dados de bilheteria, streaming e mídias sociais que 
serão utilizados no estudo.
• requests: é uma biblioteca para fazer requisições HTTP. É necessária para acessar 
dados de APIs externas, como as APIs de plataformas de streaming.
• IPython.display: é uma biblioteca para exibir dados em notebooks IPython. É útil 
para visualizar os resultados da análise de dados de forma interativa.
• tensorflow: é uma biblioteca para Machine Learning em Python. É necessária para 
treinar e aplicar modelos de Machine Learning para análise de dados.

## Como Executar
Clone este repositório em sua máquina local.
Abra um terminal na pasta raiz do projeto.
Execute o comando jupyter notebook para abrir o Jupyter Notebook em seu navegador.
Abra o Recomendacao_KNN.ipynb e execute as células de código na ordem desejada. Certifique-se de instalar todas as bibliotecas utilizadas no projeto.
Além disso, é necessário descompactar o zip na máquina e subir em um servidor MySQL, usando os seguintes comandos:


CREATE DATABASE mackenzie_recomendacao_filmes;

use mackenzie_recomendacao_filmes;

CREATE TABLE movies (
    movieId INT,
    title VARCHAR(255),
    genresmovies VARCHAR(255)
);

CREATE TABLE rating (
    userId INT,
    movieId INT,
    rating FLOAT,
    timestamp INT
);

Faça o insert do conteúdo presente nos CVS dentro dessas duas bases: Movies e Rating.

Ao finalizar, salve todas as alterações e feche o Jupyter Notebook.
