# 🍔 iFood – Case de Dados (Análise de Experimento A/B de Cupons)

Este projeto apresenta uma **análise exploratória e avaliação de viabilidade financeira** de uma campanha de cupons utilizando **experimento A/B**.

O objetivo é verificar se oferecer cupons para um grupo de usuários gera **impacto positivo em conversão e receita** para a plataforma.

A análise foi desenvolvida utilizando **Python e Databricks**, simulando um cenário real de análise de produto em empresas de tecnologia.

---

# 📊 Objetivo do Experimento

O experimento separa os usuários em dois grupos:

**Grupo Controle**

* Não recebe cupom
* Serve como baseline para comparação

**Grupo Teste (Target)**

* Recebe cupom promocional
* Objetivo é medir aumento de conversão

A análise busca responder:

* O grupo teste possui comportamento diferente do controle?
* A campanha de cupons gera impacto positivo?
* A campanha é financeiramente viável?

---

# 📂 Estrutura do Projeto

```
ifood-ab-test-anna-maciel/
│
├── notebooks/
│   └── 01_ifood_ab_test_analysis.ipynb
│
├── data/
│   ├── consumer.csv.gz
│   ├── restaurant.csv.gz
│   └── ab_test_ref.csv
│
├── relatorio/
│   └── relatorio_executivo_ifood_ab_test_layout.pdf
│
└── README.md
```

### Descrição dos arquivos

| Arquivo                                      | Descrição                                                |
| -------------------------------------------- | -------------------------------------------------------- |
| consumer.csv.gz                              | Cadastro de usuários da plataforma                       |
| restaurant.csv.gz                            | Cadastro de restaurantes                                 |
| ab_test_ref.csv                              | Base que identifica usuários do grupo controle e teste   |
| 01_ifood_ab_test_analysis.ipynb              | Notebook com análise exploratória e simulação financeira |
| relatorio_executivo_ifood_ab_test_layout.pdf | Relatório executivo com resultados e recomendações       |

---

# ⚙️ Tecnologias Utilizadas

* Python
* Pandas
* Matplotlib
* Databricks


---

# ▶️ Como executar o projeto

## 🔹 Opção 1 — Executar no Databricks (Recomendado)

A análise foi originalmente desenvolvida no **Databricks**.

### 1️⃣ Criar um workspace

https://www.databricks.com

### 2️⃣ Criar um Cluster

Configuração sugerida:

* Runtime: Databricks Runtime 13+
* Language: Python

---

### 3️⃣ Importar o notebook

Menu:

```
Workspace → Import
```

Importar o arquivo:

```
01_ifood_ab_test_analysis.ipynb
```

---

### 4️⃣ Fazer upload dos datasets

Menu:

```
Data → Add Data → Upload File
```

Upload dos arquivos:

```
consumer.csv.gz
restaurant.csv.gz
ab_test_ref.csv
```

---

### 5️⃣ Ajustar caminho dos arquivos

Exemplo:

```python
consumer = pd.read_csv("/dbfs/FileStore/consumer.csv.gz")
restaurant = pd.read_csv("/dbfs/FileStore/restaurant.csv.gz")
ab_test = pd.read_csv("/dbfs/FileStore/ab_test_ref.csv")
```

---

### 6️⃣ Executar o notebook

Selecionar:

```
Run All
```

---

# 💻 Execução alternativa (local)

Caso prefira rodar localmente.

### 1️⃣ Clonar repositório

```bash
git clone https://github.com/AnnaDscience/ifood-ab-test-anna-maciel.git
cd ifood-ab-test-anna-maciel
```

### 2️⃣ Instalar dependências

```bash
pip install pandas matplotlib jupyter
```

### 3️⃣ Rodar notebook

```bash
jupyter notebook
```

Abrir:

```
01_ifood_ab_test_analysis.ipynb
```

---

# 📈 Etapas da Análise

A análise foi dividida em quatro etapas principais.

### 1️⃣ Preparação dos dados

* Leitura dos datasets
* Validação das colunas
* Criação de variáveis auxiliares
* Identificação de grupos do experimento

---

### 2️⃣ Análise exploratória

Foram avaliados:

* distribuição de usuários por grupo
* proporção de usuários ativos
* distribuição de data de criação das contas

Essa etapa garante que os grupos são **comparáveis**.

---

### 3️⃣ Visualizações

Foram criados gráficos para avaliar:

* equilíbrio do experimento
* evolução temporal dos usuários
* diferenças entre grupos

---

### 4️⃣ Simulação de impacto financeiro

Como o dataset não possui dados de pedidos (`orders`), foi construída uma **simulação baseada em premissas de negócio**.

Premissas utilizadas:

| Premissa                   | Valor |
| -------------------------- | ----- |
| Ticket médio               | R$ 60 |
| Comissão da plataforma     | 20%   |
| Valor médio do cupom       | R$ 10 |
| Taxa de conversão estimada | 5%    |

---

# 📊 Resultados estimados

Baseado nas premissas:

* Usuários impactados: **445.925**
* Pedidos estimados: **22.296**
* Receita total gerada: **R$ 1.337.775**
* Receita iFood: **R$ 267.555**
* Custo da campanha: **R$ 222.962**

Resultado estimado:

**ROI aproximado: 20%**

---

# 🧠 Recomendações Estratégicas

Com base na análise, são recomendadas as seguintes ações:

### 1️⃣ Escalar campanhas vencedoras

Expandir campanhas que apresentarem ROI positivo.

### 2️⃣ Segmentar usuários

Aplicar diferentes estratégias para:

* novos usuários
* usuários recorrentes
* usuários inativos

### 3️⃣ Otimizar custo de cupons

Testar variações como:

* cupons com pedido mínimo
* desconto percentual com teto
* cupons exclusivos para segmentos específicos

---

# 📄 Relatório Executivo

O relatório executivo completo pode ser encontrado em:

```
relatorio/relatorio_executivo_ifood_ab_test_layout.pdf
```

O relatório apresenta:

* contexto do experimento
* análise exploratória
* simulação financeira
* recomendações estratégicas

---

# 👩‍💻 Autora

**Anna Cláudia Maciel**

Data Analyst | BI | Product Analytics

LinkedIn
https://www.linkedin.com/in/anna-cláudia-maciel-365b8813a

GitHub
https://github.com/AnnaDscience
