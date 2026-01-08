# Tech Challenge – Fase 03 | Análise PNAD COVID-19

## 📌 Descrição do Projeto

Este repositório contém a implementação de um pipeline analítico desenvolvido a partir dos **microdados da PNAD COVID-19 (IBGE)**, com o objetivo de estruturar, modelar e analisar informações relevantes para o **planejamento hospitalar em cenários de surtos epidemiológicos**.

O projeto foi construído como parte do **Tech Challenge – Fase 03 (Pós-Tech Data Analytics - FIAP)** e tem foco em:
- Organização de dados para análise;
- Modelagem dimensional (Star Schema);
- Consultas analíticas voltadas à tomada de decisão.

---

## ⚡ Quick Start

Execute o projeto em poucos passos:

```bash
# 1. Clone o repositório
git clone https://github.com/seu-usuario/seu-repositorio.git
cd seu-repositorio

# 2. Instale as dependências
pip install pyspark pandas notebook

# 3. Inicie o Jupyter Notebook
jupyter notebook
```

Em seguida, abra o arquivo **`script.ipynb`** e execute todas as células sequencialmente.  
Os csv necessários (`PNAD_COVID_052020.csv`, `PNAD_COVID_062020.csv`, `PNAD_COVID_072020.csv`) já estarão disponíveis no repositório para fins do exercício.


---

## 🧠 Problema de Negócio

Dado um cenário de pandemia, um hospital precisa responder rapidamente a perguntas como:
- Quais sintomas se intensificam ao longo do tempo?
- Quais perfis populacionais demandam mais atendimento?
- Há diferenças significativas entre regiões?
- Como fatores socioeconômicos influenciam a busca por atendimento médico?

Este projeto responde a essas questões utilizando dados públicos e confiáveis do IBGE.

---

## 📊 Fonte de Dados

- **Base:** PNAD COVID-19 – IBGE  
- **Formato:** CSV (microdados)
- **Período:** 3 meses (conforme especificação do desafio)
- **Link oficial:** https://covid19.ibge.gov.br/pnad-covid/

⚠️ **Observação:** Os dados não estão versionados no repositório devido ao tamanho. O script espera que os arquivos estejam disponíveis localmente.


⚠️ **Observação para fins do exercício**

Para facilitar a reprodução deste projeto no contexto acadêmico e de portfólio, **os seguintes arquivos de dados serão disponibilizados neste repositório**:

- `PNAD_COVID_052020.csv`
- `PNAD_COVID_062020.csv`
- `PNAD_COVID_072020.csv`

Esses arquivos correspondem aos **três meses utilizados na análise**, conforme especificação do Tech Challenge, e permitem a execução completa do notebook sem necessidade de download adicional junto ao IBGE.


---

## 🗂️ Estrutura do Repositório

```
.
├── script.ipynb          # Notebook principal do projeto
├── README.md             # Documentação do projeto
```

---

## 🛠️ Tecnologias Utilizadas

- Python 3.9+
- PySpark
- Pandas
- SQL
- Jupyter Notebook
- Banco de Dados em Nuvem (modelo relacional)

---

## ⚙️ Pré-requisitos

- Python 3.9 ou superior  
- Java 8+ (necessário para PySpark)  
- Jupyter Notebook ou Jupyter Lab  

### Instalação de dependências
```bash
pip install pyspark pandas notebook
```

---

## ▶️ Como Executar o Projeto

### 1️⃣ Clonar o Repositório
```bash
git clone https://github.com/seu-usuario/seu-repositorio.git
cd seu-repositorio
```

### 2️⃣ Preparar os Dados
1. Faça o download dos microdados da PNAD COVID-19 no site do IBGE.
2. Extraia os arquivos CSV.
3. Ajuste no notebook `script.ipynb` o caminho para os dados.

Exemplo:
```python
path = "data/pnad_covid/"
```

### 3️⃣ Executar o Notebook
```bash
jupyter notebook
```
Abra o arquivo `script.ipynb` e execute as células sequencialmente.

---

## 🧱 Arquitetura da Solução

### Pipeline de Dados
1. Ingestão dos microdados (CSV)
2. Tratamento e seleção de variáveis
3. Modelagem dimensional (Star Schema)
4. Persistência em banco de dados
5. Consultas analíticas via SQL

### Modelagem Dimensional
- **Dimensões:** Tempo, Localização, Pessoa, Socioeconômica  
- **Fato:** Eventos relacionados à COVID-19

Diagrama do modelo:
https://dbdiagram.io/d/Tech_challenge_003-6959987239fa3db27b0755a7

---

## 🔎 Análises Implementadas

- Evolução temporal dos sintomas
- Relação entre atendimento médico e internação
- Distribuição etária dos casos
- Comparação entre capitais e interior

---

## 📈 Aplicação Prática

A solução fornece subsídios para:
- Planejamento de capacidade hospitalar
- Identificação de grupos de risco
- Definição de ações preventivas
- Expansão para dashboards e BI

---

## 📄 Referências

- IBGE – PNAD COVID-19  
- Tech Challenge – Pós-Tech Data Analytics - FIAP
