# 📊 Tratativa e Análise de Dados de CNPJ — Dezembro/2025
![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python&logoColor=white)
![Apache Spark](https://img.shields.io/badge/Apache%20Spark-4.1-orange?logo=apachespark&logoColor=white)
![Delta Lake](https://img.shields.io/badge/Delta%20Lake-4.0-blueviolet)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-Ubuntu-E95420?logo=ubuntu&logoColor=white)
![Data Engineering](https://img.shields.io/badge/Data-Engineering-success)
![Public Data](https://img.shields.io/badge/Data-Public%20Dataset-informational)
![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)
![Status](https://img.shields.io/badge/Status-Em%20Desenvolvimento-yellow)

Projeto dedicado à **coleta, organização, tratamento e análise** dos dados públicos de **CNPJ (Cadastro Nacional da Pessoa Jurídica)** referentes a **dezembro de 2025**, disponibilizados pelo portal **dados.gov.br**.

O objetivo principal é estruturar os dados brutos, realizar tratativas e possibilitar a geração de **insights analíticos** sobre empresas brasileiras, como natureza jurídica, porte, localização, CNAE, regime do Simples Nacional, sócios, entre outros.

---

## 🧠 Objetivos do Projeto

- Coletar dados públicos de CNPJ no padrão oficial
- Organizar os arquivos em uma estrutura clara (RAW → TRS)
- Realizar tratamento e padronização dos dados
- Preparar o dataset para análises exploratórias e futuras visualizações
- Servir como base para estudos, dashboards e pipelines de dados

---

## 🗂️ Estrutura do Projeto

```text
CNPJ_12-2025/
├── .venv/                     # Ambiente virtual Python
├── LND/                       # Camada de landing (dados organizados por domínio)
│   ├── cnaes/
│   ├── empresas/
│   ├── estabelecimentos/
│   ├── logs/
│   ├── motivos/
│   ├── municipios/
│   ├── naturezas/
│   ├── paises/
│   ├── qualificacoes/
│   ├── simples/
│   └── socios/
│
├── notebooks/
│   ├── 01_NOTEBOOKS_RAW/      # Tratativa inicial dos dados brutos
│   │   ├── 01_socios.ipynb
│   │   ├── 02_simples.ipynb
│   │   ├── 03_paises.ipynb
│   │   ├── 04_qualificacoes.ipynb
│   │   ├── 05_naturezas.ipynb
│   │   ├── 06_municipios.ipynb
│   │   ├── 07_motivos.ipynb
│   │   ├── 08_estabelecimentos.ipynb
│   │   ├── 09_empresas.ipynb
│   │   └── 10_cnaes.ipynb
│   │
│   ├── 02_NOTEBOOKS_TRS/      # Transformações e consolidações
│   │   ├── 01_socios.ipynb
│   │   ├── 02_simples.ipynb
│   │   ├── 03_paises.ipynb
│   │   ├── 04_qualificacoes.ipynb
│   │   ├── 05_naturezas.ipynb
│   │   ├── 06_municipios.ipynb
│   │   ├── 07_motivos.ipynb
│   │   ├── 08_estabelecimentos.ipynb
│   │   ├── 09_empresas.ipynb
│   │   └── 10_cnaes.ipynb
│   └── 01_coleta_dados.ipynb
│
├── RAW/                       # Dados brutos, sem tratamento
│   ├── cnae/
│   ├── empresas/
│   ├── estabelecimentos/
│   ├── motivos/
│   ├── municipios/
│   ├── naturezas/
│   ├── paises/
│   ├── qualificacoes/
│   ├── simples/
│   └── socios/
│
├── TRS/                       # Dados tratados e prontos para análise
│
├── README.md
└── requirements.txt
```

## 🛠️ Tecnologias Utilizadas

- Python 3
- Jupyter Notebook / JupyterLab
- Apache Spark (PySpark)
- Delta Lake (delta-spark)
- Requests (coleta de dados via HTTP)
- WSL + Ubuntu (ambiente de desenvolvimento)
> O uso do Spark permite escalabilidade e processamento eficiente de grandes volumes de dados.

---

## 📦 Instalação do Ambiente

1️⃣ Crie e ative um ambiente virtual (opcional, mas altamente recomendado)
```bash
python -m venv .venv
source .venv/bin/activate  # Linux / WSL
```
2️⃣ Instale as dependências

```bash
pip install -r requirements.txt
```
## 📑 Principais Dependências
Algumas bibliotecas-chave utilizadas no projeto:
- ``pyspark==4.1.1``
- ``delta-spark==4.0.0``
- ``requests==2.32.5``
- ``jupyterlab==4.5.1``
- ``ipykernel==7.1.0``
> A lista completa está disponível no arquivo ``requirements.txt``.

---
## 📄 Licença

Este projeto utiliza dados públicos, sendo destinado a fins educacionais, analíticos e experimentais.

## ✍️ Autor

Desenvolvido por Williams
Foco em Engenharia de Dados, Python e Banco de Dados
