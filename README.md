# Análise de Dados de E-commerce: Indicadores RFM

## Introdução
Este projeto foi realizado para uma empresa fictícia do ramo de e-commerce, que buscava entender melhor o comportamento de seus clientes através da análise dos indicadores de Recência, Frequência e Ticket Médio (RFM). A empresa possui um vasto conjunto de dados de compras realizadas por clientes de 37 países, com informações detalhadas sobre produtos, preços, quantidades e datas de compras.

O objetivo deste projeto foi limpar e tratar os dados, analisar padrões de compras e calcular os indicadores RFM para segmentar os clientes, fornecendo insights para a tomada de decisões estratégicas.

### Dados
1. Para acessar o dataset `DNC_desafio_5.csv`, clique [aqui](https://drive.google.com/file/d/1XQi22jMPBcsSDJIWgaHN1wMhiTSi3S9T/view?usp=sharing).
2. As informações do dataset incluem:
- `CustomerID`: Código de identificação do cliente.
- `Description`: Descrição do produto.
- `InvoiceNo`: Código da fatura.
- `StockCode`: Código de estoque do produto.
- `Quantity`: Quantidade do produto.
- `InvoiceDate`: Data do faturamento (compra).
- `UnitPrice`: Preço unitário do produto.
- `Country`: País da compra.

### Tecnologias Utilizadas
- **Python**: Utilizado para limpeza e tratamento de dados.
- **Pandas**: Biblioteca utilizada para manipulação e análise de dados.
- **Matplotlib/Seaborn**: Bibliotecas utilizadas para visualização de dados.

## Etapas do Projeto

### 1. Leitura e Inspeção dos Dados
- Leitura do dataset e inspeção inicial para entender a estrutura e a distribuição dos dados.

  ![image](https://github.com/leandroboteon/data-wrangling-marketing-rfm/assets/167100723/282b0270-67c8-4fb8-ad31-fe45f33222e7)

  ![image](https://github.com/leandroboteon/data-wrangling-marketing-rfm/assets/167100723/45448083-bf2d-40fb-8c8e-59e24949075d)

  ![image](https://github.com/leandroboteon/data-wrangling-marketing-rfm/assets/167100723/d55bbdb5-8832-42ca-a2d8-a6aceea863fa)


### 2. Tratamento de Valores Faltantes
- Identificação e remoção de valores nulos para garantir a integridade dos dados.

  ![image](https://github.com/leandroboteon/data-wrangling-marketing-rfm/assets/167100723/f10ff960-3286-4608-93a3-9067c0c7b8f2)


### 3. Tratamento de Preços Unitários e Quantidades
- Filtragem de dados inválidos (preços e quantidades menores ou iguais a zero) para assegurar análises precisas.

### 4. Remoção de Linhas Duplicadas
- Verificação e remoção de entradas duplicadas para evitar distorções nas análises.

  ![image](https://github.com/leandroboteon/data-wrangling-marketing-rfm/assets/167100723/1937d382-f7b7-42a6-b747-b40a8c97e98e)


### 5. Correção dos Tipos de Dados
- Ajuste dos tipos de dados das colunas `CustomerID` e `InvoiceDate` para facilitar a manipulação.

### 6. Tratamento de Outliers
- Identificação e remoção de outliers extremos que poderiam influenciar negativamente as análises.

  ![image](https://github.com/leandroboteon/data-wrangling-marketing-rfm/assets/167100723/5cef9c07-5b72-493b-83b7-2a4d96f2dfe1)


### 7. Criação de Coluna Adicional
- Criação de uma coluna com o preço total da compra, combinando quantidade e preço unitário.

### 8. Cálculo da Última Data de Compra
- Determinação da data da última compra no dataset para cálculo do indicador de recência.

### 9. Visualização dos Dados
- Criação de gráficos para analisar a distribuição de vendas por país, produtos mais vendidos, vendas mensais e outros insights visuais.

  ![image](https://github.com/leandroboteon/data-wrangling-marketing-rfm/assets/167100723/20460d60-21ab-45ae-8327-b4645694ddd8)
  
  ![image](https://github.com/leandroboteon/data-wrangling-marketing-rfm/assets/167100723/0250a88d-da7a-413a-b999-cb4d02854f77)
  
  ![image](https://github.com/leandroboteon/data-wrangling-marketing-rfm/assets/167100723/d1eb309f-08c2-4374-9bc9-0dc0d90b0075)
  
  ![image](https://github.com/leandroboteon/data-wrangling-marketing-rfm/assets/167100723/eec7c2c4-d6c0-4beb-8a81-bee6e7abddee)


### 10. Cálculo do RFM
- Cálculo dos indicadores de Recência, Frequência e Ticket Médio para cada cliente, segmentando-os em diferentes perfis de consumo.

  ![image](https://github.com/leandroboteon/data-wrangling-marketing-rfm/assets/167100723/ab0b35b1-04d7-42d3-952b-f1d3d722b51d)
  
  ![image](https://github.com/leandroboteon/data-wrangling-marketing-rfm/assets/167100723/9f444a0b-c4c3-4955-856d-bcba2465de95)
  
  ![image](https://github.com/leandroboteon/data-wrangling-marketing-rfm/assets/167100723/02f7fa5c-6483-4ad4-ac1b-0fce4f09105d)


### 11. Salvando o DataFrame em CSV
- Salvando o DataFrame final em um arquivo CSV para futuras análises e modelagem.

## Conclusões

- **Qualidade dos Dados:** Após a inspeção inicial, foi identificado e corrigido um número de valores faltantes, duplicados e dados inválidos. Este processo garantiu que as análises subsequentes fossem realizadas com um dataset limpo e válido.

- **Distribuição de Vendas:** A análise dos dados revelou que as vendas estão concentradas no *United Kingdom*. Essa concentração pode indicar mercados prioritários para estratégias de marketing e logística.

- **Produtos Mais Vendidos:** Os dados indicaram que há uma parcela de produtos que são responsáveis pela maior parte das vendas, onde *world war 2 gliders asstd designs* lidera. Entender quais produtos são mais populares pode ajudar a empresa a otimizar seu estoque e suas ofertas de produtos.

- **Tendências Temporais:** As visualizações mostraram variações mensais no valor total das vendas. Há um pico de vendas em *11/2011* e queda acentuada em *12/2011*.

- **Preparação para Modelagem:** Com o dataset limpo e os indicadores calculados, os dados estão prontos para serem utilizados em modelos de machine learning.
