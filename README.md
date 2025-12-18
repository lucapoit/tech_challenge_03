[[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/lucapoit/tech_challenge_03/blob/main/tech_challenge_03.ipynb)](https://github.com/lucapoit/tech_challenge_03/blob/main/tech_challenge_03_colab.ipynb)

# 🛫 Predição de Cancelamento de Voos – EDA + Modelagem

Este projeto realiza uma **Análise Exploratória de Dados (EDA)** seguida de um processo de **modelagem preditiva** para identificar a probabilidade de **cancelamento de voos nos Estados Unidos**.  
O estudo utiliza três arquivos principais do dataset original:

- `flights`
- `airlines`
- `airports`

Todo o fluxo — da EDA até os modelos finais — está detalhado no notebook, disponível no Google Colab.

---

## 📘 Notebook no Google Colab

👉 **[Clique aqui para abrir o notebook no Google Colab][([![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/lucapoit/tech_challenge_03/blob/main/tech_challenge_03.ipynb))](https://github.com/lucapoit/tech_challenge_03/blob/main/tech_challenge_03_colab.ipynb)**  
*(Ele contém todas as análises, gráficos, modelagens e conclusões.)*

---

## 📊 1. Análise Exploratória dos Dados (EDA)

A EDA foi conduzida de forma completa, buscando entender o comportamento geral dos dados de voos e suas relações.  
Incluiu:

- Distribuições gerais dos dados  
- Contagens e estatísticas descritivas  
- Análises de atraso e cancelamento  
- Visualizações com gráficos e mapas  
- Correlações entre variáveis de tempo, companhia aérea e aeroportos  

O objetivo principal foi identificar padrões que pudessem influenciar o **cancelamento dos voos**.

---

## 🔧 2. Preparação e Engenharia de Atributos

Para viabilizar a modelagem, foram aplicados os seguintes processos:

### ✔️ Tratamento de datas
Extração de:
- Dia da semana  
- Mês  
- Horário  
- Diferença entre horários programados e reais  

### ✔️ Enriquecimento com API de Feriados
Os dados foram integrados com uma API de feriados dos EUA, adicionando uma feature indicando se o voo ocorria em um feriado nacional.

### ✔️ Tratamento de nulos
Foram avaliados e tratados casos relevantes de valores ausentes, buscando minimizar perda de informação.

---

## 🤖 3. Modelagem Preditiva – Cancelamento de Voos

O problema foi formulado como uma **classificação binária**, com classes fortemente desbalanceadas (a maior parte dos voos não é cancelada).

### ✔️ Modelo Base: XGBoost
Foi escolhido o **XGBoost**, por sua robustez em problemas tabulares e desbalanceados.

### ✔️ Otimização com Bayesian Search
Após a criação do modelo base, realizou-se um ajuste fino dos hiperparâmetros utilizando **Bayesian Optimization**, buscando:

- Reduzir overfitting  
- Melhorar capacidade de generalização  
- Ajustar profundidade, taxa de aprendizado e número de árvores  

---

## 🧪 4. Experimentos com K-Means + PCA

Além do modelo supervisionado, também foi conduzida uma análise não supervisionada:

### ✔️ Clusterização com K-Means  
Criou-se um modelo base para tentar agrupar voos com padrões semelhantes.

### ✔️ Testes com PCA  
Utilizou-se PCA para:

- Reduzir dimensionalidade  
- Remover colinearidade entre features  
- Verificar se clusters ficavam mais separados

Esses experimentos serviram como apoio à compreensão estrutural dos dados.

---

## 📦 Tecnologias Utilizadas

- Python  
- Pandas, NumPy  
- Scikit-Learn  
- XGBoost  
- PCA  
- Seaborn / Matplotlib  
- Requests (API de feriados)  
- Google Colab  

---

## 📁 Estrutura do Projeto


└── tech_challenge_03.ipynb


---

## 📌 Conclusão

O projeto fornece um pipeline completo — desde exploração inicial até modelos supervisionados e não supervisionados — oferecendo insights sobre os fatores que influenciam o cancelamento de voos nos Estados Unidos.

Todo o processo está documentado no notebook disponibilizado via Colab.


