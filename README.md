# Apartment Rental Price Prediction for Sao Paulo - Brazil
<p align="center"><img src="https://camo.githubusercontent.com/2395b9addd283caae164beb046a4c22d0bcf28c6b2a56eca306248eb3ab52164/68747470733a2f2f6d7277616c6c70617065722e636f6d2f696d616765732f68642f73616f2d7061756c6f2d6272617a696c2d706f6e74652d6573746169616469612d6272696467652d717732366c35323839393537776165362e6a7067" width="550"></p>

## Visão Geral do Projeto
<p align="justify">Este projeto final do curso de MLOps Zoomcamp tem como objetivo prever os preços de aluguel de apartamentos em São Paulo, Brasil, utilizando um conjunto de dados com informações sobre aproximadamente 13.000 apartamentos desta grande cidade. Dessa forma, buscou-se desenvolver um modelo de machine learning para facilitar a tomada de decisões de potenciais inquilinos, possibilidade de futura compra e até mesmo investidores ou instalação de pequenas empresas, ajudando-os a entender e avaliar melhor os preços de aluguel nessa grande metrópole, que possui diversos bairros e prédios. Assim, espero que este projeto possa contribuir, por exemplo, para uma escolha imobiliária mais transparente e acessível, culminando em decisões embasadas nos dados para ver se realmente vale a pena morar no prédio escolhido.</p>

> ✅ Dataset utilizado disponível em: https://www.kaggle.com/datasets/argonalyst/sao-paulo-real-estate-sale-rent-april-2019

## Descrição do Problema
<p align="justify">Os preços de aluguel qualquer tipo de apartamento são influenciados por vários fatores para chegar em um valor aceitável para o dono, tal como localização, tamanho/área construída, número de quartos e outras características dos imóveis. Como São Paulo (Brasil) é a maior cidade do Brasil, com muitos negócios e empresas de qualquer porte e seguimento instaladas, esses fatores acabam se potencializando, elevando os custos de vida e a qualidade de vida de maneira significativa. Desta maneira, dependendo do bairro e do prédio, os valores podem apresentar mudanças consideráveis, transformando a decisão de alugar um apartamento desafiadora, devido a necessidade de equilibrar a necessidade, dinheiro disponível e finalidade dessa locação. Neste cenário, este projeto buscou desenvolver um modelo de machine learning que possa prever, de modo mais preciso, os preços de aluguel de apartamentos para ajudar interessados a encontrar moradias acessíveis e/ou adequadas às suas necessidades.</p>

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
<p align="justify">O <a href="https://www.kaggle.com/datasets/argonalyst/sao-paulo-real-estate-sale-rent-april-2019">conjunto de dados</a> utilizado neste projeto inclui informações de apartamentos para alugar na grande cidade de São Paulo - Brasil, disponiblizado em abril de 2019. As principais características do conjunto de dados incluem: </p>

- **Latitude e Longitude:** Coordenadas geográficas do apartamento  
- **Número de Quartos:** Quantidade de quartos no apartamento  
- **Área Construída:** Tamanho do apartamento em metros quadrados (m²)  
- **Preço de Aluguel:** Valor do aluguel em reais brasileiros (R$) **[🎯 alvo da previsão ]**

## Execução do Projeto [Localmente]
### Configuração do Ambiente
Clone o repositório:

```bash
git clone https://github.com/victorfxz/Apartment_Rental_Price_Prediction/
cd Apartment_Rental_Price_Prediction
```

Crie e ative o ambiente virtual:
> OBS.: Para isso será utilizado o Ambiente Anaconda [ <a href="https://www.anaconda.com/download/success"><img src="https://github.com/user-attachments/assets/62bb7b30-50ed-4a7c-a427-05718f023c62" width="15"></a> ]

```bash
conda create -n previsao-aluguel python=3.10
conda activate previsao-aluguel
```
> Caso não tenha o pip:
> ```bash
> conda install pip

Instale todas as dependências:

```bash
pip install -r requirements.txt
```

### Exploração e Pré-processamento de Dados
Inicie o notebook `model_to_predict_apartment_rental_prices_SP-BR` com o Jupyter Notebook:

```bash
jupyter notebook
```

### Deploy do Modelo
Inicie o servidor Flask para deploy do modelo:

```bash
python app.py
```

### Rastreamento de Experimentos com MLflow
Inicie o MLflow para rastreamento de experimentos:

```bash
mlflow ui --backend-store-uri sqlite:///mlflow.db
```

### Monitoramento com Grafana
> Caso não tenha o Grafana instalado [ <a href="https://grafana.com/grafana/download?platform=windows"><img src="https://github.com/user-attachments/assets/62bb7b30-50ed-4a7c-a427-05718f023c62" width="15"></a> ]

Configure e inicie o Grafana para monitoramento:
Siga as instruções no arquivo monitoring_setup.md para configurar o Grafana.

## Considerações e Conclusão
Este projeto oferece uma solução abrangente para o problema de prever preços de aluguel de apartamentos em São Paulo. Ao seguir uma abordagem estruturada de exploração de dados, engenharia de recursos, construção e avaliação de modelos, conseguimos desenvolver um modelo preditivo robusto. Esta solução pode ser extremamente útil para diversas partes interessadas no mercado imobiliário, auxiliando na tomada de decisões informadas sobre preços de aluguel.

Para mais informações e detalhes sobre a implementação, consulte os notebooks e arquivos de código incluídos no repositório. Esperamos que este projeto sirva como uma ferramenta valiosa para prever preços de aluguel e melhorar a eficiência do mercado imobiliário.

