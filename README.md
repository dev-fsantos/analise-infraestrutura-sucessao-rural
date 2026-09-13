# 🌱 Diagnóstico Socioambiental e Sucessão Rural — Comunidade de São Roque

Análise exploratória de dados (EDA) sobre aspectos socioambientais, infraestrutura e sucessão rural na comunidade de São Roque.

O estudo utiliza dados coletados de **28 famílias**, correspondendo a aproximadamente **47% das famílias da comunidade**, para investigar possíveis associações entre a perspectiva de sucessão rural, conectividade digital e infraestrutura de captação de água da chuva.

> **Nota:** este é um estudo exploratório e observacional. As associações identificadas não permitem estabelecer relações de causalidade.

---

## 📋 Sumário

* [Contexto](#-contexto)
* [Objetivos](#-objetivos)
* [Dados](#-dados)
* [Metodologia](#-metodologia)
* [Principais resultados](#-principais-resultados)
* [Limitações](#-limitações)
* [Estrutura do repositório](#-estrutura-do-repositório)
* [Como reproduzir](#-como-reproduzir)
* [Tecnologias utilizadas](#-tecnologias-utilizadas)

---

## 🎯 Contexto

A sucessão rural é um dos desafios enfrentados pela agricultura familiar, especialmente diante das transformações sociais, econômicas e tecnológicas que afetam a permanência das novas gerações no campo.

A partir dessa problemática, este projeto busca explorar a realidade de famílias da comunidade de São Roque, observando a relação entre:

* perspectiva de sucessão familiar;
* qualidade da conexão com a internet;
* presença de sistemas de captação de água da chuva.

A proposta é utilizar dados locais para identificar **padrões e possíveis relações que possam orientar investigações futuras e iniciativas de desenvolvimento rural**.

---

## 🎯 Objetivos

### Objetivo geral

Realizar uma análise exploratória dos dados socioambientais da comunidade de São Roque, buscando identificar padrões relacionados à sucessão rural e à infraestrutura das propriedades.

### Objetivos específicos

* Quantificar a proporção de famílias com e sem perspectiva de sucessão;
* Analisar a distribuição da qualidade da conexão com a internet;
* Verificar a presença de sistemas de captação de água da chuva;
* Explorar a associação entre conectividade e perspectiva de sucessão;
* Explorar a associação entre infraestrutura hídrica e perspectiva de sucessão;
* Identificar possíveis hipóteses para estudos posteriores.

---

## 📊 Dados

A análise foi realizada a partir de dados coletados junto a **28 famílias da comunidade de São Roque**.

A amostra corresponde a aproximadamente **47% das famílias da comunidade**, proporcionando uma visão relevante da realidade local, embora os resultados devam ser interpretados dentro dos limites da amostra estudada.

Entre as variáveis analisadas estão:

| Variável                              | Tipo               |
| ------------------------------------- | ------------------ |
| Perspectiva de sucessão rural         | Categórica         |
| Qualidade da conexão com a internet   | Categórica ordinal |
| Presença de captação de água da chuva | Categórica binária |

Os dados utilizados na análise foram tratados antes da etapa exploratória.

---

## 🔧 Metodologia

O projeto foi desenvolvido seguindo um fluxo de **ETL + Análise Exploratória de Dados (EDA)**.

### 1. Importação e tratamento dos dados

Os dados foram originalmente obtidos em uma planilha com características comuns a bases coletadas localmente.

Durante o processo de preparação foram realizados:

* ajuste da codificação dos caracteres (`latin1`);
* definição do separador utilizado pela planilha (`;`);
* remoção de colunas residuais, como `Unnamed`;
* padronização dos nomes das colunas;
* organização das variáveis para análise.

### 2. Análise exploratória

Após a limpeza, foram realizadas análises descritivas e cruzamentos entre variáveis categóricas.

Para investigar possíveis associações foram utilizados recursos como:

```python
pd.crosstab()
```

Os resultados foram posteriormente transformados em visualizações para facilitar a interpretação dos padrões encontrados.

### 3. Visualização

Foram utilizados:

* **Matplotlib**
* **Seaborn**

principalmente para construção de gráficos de distribuição e cruzamentos bivariados.

---

## 📈 Principais resultados

### 1. Panorama geral da amostra

Entre as 28 famílias analisadas:

| Indicador                                            |  Resultado |
| ---------------------------------------------------- | ---------: |
| Famílias com perspectiva de sucessão                 | **57,14%** |
| Famílias sem perspectiva de sucessão                 | **42,86%** |
| Famílias com captação de água da chuva               | **17,86%** |
| Famílias com internet classificada como Bom ou Ótimo | **60,71%** |

Os resultados representam exclusivamente a amostra analisada.

---

### 2. Conectividade × sucessão rural

O cruzamento entre a perspectiva de sucessão e a qualidade da conexão apresentou diferenças entre os grupos analisados.

Entre as famílias que declararam possuir perspectiva de sucessão, **não foram observadas classificações de conexão como "Ruim"** na amostra analisada.

Entre as famílias sem perspectiva de sucessão, houve uma maior concentração de avaliações **"Regular" e "Ruim"**.

Esse padrão sugere uma possível associação entre **conectividade digital e perspectiva de sucessão rural**.

Entretanto, os dados não permitem afirmar que a qualidade da internet seja responsável pela permanência ou saída das novas gerações.

Outros fatores — econômicos, familiares, educacionais, produtivos e estruturais — também podem influenciar essa decisão.

---

### 3. Captação de água da chuva × sucessão rural

Também foi observada diferença na presença de sistemas de captação de água da chuva entre os grupos.

Na amostra analisada:

* **100% das famílias sem perspectiva de sucessão não possuíam sistema de captação de água da chuva**;
* entre as famílias com perspectiva de sucessão, **31,25% possuíam esse tipo de infraestrutura**.

O resultado indica uma possível associação entre **perspectiva de continuidade da propriedade e realização de investimentos em infraestrutura hídrica**.

Uma possível hipótese para estudos futuros é investigar se famílias que esperam manter a propriedade por períodos mais longos apresentam maior propensão a realizar investimentos estruturais.

Novamente, essa relação não deve ser interpretada como causal com base apenas nesta análise.

---

## ⚠️ Limitações

Algumas limitações devem ser consideradas na interpretação dos resultados:

* a análise utiliza uma amostra de **28 famílias**;
* trata-se de um estudo **observacional e exploratório**;
* associações encontradas não demonstram causalidade;
* a forma de seleção das famílias pode introduzir viés de amostragem;
* variáveis não analisadas podem influenciar os resultados;
* os resultados não devem ser generalizados automaticamente para outras comunidades rurais.

Apesar dessas limitações, a base possui valor para **diagnóstico exploratório local e geração de hipóteses para estudos posteriores**.

---

## 🔎 Possíveis análises futuras

A base pode ser expandida com outras variáveis para investigar a sucessão rural de maneira mais abrangente.

Algumas possibilidades incluem:

* idade dos possíveis sucessores;
* escolaridade;
* tamanho da propriedade;
* atividade agrícola principal;
* renda;
* acesso a tecnologias;
* mecanização;
* infraestrutura produtiva;
* distância até centros urbanos;
* acesso a serviços públicos;
* histórico de permanência dos jovens na propriedade.

Com uma base maior, também seria possível aplicar métodos estatísticos mais robustos para avaliar a significância das associações observadas.

---

## 📁 Estrutura do repositório

```text
├── dados/
│   ├── dados_analise.csv
│   └── grafico_analise_bivariada.png
│
├── notebooks/
│   └── eda_sao_roque.ipynb
│
├── .gitignore
├── README.md
└── requirements.txt
```

### Descrição

**`dados/`**
Contém a base tratada utilizada na análise e os gráficos exportados.

**`notebooks/`**
Contém o notebook Jupyter com as etapas de tratamento, exploração e visualização dos dados.

**`requirements.txt`**
Lista as bibliotecas necessárias para reprodução do projeto.

---

## 🚀 Como reproduzir

### Pré-requisitos

* Python 3.10 ou superior;
* VS Code ou Jupyter Notebook;
* Git.

### 1. Clone o repositório

```bash
git clone https://github.com/seu-usuario/seu-repositorio.git

cd seu-repositorio
```

### 2. Crie um ambiente virtual

```bash
python -m venv venv
```

No Windows:

```bash
venv\Scripts\activate
```

No Linux/macOS:

```bash
source venv/bin/activate
```

### 3. Instale as dependências

```bash
pip install -r requirements.txt
```

### 4. Execute a análise

Abra:

```text
notebooks/eda_sao_roque.ipynb
```

no VS Code ou Jupyter Notebook e execute as células sequencialmente.

---

## 🛠️ Tecnologias utilizadas

| Tecnologia           | Finalidade                                 |
| -------------------- | ------------------------------------------ |
| **Python**           | Linguagem utilizada no projeto             |
| **Pandas**           | Limpeza, transformação e análise dos dados |
| **Matplotlib**       | Visualização de dados                      |
| **Seaborn**          | Visualização estatística                   |
| **Jupyter Notebook** | Desenvolvimento e documentação da análise  |
| **Git**              | Versionamento                              |
| **GitHub**           | Hospedagem e documentação do projeto       |

---

## 📌 Conclusão

A análise exploratória identificou diferenças relevantes entre famílias com e sem perspectiva de sucessão, especialmente nos indicadores relacionados à **conectividade digital** e à **infraestrutura de captação de água da chuva**.

Os resultados não permitem determinar relações de causa e efeito, mas apontam **padrões e hipóteses que podem ser investigados em estudos posteriores**, especialmente com uma base de dados maior e um conjunto mais amplo de variáveis socioeconômicas e produtivas.

O projeto demonstra a aplicação de técnicas de **ETL, análise exploratória e visualização de dados em um problema real**, utilizando dados coletados em uma comunidade rural.

---

<p align="center">
  Desenvolvido com foco em análise de dados aplicada ao contexto rural 🌱📊
</p>
