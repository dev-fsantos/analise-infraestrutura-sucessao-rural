# 🌱 Diagnóstico Socioambiental e Sucessão Rural — Comunidade de São Roque

Análise exploratória de dados (EDA) focada na identificação de gargalos socioambientais, infraestrutura e fatores determinantes para a sucessão rural na comunidade de São Roque. O estudo analisa dados de **28 famílias**, representando uma amostra altamente expressiva de **~47%** de toda a comunidade local.

---

## 📋 Sumário

- [Contexto do Projeto](#-contexto-do-projeto)
- [Metodologia e ETL](#-metodologia-e-etl-tratamento-de-dados)
- [Principais Insights e Resultados](#-principais-insights-e-resultados)
- [Estrutura do Repositório](#-estrutura-do-repositório)
- [Como Reproduzir este Projeto](#-como-reproduzir-este-projeto)
- [Tecnologias Utilizadas](#-tecnologias-utilizadas)

---

## 🎯 Contexto do Projeto

A continuidade da agricultura familiar enfrenta desafios estruturais associados ao êxodo rural dos jovens e à falta de infraestrutura básica nas propriedades. Este projeto foi desenvolvido para mapear a realidade socioeconômica de São Roque, investigando como a qualidade da conexão de internet e a segurança hídrica (coleta de água da chuva) influenciam diretamente a perspectiva de sucessão rural.

### Objetivos Principais

- Quantificar a taxa de retenção/sucessão familiar nas propriedades rurais.
- Correlacionar o acesso à conectividade digital com a permanência dos jovens no campo.
- Avaliar o impacto da perspectiva de futuro no investimento em infraestrutura sustentável e resiliência hídrica.
- Fornecer diagnósticos baseados em dados para orientação de políticas públicas e projetos de desenvolvimento comunitário.

---

## 🔧 Metodologia e ETL (Tratamento de Dados)

Os dados brutos coletados em campo passaram por um fluxo robusto de higienização e tratamento em Python (`pandas`), superando inconsistências de codificação e estruturação de planilhas locais:

- **Tratamento de Codificação e Separadores:** correção de erros de decodificação de texto ajustando o parâmetro de leitura para `encoding='latin1'` e separador de colunas `sep=';'`.
- **Higienização de Estrutura:** remoção automatizada de colunas residuais e nulas (`Unnamed`), padronização da nomenclatura das colunas para eliminação de ambiguidades de sintaxe.
- **Análise Estatística e Visual:** cruzamento de variáveis categóricas bivariadas (`pd.crosstab`) e geração de visualizações empilhadas utilizando `seaborn` e `matplotlib`.

---

## 📊 Principais Insights e Resultados

### Diagnóstico Geral da Amostra (28 Famílias)

| Indicador | Categoria | Percentual / Proporção |
|---|---|---|
| Perspectiva de Sucessão Rural | Sim / Não | 57,14% (Sim) \| 42,86% (Não) |
| Infraestrutura Hídrica | Captação de Água | 17,86% possuem captação sustentável |
| Conectividade Digital | Qualidade Satisfatória | 60,71% (avaliada como Bom ou Ótimo) |

### 1. Conectividade Digital vs. Sucessão Rural

- **100%** das famílias com perspectiva de sucessão possuem acesso à internet classificado de forma positiva (75% "Bom" e 25% "Regular"). Nenhuma propriedade com sucessor declarou ter conexão "Ruim".
- **75%** das famílias sem sucessores enfrentam forte insatisfação com a conectividade (33,3% "Ruim" e 41,7% "Regular").

> **Conclusão:** o isolamento digital atua como um vetor direto de desestímulo à permanência das novas gerações no campo, limitando o acesso à educação, lazer e modernização da gestão agrícola.

### 2. Segurança Hídrica vs. Sucessão Rural

- **100%** das famílias sem perspectiva de sucessão não possuem sistemas de captação de água da chuva.
- **31,25%** das propriedades com sucessão garantida já possuem infraestrutura de coleta instalada.

> **Conclusão:** o horizonte temporal da propriedade determina a decisão de investimento. Na ausência de herdeiros, o produtor evita aportes financeiros em infraestruturas de longo prazo, gerando um ciclo vicioso de vulnerabilidade produtiva frente a eventos climáticos.

---

## 📁 Estrutura do Repositório

```
├── dados/
│   ├── dados_analise.csv             # Base de dados tratada
│   └── grafico_analise_bivariada.png # Gráficos exportados para apresentação
├── notebooks/
│   └── eda_sao_roque.ipynb           # Notebook Jupyter com o código da análise
├── .gitignore                        # Arquivos ignorados pelo versionamento
├── README.md                         # Documentação principal do projeto
└── requirements.txt                  # Dependências das bibliotecas Python
```

---

## 🚀 Como Reproduzir este Projeto

### Pré-requisitos

- Python 3.10 ou superior instalado
- VS Code ou Jupyter Notebook

### Passo a Passo

**1. Clonar o repositório**

```bash
git clone https://github.com/seu-usuario/seu-repositorio.git
cd seu-repositorio
```

**2. Criar e ativar um ambiente virtual** (opcional, mas recomendado)

```bash
python -m venv venv

# No Windows:
venv\Scripts\activate

# No Linux/Mac:
source venv/bin/activate
```

**3. Instalar as dependências**

```bash
pip install -r requirements.txt
```

**4. Executar a análise**

Abra o arquivo `notebooks/eda_sao_roque.ipynb` no seu ambiente Jupyter e execute as células sequencialmente.

---

## 🛠️ Tecnologias Utilizadas

| Tecnologia | Finalidade |
|---|---|
| **Python** | Linguagem base para manipulação e análise de dados |
| **Pandas** | Limpeza, transformação (ETL) e agregação bivariada |
| **Matplotlib & Seaborn** | Construção de gráficos estatísticos e personalização visual |
| **Git & GitHub** | Versionamento de código e documentação |

---

<p align="center">Desenvolvido com foco em dados para impacto social e desenvolvimento rural sustentável 🌾</p>
