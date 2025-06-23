Análise de Evasão de Clientes (Churn) de uma Empresa de Telecom
📝 Visão Geral do Projeto
Este repositório contém uma análise exploratória de dados (AED) completa sobre um conjunto de dados de clientes de uma empresa de telecomunicações. O objetivo principal é investigar os fatores que influenciam a evasão de clientes (conhecida como "Churn") e, a partir dos insights gerados, construir um perfil claro do cliente com maior risco de cancelar o serviço.

🎯 O Problema de Negócio
A evasão de clientes é um dos principais desafios para empresas de serviços baseados em assinatura. Adquirir novos clientes é muito mais caro do que reter os existentes. Portanto, entender por que e quando os clientes saem é fundamental para direcionar ações estratégicas de retenção, marketing e desenvolvimento de produtos, visando aumentar a lealdade e a lucratividade da empresa.

💾 Sobre o Dataset
O conjunto de dados utilizado, TelecomX_Data.json, é um arquivo em formato JSON que contém informações demográficas, detalhes dos serviços contratados e dados da conta de cada cliente. As principais categorias de dados incluem:

Dados do Cliente: gênero, se é idoso, se possui parceiro(a) ou dependentes.
Serviços Contratados: plano de telefone, múltiplas linhas, tipo de serviço de internet, e serviços adicionais (segurança online, backup, etc.).
Informações da Conta: tempo de contrato (tenure), tipo de contrato, forma de pagamento, faturamento mensal e total.
Variável Alvo: Churn (indica se o cliente cancelou o serviço ou não).
🛠️ Metodologia Aplicada
A análise foi estruturada seguindo as melhores práticas de um projeto de Data Science, abrangendo as seguintes etapas:

Carregamento e Limpeza de Dados:

Carregamento do arquivo JSON aninhado e sua conversão para um DataFrame tabular do pandas.
Tratamento de tipos de dados (ex: conversão da cobrança total para formato numérico).
Identificação e remoção de dados ausentes ou inconsistentes na variável alvo (Churn).
Verificação de dados duplicados.
Análise Exploratória de Dados (AED):

Cálculo de estatísticas descritivas para entender as distribuições das variáveis numéricas e categóricas.
Criação de visualizações (gráficos de pizza, barras, histogramas e boxplots) para identificar a relação entre cada variável e a taxa de evasão.
Engenharia de Features:

Criação da variável Contas_Diarias para fornecer uma visão normalizada dos custos.
Pré-processamento para Modelagem:

Transformação de variáveis categóricas em formato numérico através de mapeamento binário e One-Hot Encoding, preparando o terreno para a aplicação de algoritmos de Machine Learning.
📊 Principais Insights e Constatações
A análise revelou padrões claros que definem o comportamento de evasão:

Taxa de Evasão Geral: Cerca de 26,5% dos clientes na base de dados cancelaram o serviço.
Fatores de Maior Impacto no Churn:
Tipo de Contrato: Clientes com contrato mensal são drasticamente mais propensos a cancelar.
Tempo de Contrato (Tenure): A evasão é massivamente concentrada em clientes novos (principalmente com menos de 10 meses).
Cobrança Mensal: Contas mensais elevadas (associadas a planos de Fibra Óptica) correlacionam-se fortemente com um maior risco de churn.
Método de Pagamento: Clientes que pagam com cheque eletrônico têm uma taxa de cancelamento significativamente maior.
Suporte Técnico: A ausência de um plano de suporte técnico aumenta a probabilidade de evasão.
Perfil do Cliente com Alto Risco de Evasão
O cliente mais propenso a cancelar é novo, possui um contrato mensal, paga uma fatura elevada (geralmente por um serviço de fibra óptica), utiliza cheque eletrônico como forma de pagamento e não tem suporte técnico contratado.

🚀 Ferramentas Utilizadas
Linguagem: Python 3
Bibliotecas: pandas para manipulação de dados, matplotlib e seaborn para visualização de dados.
Ambiente: A análise foi desenvolvida em um ambiente de notebook, como o Google Colab ou Jupyter Notebook.
⚙️ Como Executar o Projeto
Para reproduzir esta análise, siga os passos abaixo:

Clone o repositório:

Bash

git clone https://github.com/johnatandin/desafio-telecomX/
cd nome-do-repositorio
Crie um ambiente virtual (recomendado):

Bash

python -m venv venv
source venv/bin/activate  # No Windows: venv\Scripts\activate
Instale as dependências:

Bash

pip install pandas matplotlib seaborn
(Você pode também criar um arquivo requirements.txt com o conteúdo das bibliotecas para facilitar a instalação)

Execute o Notebook:

Abra o notebook principal do projeto (ex: analise_churn.ipynb) em um ambiente como Jupyter ou Google Colab.
Certifique-se de que o arquivo TelecomX_Data.json esteja no mesmo diretório.
Execute as células do notebook em ordem.
📁 Estrutura do Repositório (Sugestão)
.
├── TelecomX_Data.json         # O conjunto de dados original
├── analise_churn.ipynb        # Notebook com toda a análise passo a passo
├── README.md                  # Este arquivo
└── requirements.txt           # Lista de bibliotecas Python para instalar
