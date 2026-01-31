📦 Previsão de Estoque Inteligente na AWS com SageMaker Canvas

Este repositório contém a solução desenvolvida para o Desafio de Projeto da DIO:

Previsão de Estoque Inteligente na AWS com SageMaker Canvas.

O projeto demonstra a criação de um modelo de Machine Learning no-code utilizando o Amazon SageMaker Canvas, com foco em previsão de estoque baseada em dados históricos de preço, promoção e variação de estoque.

🎯 Objetivo do Projeto

Desenvolver um modelo preditivo capaz de estimar a quantidade de estoque de produtos, auxiliando na tomada de decisão para:
- Planejamento de reposição
- Redução de rupturas de estoque
- Otimização de custos operacionais
- Antecipação de demanda em períodos promocionais

🧰 Tecnologias e Serviços Utilizados

- Amazon SageMaker Canvas (ML No-Code)
- Amazon S3 para armazenamento do dataset
- Machine Learning – Regressão
- GitHub para versionamento e documentação

📊 Dataset Utilizado

O modelo foi treinado utilizando o dataset:

dataset-1000-com-preco-promocional-e-renovacao-estoque.csv

O dataset contém 1.000 registros históricos, com as seguintes variáveis:

- ID_PRODUTO	- Identificador do produto
- DATA_EVENTO	- Data do registro
- PRECO	- Preço do produto
- FLAG_PROMOCAO	- Indica se o produto estava em promoção (0 = Não, 1 = Sim)
- QUANTIDADE_ESTOQUE	- Quantidade disponível em estoque (variável alvo)

Esse conjunto de dados permite analisar o impacto de preço e promoções na variação do estoque ao longo do tempo.

🚀 Passo a Passo do Desenvolvimento

1️⃣ Upload do Dataset

1. Acesse o Amazon SageMaker Canvas no console da AWS
2. Faça o upload do arquivo CSV presente na pasta datasets/
3. Verifique a integridade e os tipos de dados após a importação

2️⃣ Construção e Treinamento do Modelo

No SageMaker Canvas:
- Tipo de problema: Regressão
- Variável alvo (Target):
   - QUANTIDADE_ESTOQUE
- Variáveis de entrada (Features):
  - PRECO
  - FLAG_PROMOCAO
  - DATA_EVENTO
  - ID_PRODUTO (como identificador)

Após a configuração, foi iniciado o treinamento automático do modelo.

3️⃣ Análise do Modelo

Após o treinamento, foram avaliadas:
- Métricas de desempenho (RMSE, MAE)
- Importância das variáveis
- Comportamento do modelo ao longo do tempo

Principais insights:
- O preço influencia diretamente a variação do estoque
- A variável FLAG_PROMOCAO apresentou forte impacto na previsão, indicando aumento da demanda durante promoções
- A variável temporal permitiu capturar padrões sazonais

4️⃣ Geração de Previsões

O modelo treinado foi utilizado para gerar previsões futuras de estoque.

Os resultados podem ser utilizados para:
- Planejamento de compras
- Estratégias promocionais
- Redução de perdas por excesso ou falta de estoque

📈 Resultados e Insights de Negócio

O SageMaker Canvas permitiu criar um modelo de Machine Learning sem a necessidade de código. As previsões apresentaram boa aderência aos dados históricos e o modelo pode ser expandido para múltiplos produtos e lojas. Por fim, a inclusão de dados promocionais torna as previsões mais realistas para cenários de varejo.

🧠 Conclusão
Este projeto demonstrou a aplicação prática de Machine Learning na nuvem utilizando ferramentas no-code. O Amazon SageMaker Canvas mostrou-se uma solução eficiente para criar modelos preditivos de forma rápida, visual e acessível, sendo ideal para profissionais que desejam aplicar ML sem necessidade de programação avançada.
