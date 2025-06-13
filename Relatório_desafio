Análise de Risco de Crédito para Prevenção de Inadimplência
🎯 Objetivo do Projeto
O objetivo deste projeto é desenvolver uma solução baseada em dados para reduzir as perdas financeiras de uma instituição, identificando os fatores que levam um mutuário à inadimplência. A análise se aprofunda em informações financeiras e de solicitação de empréstimo para encontrar padrões e construir um modelo de risco.

🛠️ Metodologia
O projeto foi estruturado em três etapas principais, desde a coleta e manipulação dos dados até a análise final e a extração de insights.

Etapa 1: Consolidação dos Dados com SQL
Os dados foram fornecidos em múltiplas tabelas. A primeira tarefa foi analisar a estrutura e as relações entre elas. Utilizando o MySQL, foi realizada a junção das tabelas para criar uma base de dados única e consolidada, pronta para a análise.

O comando SQL utilizado para esta etapa foi:

CREATE TABLE dados_juntos AS
SELECT
    dm.person_age,
    dm.person_income,
    dm.person_home_ownership,
    dm.person_emp_length,
    e.loan_intent,
    e.loan_grade,
    e.loan_amnt,
    e.loan_int_rate,
    e.loan_status,
    e.loan_percent_income,
    hb.cb_person_default_on_file,
    hb.cb_person_cred_hist_length
FROM ids i
JOIN dados_mutuarios dm ON dm.person_id = i.person_id
JOIN emprestimos e ON e.loan_id = i.loan_id
JOIN historicos_banco hb ON hb.cb_id = i.cb_id;

Etapa 2: Limpeza e Preparação dos Dados com Python
Com a base de dados unificada, o foco passou para a qualidade e organização dos dados. Utilizando a linguagem Python e bibliotecas como Pandas, foram executadas as seguintes tarefas:

Renomeação das Colunas: Tradução dos nomes para o português e padronização para facilitar a interpretação.

Tratamento de Valores Nulos: Identificação e tratamento de dados ausentes para garantir a integridade da análise.

Remoção de Outliers: Análise e tratamento de valores atípicos que poderiam distorcer os resultados dos modelos e das análises estatísticas.

Etapa 3: Análise Exploratória e Visualização de Dados
Nesta etapa final, com os dados devidamente tratados, foram utilizadas as bibliotecas Seaborn e Matplotlib para gerar visualizações e extrair insights sobre os fatores de risco.

📊 Análise de Insights e Conclusões
A seguir, são apresentados os principais gráficos e as conclusões obtidas a partir da análise dos dados.

1. Situação da Propriedade vs. Taxa de Inadimplência
Insight: A taxa de inadimplência é visivelmente maior para clientes que moram de aluguel. Isso sugere que a ausência de um imóvel próprio pode ser um indicador de menor estabilidade ou poder aquisitivo.

2. Motivo do Empréstimo vs. Taxa de Inadimplência
3. Taxa de Inadimplência por Pontuação de Crédito
Insight: Existe uma relação clara e crescente: quanto pior a pontuação de crédito (mais próximo de 'G'), maior a taxa de inadimplência. A pontuação é um dos preditores mais fortes de risco.

4. Mapa de Calor de Correlação
Insights Principais:

Taxa de Juros e Inadimplência: Há uma correlação positiva. Taxas de juros mais altas são oferecidas a clientes com maior risco percebido, que por sua vez, têm maior probabilidade de se tornarem inadimplentes.

Renda Anual e Inadimplência: Há uma correlação negativa. Clientes com maior renda anual apresentam menor chance de inadimplência, indicando maior capacidade de pagamento.

Renda Anual e Valor do Empréstimo: Clientes com maior renda tendem a solicitar (e receber aprovação para) empréstimos de maior valor.
