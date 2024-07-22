# Apartment Rental Price Prediction for Sao Paulo - Brazil

<p align="center"><img src="https://camo.githubusercontent.com/2395b9addd283caae164beb046a4c22d0bcf28c6b2a56eca306248eb3ab52164/68747470733a2f2f6d7277616c6c70617065722e636f6d2f696d616765732f68642f73616f2d7061756c6f2d6272617a696c2d706f6e74652d6573746169616469612d6272696467652d717732366c35323839393537776165362e6a7067" width="550"></p>

## Visão Geral do Projeto
<p align="justify">Este projeto final para o curso de MLOps Zoomcamp visa prever os preços de aluguel de apartamentos na cidade de São Paulo, Brasil, utilizando um conjunto de dados que contém informações de aproximadamente 13.000 apartamentos. O objetivo é desenvolver um modelo de machine learning que possa ajudar potenciais inquilinos, proprietários e investidores a tomar decisões informadas sobre os preços de aluguel da grande cidade de São Paulo.</p>

#### ✅ Dataset utilizado disponível em: https://www.kaggle.com/datasets/argonalyst/sao-paulo-real-estate-sale-rent-april-2019

## Descrição do Problema
<p align="justify">Os preços de aluguel são influenciados por vários fatores, incluindo localização, tamanho, número de quartos e outras características dos imóveis. Algo que é impusionado por ser a maior cidade do Brasil, o que, consequentemente, eleva os custos e qualidade de vida, ou seja, dependendo do bairro e do prédio, os valores se alteram consideravelmente. Assim, este projeto aborda a necessidade de um modelo preditivo preciso que possa estimar os preços de aluguel com base nesses fatores para uma tomada de decisão de alugar um apartamento, seja para moradia ou para instalação de um pequeno negócio, considerando os valores e caracteristicas do apartamento.</p>

## Tecnologias e ferramentas utilizadas
### Principais tecnologias
ㅤ<img src="https://github.com/user-attachments/assets/d19d6bf8-7500-47c7-92bf-c3f46229099a" width="13">ㅤ**Vercel** - Utilizado como plataforma de hospedagem e implantação de aplicativos web baseada em nuvem  
ㅤ<img src="https://github.com/user-attachments/assets/818cc442-56fd-4400-874d-a1d0a791cfbb" width="13">ㅤ**MLflow** - Utilizado para rastreamento do experimento e registro do modelo de previsão  
ㅤ<img src="https://cdn.worldvectorlogo.com/logos/prefect-1.svg" width="13">ㅤ**Prefect** - Utilizado para orquestração do fluxo de trabalho  
ㅤ<img src="https://github.com/user-attachments/assets/8f674d6d-62f0-4e7d-a5b1-922d72911d53" width="13">ㅤ**Flask** - Utilizado para implantação do modelo (web service)  
ㅤ<img src="https://github.com/user-attachments/assets/ec87d23a-028b-43f1-b739-8195e256c817" width="13">ㅤ**Docker** - Utilizado para containerização do aplicativo    
ㅤ<img src="https://github.com/user-attachments/assets/d48aa56b-bce1-404d-9b72-25632905c001" width="13">ㅤ**Anaconda** - Utilizado para gerenciar os pacotes e criar o ambiente virtual  
ㅤ<img src="https://github.com/user-attachments/assets/27fb21a1-33bb-478e-b755-e33bec6c3bbf" width="13">ㅤ**Grafana** - Utilizado para monitoramento do desempenho do modelo de previsão  

### Bibliotecas utilizadas
ㅤ<img src="https://github.com/user-attachments/assets/9dd16004-ce95-4961-8e5a-fe22369784be" width="14">ㅤ**Pandas** - Utilizada para manipulação e análise dos dados  
ㅤ<img src="https://github.com/user-attachments/assets/97bba754-6e20-4fc9-ac8d-b8c919555837" alt="PybSklearn" width="13">ㅤ**Scikit-learn** - Utilizada para construir, treinar e avaliar o modelo de previsão  
ㅤ<img src="https://github.com/user-attachments/assets/acdeb0d6-3baf-4dda-a06d-d518e0d9a2b0" alt="PybMathplot" width="13">ㅤ**Matplotlib** - Utiliazada para a visualização dos dados  

### Outras ferramentas utilizadas para o desenvolvimento
ㅤ<img src="https://github.com/user-attachments/assets/ec1b86c6-492f-4345-ad16-6dc138b990c3" width="13">ㅤ**Git** - Utilizado para realizar o controle da versão  
ㅤ<img src="https://github.com/user-attachments/assets/704b646c-58ae-426d-8f1c-e7c2c7fc964b" width="13">ㅤ**Visual Studio Code** - Utilizado para efetuar o depuramento e gerenciamento do código Python e os demais arquivos  
ㅤ<img src="https://github.com/user-attachments/assets/d3eee82b-8a6b-4789-8182-d4d6816f0273" width="13">ㅤ**Jupyter Notebook** - Utilizado para realizar a exploração e visualização dos dados  
ㅤ<img src="https://github.com/user-attachments/assets/52316734-849b-4f46-8bf8-6a7f839405af" width="13">ㅤ**PostgreSQL** - Utilizado como gerenciamento de banco de dados relacional  


## Conjunto de Dados
<p align="justify">O conjunto de dados utilizado neste projeto inclui informações de apartamentos para alugar na grande cidade de São Paulo - Brasil, disponiblizado em abril de 2019. As principais características do conjunto de dados incluem: </p>

- **Latitude e Longitude:** Coordenadas geográficas do apartamento  
- **Número de Quartos:** Quantidade de quartos no apartamento  
- **Área Construída:** Tamanho do apartamento em metros quadrados  
- **Preço de Aluguel:** Valor do aluguel em reais brasileiros **[🎯 alvo da previsão ]**

## Estrutura do Projeto
The project has been structured with the following folders and files:

- .github: contains the CI/CD files (GitHub Actions)
- data: dataset and test sample for testing the model
- integration_tests: prediction integration test with docker-compose
- lambda: test of the lambda handler with and w/o docker
- model: full pipeline from preprocessing to prediction and monitoring using MLflow, Prefect, Grafana, Adminer, and docker-compose
- notebooks: EDA and Modeling performed at the beginning of the project to establish a baseline
- tests: unit tests
- makefile: set of execution tasks
- pyproject.toml: linting and formatting
- setup.py: project installation module
- requirements.txt: project requirements

## Execução do Projeto
#### Configuração do Ambiente
Clone o repositório:

```bash
git clone https://github.com/seuusuario/seu-repositorio.git
cd seu-repositorio
```

Crie um ambiente virtual e instale as dependências:

```bash
conda create -n previsao-aluguel python=3.9
conda activate previsao-aluguel
pip install -r requirements.txt
```

#### Exploração e Pré-processamento de Dados
Inicie o Jupyter Notebook:

```bash
jupyter notebook
```

Execute os notebooks de exploração e pré-processamento de dados:

*data_exploration.ipynb:* Exploração inicial dos dados.
*data_preprocessing.ipynb:* Limpeza e preparação dos dados para modelagem.

#### Engenharia de Recursos

Execute o notebook de engenharia de recursos:
*feature_engineering.ipynb:* Criação e transformação de características para melhorar o desempenho do modelo.

#### Construção e Avaliação do Modelo
Execute os notebooks de construção e avaliação de modelos:
*model_building.ipynb:* Desenvolvimento e treinamento de modelos de machine learning.
*model_evaluation.ipynb:* Avaliação dos modelos e seleção do melhor desempenho.

#### Deploy do Modelo
Inicie o servidor Flask para deploy do modelo:

```bash
python app.py
```

Faça as previsões usando a API:

Utilize a rota /predict para enviar dados e obter previsões de aluguel.

#### Rastreamento de Experimentos com MLflow
Inicie o MLflow para rastreamento de experimentos:

```bash
mlflow ui --backend-store-uri sqlite:///mlflow.db
```

#### Monitoramento com Grafana
Configure e inicie o Grafana para monitoramento:
Siga as instruções no arquivo monitoring_setup.md para configurar o Grafana.

--------------------------------------------------

### Project Best Practices
- ✅ Problem description: The project is well described and it's clear and understandable.
- ✅ Experiment tracking and model registry: Both experiment tracking and model registry are used.
- ✅ Workflow orchestration: Fully deployed workflow.
- ✅ Model deployment: The model deployment code is containerized and can be deployed to the cloud.
- ✅ Model monitoring: Basic model monitoring that calculates and reports metrics.
- ✅ Reproducibility: Instructions are clear, it's easy to run the code, and it works. The versions for all the dependencies are specified.

--------------------------------------------------

### Considerações e Conclusão
Este projeto oferece uma solução abrangente para o problema de prever preços de aluguel de apartamentos em São Paulo. Ao seguir uma abordagem estruturada de exploração de dados, engenharia de recursos, construção e avaliação de modelos, conseguimos desenvolver um modelo preditivo robusto. Esta solução pode ser extremamente útil para diversas partes interessadas no mercado imobiliário, auxiliando na tomada de decisões informadas sobre preços de aluguel.

Para mais informações e detalhes sobre a implementação, consulte os notebooks e arquivos de código incluídos no repositório. Esperamos que este projeto sirva como uma ferramenta valiosa para prever preços de aluguel e melhorar a eficiência do mercado imobiliário.

