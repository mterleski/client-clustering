# Clusterização de Clientes com K-Means

## 1. Visão Geral do Projeto
Este projeto tem como objetivo realizar a **segmentação de clientes** de um shopping utilizando o algoritmo de aprendizado não supervisionado **K-Means**. A segmentação permite identificar padrões de comportamento e agrupar os clientes em perfis distintos, fornecendo insights para estratégias de marketing personalizadas e otimização de vendas.

---

## 2. Estrutura do Dataset
O modelo utiliza o arquivo `Mall_Customers.csv`, que contém informações de **200 clientes** com os seguintes atributos:

*   **CustomerID:** Identificador único do cliente.
*   **Gender:** Gênero (Masculino / Feminino).
*   **Age:** Idade do cliente.
*   **Annual Income (k$):** Renda anual do cliente (em milhares de dólares).
*   **Spending Score (1-100):** Pontuação de gastos atribuída pelo shopping com base no comportamento de compra.

---

## 3. Pipeline do Projeto

### 🛠️ Exploração e Tratamento dos Dados
1.  **Leitura e Inspeção:** Carga dos dados utilizando a biblioteca `pandas` e verificação inicial com `.head()` e `.info()`.
2.  **Limpeza:** Verificação de dados ausentes e análise de inconsistências na variável categórica `Gender` via `.unique()`.
3.  **Seleção de Atributos:** Remoção das colunas `CustomerID` e `Gender` por não serem correlacionadas diretamente à formação geométrica dos clusters no algoritmo de distância.
4.  **Análise Descritiva:** Uso do `.describe()` para avaliar a distribuição, médias e medianas, seguido de uma análise visual de outliers via `boxplot`.

### 🤖 Modelagem (K-Means)
O projeto utiliza o algoritmo **K-Means** (via `scikit-learn`) para encontrar grupos homogêneos baseados nas características de idade, renda e pontuação de gastos. 

*Nota: O código inclui as etapas para preparação de escala dos dados (`StandardScaler`) e identificação do número ideal de clusters.*

---

## 4. Tecnologias Utilizadas

*   **Python 3**
*   **Pandas:** Manipulação e análise de dados.
*   **Seaborn / Matplotlib:** Visualização estatística e análise de outliers.
*   **Plotly Express:** Gráficos interativos para análise tridimensional dos clusters.
*   **Scikit-Learn:** Pré-processamento (`StandardScaler`) e o modelo de agrupamento (`KMeans`).
