# Telecom X — Churn de Clientes

##  Objetivo
Este projeto tem como objetivo realizar o processo de **ETL (Extração, Transformação e Carga)** e a **Análise Exploratória de Dados (EDA)** para entender os fatores relacionados à evasão de clientes (churn) na empresa Telecom X.

Com base nesse trabalho, a equipe de Data Science poderá desenvolver modelos preditivos e estratégias de retenção de clientes.

---

##  Estrutura do Projeto
```
telecomx-churn/
├─ telecomx_churn_etl_eda.ipynb   # Notebook com ETL + EDA completo
├─ churn_clean.csv                # Dados tratados (CSV)
├─ churn_clean.parquet            # Dados tratados (Parquet)
└─ README.md                      # Este arquivo
```

---

##  Tecnologias Utilizadas
- Python 3.x
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Requests

---

##  Passos do Projeto

### 1) Extração (Extract)
- Os dados foram extraídos de um **CSV hospedado no GitHub**.
- Fonte utilizada: [Telco Customer Churn Dataset (IBM)](https://raw.githubusercontent.com/IBM/telco-customer-churn-on-icp4d/master/data/Telco-Customer-Churn.csv).

### 2) Transformação (Transform)
- Conversão de colunas numéricas (`TotalCharges`).
- Tratamento de valores nulos.
- Padronização de colunas booleanas (Yes/No → 1/0).
- Criação de novas features, como **AvgAnnualSpend**.

### 3) Carga (Load)
- Salvamento dos dados tratados em **CSV** e **Parquet**.

### 4) Análise Exploratória (EDA)
- Taxa geral de churn.
- Distribuições de tenure e charges.
- Relação entre churn e tipo de contrato.
- Gráficos de boxplot, histogramas e barras empilhadas.

---

##  Principais Achados
- Clientes com **contrato mensal (Month-to-month)** apresentam maior churn.
- Clientes com **tenure baixo (≤ 6 meses)** tendem a sair mais rápido.
- O **valor das mensalidades** pode estar relacionado à evasão em alguns segmentos.

Esses insights podem orientar campanhas de retenção, revisão de planos e ofertas personalizadas.

---

##  Como Executar
1. Clone este repositório ou faça o download dos arquivos.
2. Instale as dependências:
   ```bash
   pip install pandas numpy matplotlib seaborn requests
   ```
3. Abra o notebook no Jupyter ou Google Colab:
   ```bash
   jupyter notebook telecomx_churn_etl_eda.ipynb
   ```

---

##  Conclusão
O projeto forneceu insights valiosos sobre os padrões de churn da Telecom X e estabeleceu a base para modelagem preditiva e estratégias de retenção de clientes.

