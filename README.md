# ifood-case
Case Téc­ni­co Data Sci­en­ce - iFo­od

## Modelo de Recomendacao de Cupons Personalizados
### Descrição do Desafio

Com o objetivo de engajar os clientes, este desafio solicita uma estratégia eficiente de distribuição de ofertas e deve considerar o tipo de cupom, canal de envio, perfil do cliente e momento do envio.

Este desafio tem como objetivo:

1. Analisar dados históricos de transações, ofertas e clientes;
2. Desenvolver uma técnica/modelo para recomendar a melhor oferta para cada cliente;
3. Demonstrar o impacto da solução no negócio.

## Modelagem
Para o desenvolvimento do modelo de recomendação de ofertas, foi utilizado o **Random Forest**, uma técnica robusta para classificação, que é capaz de lidar bem com grandes volumes de dados e variáveis complexas. Abaixo estão os detalhes sobre as abordagens utilizadas:

1. **Pré-processamento dos Dados**:
   - **StringIndexer**: Para converter variáveis categóricas em índices numéricos.
   - **VectorAssembler**: Para combinar várias colunas em um único vetor de características para o modelo.

2. **Modelagem**:
   - **Random Forest Classifier**: Escolhido para a tarefa de classificação, dado que é eficaz para lidar com dados complexos e grande dimensionalidade.
   
3. **Avaliação**:
   - **BinaryClassificationEvaluator**: Utilizado para avaliar a performance do modelo com base em métricas como AUC (Area Under Curve).

4. **Ajuste de Hiperparâmetros**:
   - **CrossValidator**: Utilizado para validação cruzada durante o processo de ajuste de hiperparâmetros.
   - **ParamGridBuilder**: Para definir a grade de parâmetros que seriam testados durante o tuning.


##  Estrutura do Repositório

```bash
ifood-case/
├── data/                  # Datasets
│   ├── raw/              # Dados originais (.json)
│   └── processed/        # Dados processados (PySpark)
├── notebooks/            # Jupyter Notebooks
│   ├── 1_data_processing.ipynb
│   └── 2_modeling.ipynb
├── presentation/         # Slides de apresentação para stakeholders
├── requirements.txt      # Dependências do projeto
└── README.md             # Este arquivo
```

##  Tecnologias Utilizadas

- Python 3.9+
- PySpark (Databricks Community Edition)
- Pandas / NumPy
- Matplotlib / Seaborn
- Databricks Community Edition ([https://community.cloud.databricks.com/](https://community.cloud.databricks.com/))

##  Como Executar

### 1. Clonar o repositório

```bash
git clone https://github.com/seu-usuario/blob-case.git
cd blob-case
```

### 2. Instalar dependências (opcional para Databricks)

```bash
pip install -r requirements.txt
```

>  Recomendado utilizar o [Databricks Community Edition](https://community.cloud.databricks.com/) para executar notebooks com PySpark.


### 3. Executar os notebooks

- `notebooks/1_data_processing.ipynb`: Responsável pela limpeza, transformação e unificação dos dados.
- `notebooks/2_modeling.ipynb`: Responsável pela criação do modelo de recomendação e avaliação.

### 5. Apresentação dos Resultados

Os insights e impacto da solução estão detalhados na pasta `presentation/`.

##  Objetivo do Modelo

Criar um modelo de recomendação que personalize as ofertas enviadas, maximizando as chances de conversão e engajamento dos clientes.

##  Métricas e Avaliação

A escolha do modelo e métricas foi baseada em testes e validação cruzada. Métricas consideradas:

- AUC/ROC

##  Conclusão

Este projeto propõe uma abordagem de recomendação baseada em dados históricos de comportamento de compra, perfil dos clientes e tipos de oferta disponíveis. A solução pode ser integrada facilmente a canais de marketing para otimizar campanhas e aumentar a conversão.

