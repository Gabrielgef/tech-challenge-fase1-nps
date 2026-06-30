# Tech Challenge NPS Preditivo

<a target="_blank" href="https://cookiecutter-data-science.drivendata.org/">
    <img src="https://img.shields.io/badge/CCDS-Project%20template-328F97?logo=cookiecutter" />
</a>

Analise de case de NPS para o Tech Challenge da Fase 1

## 👥 Integrantes do Grupo
* [Gabriel Enrique Ferreira](https://github.com/Gabrielgef)
* [Guilherme Ramos Cordeiro](https://github.com/Guicordram)
* [Matheus Reis](https://github.com/mkonigen)
* [André Vinicius Barros Santos](https://github.com/andrestos-20)

# Tech Challenge Fase 1 - Case NPS Preditivo

Este repositório contém a entrega da Fase 1 do Tech Challenge, cujo foco é a análise de dados operacionais de um e-commerce para entender as alavancas de satisfação do cliente e a construção de um modelo preditivo de Net Promoter Score (NPS).

## 🎯 Objetivo do Projeto
Com o crescimento acelerado do volume de pedidos e entregas, a área de Experiência do Cliente identificou uma alta variabilidade no NPS. O objetivo deste projeto é responder à questão central do negócio: **quais fatores operacionais realmente influenciam a satisfação do cliente?** Além de diagnosticar o cenário atual através de dados, o projeto entrega um modelo preditivo capaz de antecipar a classificação do cliente (Promotor, Neutro ou Detrator) antes da aplicação da pesquisa. Isso permite à operação atuar de forma proativa na mitigação de atritos (como atrasos logísticos ou problemas de atendimento) e na recuperação de clientes em risco.

## 📊 Descrição da Base de Dados
Os dados utilizados representam a operação de um e-commerce e as interações na jornada de compra do consumidor. A base consolida informações de diferentes etapas da esteira, incluindo:
* **Dados Demográficos/Cliente:** Informações de perfil (ex: idade).
* **Dados Operacionais e Logísticos:** Histórico de pedidos, tempos de entrega e eventuais atrasos.
* **Dados de Atendimento:** Volume de contatos com o suporte, esforço do cliente e notas de CSAT (Customer Satisfaction Score).
* **Variável Alvo (Target):** A nota final de NPS e a classificação do cliente em Detrator, Neutro ou Promotor.

## 🔬 Metodologia Utilizada
O projeto foi desenvolvido seguindo as etapas clássicas de Ciência de Dados, com forte foco em resolver o problema de negócio:

1. **Pré-processamento de Dados:** Limpeza de valores nulos e transformação de variáveis categóricas (One-Hot Encoding) para adequação aos algoritmos matemáticos.
2. **Análise Exploratória de Dados (EDA):** Teste de hipóteses para isolar as variáveis que mais impactam o NPS. Foram analisadas correlações entre fatores demográficos, fricções operacionais (como atrasos na entrega) e a percepção final do cliente.
3. **Modelagem Preditiva de Classificação:** Foram treinados e testados diferentes algoritmos de Machine Learning (Regressão Logística, Random Forest e Gradient Boosting).
4. **Avaliação e Escolha do Modelo:** O modelo **Gradient Boosting** foi selecionado como vencedor. A decisão foi baseada em critérios de negócio, priorizando a métrica de *Recall* para a classe de "Detratores" (96,2%), garantindo que a empresa identifique a esmagadora maioria dos clientes insatisfeitos para ações de retenção.

## 🗂️ Estrutura do Projeto

```
├── LICENSE            <- Licença Open-source
├── README.md          <- Apresentação do projeto, metodologia e instruções.
├── data
│   ├── processed      <- Dados limpos e transformados prontos para modelagem.
│   └── raw            <- Base de dados original (ex: dataset_nps.csv).
│
├── models             <- Modelos treinados e exportados (ex: modelo_predicao_detrator_nps.pkl)
│
├── notebooks          <- Jupyter notebooks contendo a experimentação.
│   ├── 01-analise-exploratoria.ipynb      <- Análise exploratória, testes de hipóteses e gráficos.
│   └── 02-modelagem-e-avaliacao.ipynb     <- Pré-processamento, treinamento e escolha do modelo preditivo.
│
├── pyproject.toml     <- Arquivo de configuração do projeto contendo metadados do pacote
│                         tech_challenge_nps_preditivo e configurações para ferramentas de desenvolvimento como o black
│
├── reports            <- Resumos de dados utlizados para a apresentação.
│
├── environment.yml     <- Arquivo para recriar o ambiente conda da análise.
│
└──  setup.cfg          <- Configuração de arquivo para o flake8

```
## Videos explicativo da análise exploratória e modelo preditivo

https://youtu.be/h7PDhohgeQs

--------

## 🚀 Como Reproduzir os Resultados

Para garantir a reprodutibilidade sem conflitos de dependências, o projeto utiliza o gerenciador de ambientes `conda`. Siga os passos abaixo:

1. **Clone o repositório**
    ```bash
    git clone https://github.com/SEU-USUARIO/tech-challenge-fase1-nps.git
    cd tech-challenge-fase1-nps
    ```

2. **Crie o ambiente virtual a partir do arquivo de configuração**
    ```bash
    conda env create -f environment.yml
    ```

3. **Ative o ambiente**
    ```bash
    conda activate tech-challenge-fase1-nps
    ```

4. **Execute os notebooks**
    Abra o Jupyter Notebook ou o VS Code e navegue até a pasta `notebooks/`. Execute os arquivos `.ipynb` na ordem cronológica.
