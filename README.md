# Apartment Rental Price Prediction for Sao Paulo - Brazil

![image](https://github.com/user-attachments/assets/08dfcef6-d72e-4d09-b00b-35237371d6db)

This project has been developed as part of the MLOps Zoomcamp course provided by DataTalks.Club.
Below you can find some instructions to understand the project content.

--------------------------------------------------

### Visão Geral do Projeto
Este projeto visa prever os preços de aluguel de apartamentos na cidade de São Paulo, Brasil, utilizando um conjunto de dados que contém informações de aproximadamente 13.000 apartamentos. O objetivo é desenvolver um modelo de machine learning que possa ajudar potenciais inquilinos, proprietários e investidores a tomar decisões informadas sobre os preços de aluguel.

### Project Description
No mercado imobiliário, prever com precisão os preços de aluguel é crucial para diversas partes interessadas. Os preços de aluguel são influenciados por vários fatores, incluindo localização, tamanho, número de quartos e outras características dos imóveis. Este projeto aborda a necessidade de um modelo preditivo preciso que possa estimar os preços de aluguel com base nesses fatores.

### Objetivos do Projeto
*Exploração e Pré-processamento de Dados:* Entender o conjunto de dados, lidar com valores ausentes e preparar os dados para a modelagem.
*Engenharia de Recursos:* Extrair características significativas e criar novas que possam melhorar o desempenho do modelo.
*Construção do Modelo:* Desenvolver e treinar vários modelos de machine learning para prever os preços de aluguel.
*Avaliação do Modelo:* Avaliar os modelos utilizando métricas apropriadas e selecionar o que tiver melhor desempenho.
*Predição:* Utilizar o modelo selecionado para fazer previsões em dados não vistos.

*Git*: Version control.
*Visual Studio Code:* Development environment.
*Jupyter Notebook:* Data exploration and visualization.
*PostgreSQL:* Data storage.
*Python:* Main programming language.
*Pandas:* Data manipulation and analysis.
*Matplotlib:* Data visualization.
*Scikit-learn:* Machine learning modeling.
*Flask:* Model deployment.
*MLflow:* Experiment tracking.
*Docker:* Application containerization.
*Anaconda:* Package and environment management.
*Grafana:* Monitoring.

--------------------------------------------------
### Conjunto de Dados
O conjunto de dados utilizado neste projeto inclui informações de apartamentos para venda e aluguel na cidade de São Paulo, anunciados em abril de 2019. As principais características do conjunto de dados incluem:

*Latitude e Longitude:* Coordenadas geográficas do apartamento.
*Número de Quartos:* Quantidade de quartos no apartamento.
*Área Construída:* Tamanho do apartamento em metros quadrados.
*Preço de Aluguel:* Valor do aluguel (alvo da previsão). 

### Tech Stack

<div style="display: inline_block"><br>
  <img align="center" src="https://camo.githubusercontent.com/3d768e26ac10ba994a60ed19acd487895cc43a9cdd43e9305c2408b93136234d/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f6769742d2532334630353033332e7376673f7374796c653d666f722d7468652d6261646765266c6f676f3d676974266c6f676f436f6c6f723d7768697465">
  <img align="center" src="https://camo.githubusercontent.com/998382ebc9a32162128b00b597ea488192df024fd015e5edec001fe29fcb93a6/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f56697375616c25323053747564696f253230436f64652d3030373864372e7376673f7374796c653d666f722d7468652d6261646765266c6f676f3d76697375616c2d73747564696f2d636f6465266c6f676f436f6c6f723d7768697465">
    <img align="center" src="https://camo.githubusercontent.com/0562f16a4ae7e35dae6087bf8b7805fb7e664a9e7e20ae6d163d94e56b94f32d/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f707974686f6e2d3336373041303f7374796c653d666f722d7468652d6261646765266c6f676f3d707974686f6e266c6f676f436f6c6f723d666664643534">
    <img align="center" src="https://camo.githubusercontent.com/ca8ee16f3ff90cf3349be99b021b0b2a366cd71499ef20bcdc2b43dbc2668483/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f416e61636f6e64612d2532333434413833332e7376673f7374796c653d666f722d7468652d6261646765266c6f676f3d616e61636f6e6461266c6f676f436f6c6f723d7768697465">
    <img align="center" src="https://camo.githubusercontent.com/c044ae9d0419850e7f2385c22ea5de56e101e6a616789bd35d2d8fa137a63642/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f6a7570797465722d2532334641304630302e7376673f7374796c653d666f722d7468652d6261646765266c6f676f3d6a757079746572266c6f676f436f6c6f723d7768697465">
     <img align="center" src="https://camo.githubusercontent.com/05cab52d05663cecbe47a23ca71075ba81b9080dd50561d0f76eb46e902cfef8/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f70616e6461732d2532333135303435382e7376673f7374796c653d666f722d7468652d6261646765266c6f676f3d70616e646173266c6f676f436f6c6f723d7768697465">
     <img align="center" src="https://camo.githubusercontent.com/edd8c9123ff9093143508af0b218cffc132f16a014be2d2147894458c351dc23/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f4d6174706c6f746c69622d2532336439656164332e7376673f7374796c653d666f722d7468652d6261646765266c6f676f3d4d6174706c6f746c6962266c6f676f436f6c6f723d626c61636b">
     <img align="center" src="https://camo.githubusercontent.com/6854ba9612c2cb025e7c65445787d93f6436d4691303601506e0bc28be2ae9b8/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f506f737467726553514c2d3331363139323f7374796c653d666f722d7468652d6261646765266c6f676f3d706f737467726573716c266c6f676f436f6c6f723d7768697465">
     <img align="center" src="https://camo.githubusercontent.com/d7eb681a1d19819ff9caeee4e3b0b1748da0b97af47e2084ca3d5e8302aec8a9/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f7363696b69742d2d6c6561726e2d2532334637393331452e7376673f7374796c653d666f722d7468652d6261646765266c6f676f3d7363696b69742d6c6561726e266c6f676f436f6c6f723d7768697465">
     <img align="center" src="https://camo.githubusercontent.com/40b50389027e826f74eb106c67530673ffc46486250581ca5845fc7284f7c717/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f4d4c666c6f772d3031393445322e7376673f7374796c653d666f722d7468652d6261646765266c6f676f3d4d4c666c6f77266c6f676f436f6c6f723d7768697465">
      <img align="center" src="https://camo.githubusercontent.com/9ed458fea6ba5324c019bbc32f837fbceaca74f3862454a77d7e94150b97fc48/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f666c61736b2d2532333030302e7376673f7374796c653d666f722d7468652d6261646765266c6f676f3d666c61736b266c6f676f436f6c6f723d7768697465">
      <img align="center" src="https://camo.githubusercontent.com/8396abd667a0eca7d28cdb29ec63b6bf29a7854c7c3d467e6ece648c7e9b81e1/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f646f636b65722d2532333064623765642e7376673f7374796c653d666f722d7468652d6261646765266c6f676f3d646f636b6572266c6f676f436f6c6f723d7768697465">
      <img align="center" src="https://camo.githubusercontent.com/a00920b123df05b3df5e368e509f18bacd65bc5909698fb42be5f35063550f47/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f747970657363726970742d2532333030374143432e7376673f7374796c653d666f722d7468652d6261646765266c6f676f3d74797065736372697074266c6f676f436f6c6f723d7768697465">
      <img align="center" src="https://camo.githubusercontent.com/65f3aaa6432363f0979f3e35bc4783d5b39753d50d200e0c149fc5c78e1eeb49/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f4e6578742e6a732d626c75653f7374796c653d666f722d7468652d6261646765266c6f676f3d4e6578742e6a73266c6f676f436f6c6f723d7768697465253232">
       <img align="center" src="https://camo.githubusercontent.com/bfe42a01bfb74a48dabc254065e874f313ca2aedd9bde944cb8bb4f9cef69dd4/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f6e6f64652e6a732d3033363834663f7374796c653d666f722d7468652d6261646765266c6f676f3d6e6f64652e6a73266c6f676f436f6c6f723d7768697465"> 
      <img align="center" src="https://camo.githubusercontent.com/509859c3a417eb3ea794450d88303bdaced996cba60811e552e5a89bf89ff584/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f67726166616e612d2532334634363830302e7376673f7374796c653d666f722d7468652d6261646765266c6f676f3d67726166616e61266c6f676f436f6c6f723d7768697465">
      <img align="center" src="https://camo.githubusercontent.com/b9ff564d8c311812747f1aacea54cf703d850756f9179f9eff6899da20a701a2/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f76657263656c2d2532333030303030302e7376673f7374796c653d666f722d7468652d6261646765266c6f676f3d76657263656c266c6f676f436f6c6f723d7768697465">
      </div>

--------------------------------------------------

### Project Structure
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

--------------------------------------------------

### Project Structure
Execução do Projeto
Configuração do Ambiente
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

Exploração e Pré-processamento de Dados
Inicie o Jupyter Notebook:

```bash
jupyter notebook
```

Execute os notebooks de exploração e pré-processamento de dados:
*data_exploration.ipynb:* Exploração inicial dos dados.
*data_preprocessing.ipynb:* Limpeza e preparação dos dados para modelagem.

Engenharia de Recursos
Execute o notebook de engenharia de recursos:
*feature_engineering.ipynb:* Criação e transformação de características para melhorar o desempenho do modelo.

Construção e Avaliação do Modelo
Execute os notebooks de construção e avaliação de modelos:
*model_building.ipynb:* Desenvolvimento e treinamento de modelos de machine learning.
*model_evaluation.ipynb:* Avaliação dos modelos e seleção do melhor desempenho.

Deploy do Modelo
Inicie o servidor Flask para deploy do modelo:

```bash
python app.py
```

Faça as previsões usando a API:

Utilize a rota /predict para enviar dados e obter previsões de aluguel.
Rastreamento de Experimentos com MLflow
Inicie o MLflow para rastreamento de experimentos:

```bash
mlflow ui --backend-store-uri sqlite:///mlflow.db
```

Monitoramento com Grafana
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

###Considerações e Conclusão
Este projeto oferece uma solução abrangente para o problema de prever preços de aluguel de apartamentos em São Paulo. Ao seguir uma abordagem estruturada de exploração de dados, engenharia de recursos, construção e avaliação de modelos, conseguimos desenvolver um modelo preditivo robusto. Esta solução pode ser extremamente útil para diversas partes interessadas no mercado imobiliário, auxiliando na tomada de decisões informadas sobre preços de aluguel.

Para mais informações e detalhes sobre a implementação, consulte os notebooks e arquivos de código incluídos no repositório. Esperamos que este projeto sirva como uma ferramenta valiosa para prever preços de aluguel e melhorar a eficiência do mercado imobiliário.

