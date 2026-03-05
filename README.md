# 🍔 iFood – Case de Dados (Teste A/B de Cupons)

Este projeto apresenta uma análise exploratória e uma estimativa de viabilidade financeira para um experimento **A/B de cupons**, com o objetivo de avaliar se a campanha gera impacto positivo para o negócio.

A análise foi desenvolvida utilizando **Python, Pandas e Matplotlib**, seguindo uma estrutura típica de análise de dados aplicada a produtos digitais.

---

# 📂 Estrutura do projeto

```
.
├── data/
│   ├── consumer.csv.gz
│   ├── restaurant.csv.gz
│   └── ab_test_ref.csv
│
├── notebooks/
│   └── 01_ifood_ab_test_analysis.ipynb
│
├── relatorio/
│   └── relatorio_executivo_ifood_ab_test_layout.pdf
│
└── README.md
```

**Descrição dos arquivos**

| Arquivo                                      | Descrição                                         |
| -------------------------------------------- | ------------------------------------------------- |
| consumer.csv.gz                              | Cadastro de usuários da plataforma                |
| restaurant.csv.gz                            | Cadastro de restaurantes                          |
| ab_test_ref.csv                              | Base de usuários participantes do experimento A/B |
| 01_ifood_ab_test_analysis.ipynb              | Notebook com análise completa                     |
| relatorio_executivo_ifood_ab_test_layout.pdf | Relatório executivo gerado a partir da análise    |

---

# ⚙️ Tecnologias utilizadas

* Python 3
* Pandas
* Matplotlib
* Jupyter Notebook

---

# ▶️ Como executar o projeto

## 1️⃣ Clonar o repositório

```bash
git clone https://github.com/AnnaDscience/ifood-ab-test-anna-maciel.git
cd ifood-ab-test-anna-maciel
```

---

## 2️⃣ Criar ambiente virtual (opcional)

```bash
python -m venv venv
source venv/bin/activate
```

Windows:

```bash
venv\Scripts\activate
```

---

## 3️⃣ Instalar dependências

```bash
pip install pandas matplotlib jupyter
```

---

## 4️⃣ Iniciar o Jupyter Notebook

```bash
jupyter notebook
```

Abra o notebook:

```
01_ifood_ab_test_analysis.ipynb
```

---

# 📊 Etapas da análise

O notebook está organizado nas seguintes etapas:

### 1️⃣ Carregamento dos dados

* leitura dos arquivos `.csv.gz`
* validação inicial das bases

### 2️⃣ Preparação dos dados

* junção das tabelas
* padronização de variáveis
* criação de variáveis auxiliares

### 3️⃣ Análise exploratória

* distribuição de usuários por grupo
* proporção de usuários ativos
* distribuição de mês de criação

### 4️⃣ Visualizações

* gráficos de distribuição
* comparação entre grupos controle e teste

### 5️⃣ Análise financeira (estimativa)

Como a base de pedidos (`orders`) não está disponível, foi construída uma **simulação baseada em premissas** para estimar:

* receita potencial
* custo da campanha
* ROI da iniciativa

### 6️⃣ Recomendações de experimento

* proposta de novos testes A/B
* métricas de avaliação
* guardrails de produto

---

# 📈 Premissas utilizadas

| Premissa                   | Valor |
| -------------------------- | ----- |
| Ticket médio do pedido     | R$ 60 |
| Comissão da plataforma     | 20%   |
| Valor médio do cupom       | R$ 10 |
| Taxa de conversão estimada | 5%    |

Essas premissas foram utilizadas apenas para **estimativa de viabilidade financeira**.

---

# ⚠️ Limitação da análise

O dataset fornecido **não contém dados de pedidos (`orders`)**.

Portanto, não foi possível calcular diretamente:

* conversão real
* ticket médio real
* receita incremental

Em um cenário real, a análise ideal incluiria:

* comparação de conversão entre grupos
* teste estatístico de significância
* cálculo de receita incremental

---

# 📄 Relatório executivo

O relatório final pode ser encontrado em:

```
relatorio/relatorio_executivo_ifood_ab_test_layout.pdf
```

Ele resume:

* contexto do experimento
* análise exploratória
* estimativa financeira
* recomendações estratégicas

---

# 👩‍💻 Autora

**Anna Cláudia Maciel**

Data Analyst | BI | Product Analytics

LinkedIn:
https://www.linkedin.com/in/anna-cláudia-maciel-365b8813a

---
