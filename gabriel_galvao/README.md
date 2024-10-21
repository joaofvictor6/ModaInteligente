# 📊 Etapas do Projeto

## 1. Coleta e Entendimento dos Dados
O dataset utilizado neste projeto é o *Fashion Clothing Products Dataset*, que contém informações detalhadas sobre produtos de vestuário, como ID, nome do produto, marca, gênero, preço, número de imagens e descrição.

- **Fonte dos dados**: [Kaggle - Fashion Clothing Products Catalog](https://www.kaggle.com/shivamb/fashion-clothing-products-catalog)
- **Estrutura do dataset**:
  - `ProductID`: Identificador único do produto.
  - `ProductName`: Nome do produto.
  - `ProductBrand`: Marca do produto.
  - `Gender`: Gênero para o qual o produto é destinado (Masculino, Feminino, Unissex).
  - `Price (INR)`: Preço do produto em Rúpias Indianas.
  - `NumImages`: Quantidade de imagens disponíveis para o produto.
  - `Description`: Descrição do produto.
  - `PrimaryColor`: Cor principal do produto.

---

## 2. Análise Exploratória de Dados (EDA)
A análise exploratória é uma parte fundamental do projeto, pois ajuda a entender a distribuição dos dados e identificar padrões importantes que podem impactar o sistema de recomendação.

### Principais insights obtidos:
- **Distribuição dos preços**: A maioria dos produtos tem preços mais acessíveis, com uma pequena quantidade de produtos de alto valor.
- **Distribuição por gênero**: A maioria dos produtos é destinada ao público feminino, com uma boa quantidade de produtos masculinos e unissex.
- **Marcas mais frequentes**: Algumas das marcas mais populares incluem *Roadster*, *HRX* e *DressBerry*.

---

## 3. Pré-Processamento dos Dados
Antes de aplicar os modelos de aprendizado de máquina, os dados precisam ser preparados:

- **Tratamento de valores ausentes**: Algumas colunas, como `PrimaryColor`, contêm valores ausentes. Esses valores foram tratados para garantir a integridade dos dados.
- **Codificação**: Colunas categóricas como `Gender` e `ProductBrand` foram convertidas para valores numéricos utilizando *One-Hot Encoding*.
- **Normalização**: Para garantir que os dados estejam em uma escala apropriada para o aprendizado de máquina, a coluna de preços foi normalizada.

---

## 4. Criação do Sistema de Recomendação
Nesta etapa, utilizamos algoritmos de aprendizado de máquina para construir um sistema de recomendação. O modelo foi baseado em dois métodos principais:

- **Filtragem Colaborativa**: Recomendamos produtos com base no comportamento de compra de usuários semelhantes.
- **Filtragem Baseada em Conteúdo**: Recomendamos produtos com base nas características dos itens (marca, preço, cor, etc.).

### Pipeline do modelo:
- **Treinamento**: Utilizamos os dados pré-processados para treinar os modelos de recomendação.
- **Avaliação**: Avaliamos o modelo com métricas como precisão e cobertura, para garantir que as recomendações fossem relevantes.

---

## 🔚 Conclusão
O sistema **ModaInteligente** oferece uma experiência de recomendação personalizada, utilizando técnicas de aprendizado de máquina para otimizar a experiência de compra dos usuários. A análise exploratória de dados revelou informações valiosas sobre os padrões de consumo, e o sistema de recomendação foi desenvolvido para atender diferentes perfis de consumidores com sugestões personalizadas.
