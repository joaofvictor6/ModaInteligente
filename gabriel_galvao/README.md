# 📊 ModaInteligente - Sistema de Recomendação de Moda

---

## 1. Coleta e Entendimento dos Dados

Neste projeto, utilizei o *Fashion Clothing Products Dataset*, que contém informações detalhadas sobre produtos de vestuário. A análise desses dados foi o ponto de partida para entender o contexto e criar o sistema de recomendação.

### **Fonte dos dados**
[Kaggle - Fashion Clothing Products Catalog](https://www.kaggle.com/shivamb/fashion-clothing-products-catalog)

## Estrutura do Projeto

```plaintext
ModaInteligente/
├── dados/                         # Arquivos de dados (não versionados)
├── notebooks/                     # Notebooks principais
│   ├── 01_EDA.ipynb               # Análise exploratória de dados
│   ├── 02_Preprocessamento.ipynb  # Pré-processamento dos dados
│   ├── 03_TF-IDF_e_Clusterizacao.ipynb  # TF-IDF e clusterização
├── resultados/                    # Resultados e visualizações
│   ├── metricas.md                # Resumo das métricas e resultados
│   └── figuras/                   # Gráficos gerados durante o projeto
├── README.md                      # Descrição geral do projeto
├── requirements.txt               # Dependências do projeto
└── .gitignore                     # Arquivos e pastas ignorados pelo Git

---

## 2. Análise Exploratória de Dados (EDA)

A **Análise Exploratória de Dados (EDA)** foi fundamental para entender o dataset e identificar padrões relevantes para o sistema de recomendação.

### **Principais insights obtidos**
- **Distribuição dos preços**: A maioria dos produtos tem preços acessíveis, com uma pequena quantidade de itens premium.
- **Distribuição por gênero**: A maior parte dos produtos é destinada ao público feminino, mas também há opções para os públicos masculino e unissex.
- **Marcas mais populares**: As marcas mais frequentes incluem *Roadster*, *HRX* e *DressBerry*.

---

## 3. Pré-Processamento dos Dados

Antes de construir o sistema de recomendação, foi necessário realizar o pré-processamento dos dados para garantir sua integridade e adequação aos modelos de aprendizado de máquina.

### **Etapas do pré-processamento**
1. **Tratamento de valores ausentes**:
   - Substituí valores ausentes na coluna `PrimaryColor` por "Desconhecido".
2. **Codificação de variáveis categóricas**:
   - Utilizei *One-Hot Encoding* para converter colunas como `Gender` e `ProductBrand` em valores numéricos.
3. **Normalização dos preços**:
   - Escalei os valores na coluna `Price` para uma faixa entre 0 e 1 usando `MinMaxScaler`.

---

## 4. Criação do Sistema de Recomendação

Nesta etapa, desenvolvi o sistema de recomendação utilizando duas abordagens principais: **Filtragem Colaborativa** e **Filtragem Baseada em Conteúdo**.

### **Abordagens Utilizadas**
- **Filtragem Colaborativa**:
  - Recomendações baseadas em padrões de comportamento de usuários semelhantes.
- **Filtragem Baseada em Conteúdo**:
  - Recomendações baseadas nas características dos produtos, como marca, preço e cor.

### **Pipeline do modelo**
1. **Treinamento**:
   - Utilizei os dados pré-processados para treinar os modelos.
2. **Avaliação**:
   - A eficácia do sistema foi avaliada utilizando métricas como precisão e cobertura.

---

## 5. Clusterização com TF-IDF

Além das recomendações diretas, utilizei **TF-IDF** para representar os textos na coluna `Description` e apliquei o algoritmo de **K-Means** para identificar agrupamentos de produtos similares.

### **Passos Realizados**
1. **TF-IDF**:
   - Transformei as descrições de texto em uma matriz numérica com as palavras mais relevantes.
2. **Clusterização com K-Means**:
   - Identifiquei clusters de produtos semelhantes e os associei às suas características.

---

## 🔚 Conclusão

O sistema **ModaInteligente** foi desenvolvido para oferecer recomendações personalizadas e análises estratégicas de produtos de vestuário.

### **Principais Etapas**
1. Entender o dataset e extrair insights com a EDA.
2. Pré-processar os dados para torná-los utilizáveis pelos modelos.
3. Construir um sistema de recomendação eficiente baseado em aprendizado de máquina.
4. Aplicar TF-IDF e K-Means para agrupar produtos e oferecer recomendações estratégicas.

### **Próximos Passos**
- Expandir o sistema para incorporar **recomendações personalizadas B2B**, ajudando empresas a identificar oportunidades de mercado.
- Implementar outros algoritmos, como **Redes Neurais** e **Sistemas Híbridos**, para melhorar a precisão das recomendações.

---

## 📋 Tecnologias Utilizadas

- **Linguagem**: Python
- **Bibliotecas**:
  - **Pandas**, **NumPy**: Manipulação de dados.
  - **Scikit-learn**: Modelos de aprendizado de máquina.
  - **NLTK**: Processamento de linguagem natural.
  - **Matplotlib**, **Seaborn**: Visualização de dados.
  - **Missingno**: Visualização de valores ausentes.
