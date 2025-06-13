# Challenge Dados - Relatório

## Introdução

O objetivo é encontrar uma solução para que seja possível diminuir as perdas financeiras por conta de pessoas mutuárias que não quitam suas dívidas.  
Como cientista de dados, você sugere um estudo das informações financeiras e de solicitação de empréstimo para encontrar padrões que possam indicar uma possível inadimplência.

---

## Organização e renomeação das tabelas

Foi feita a junção das tabelas e renomeação de cada coluna, traduzindo para português e escolhendo um nome que simplifica o entendimento do que o valor daquela coluna representa.

---

## Limpeza de valores nulos e outliers

A partir de uma série de comandos foi verificado quais colunas haviam valores nulos e outliers, e esses foram removidos.

---

## Análise e insights obtidos

Foi feita a geração dos seguintes gráficos e insights com as informações ilustradas:

Avaliando a correlação dos valores de cada coluna foi possível obter conclusões relevantes.

---

## ETAPA 1 - Manipulação dos dados

Foi fornecido um conjunto de dados divididos em tabelas.  
Primeiramente, realizei a análise para avaliar do que se tratava cada uma.  
Identifiquei que uma das tabelas relacionava as informações contidas nas outras, então, utilizando **MySQL**, realizei a junção das tabelas com base na relação entre elas.

---

## ETAPA 2 - Limpeza e Organização

Utilizando o **Python**, foi feita a renomeação das tabelas, remoção de valores nulos e outliers.  
Mais detalhes podem ser visualizados no arquivo anexado no repositório.

---

## ETAPA 3 - Análise e criação de gráficos

Com a base de dados tratada e organizada, utilizando o **Python**:

- Calculamos a **correlação** entre as variáveis.
- Geramos **gráficos** para melhor interpretação dos dados e descoberta de padrões.

---

### Observações e Insights:

- **(Inadimplência x Aluguel)**  
  Faz sentido a maior taxa de inadimplência estar relacionada ao aluguel, pois quem não é dono de uma propriedade geralmente não tem tanto poder aquisitivo.

- **(Inadimplência x Taxa de juros)**  
  Uma taxa de juros mais alta geralmente está associada a um maior risco percebido por parte da instituição, o que também pode refletir uma maior chance de inadimplência.

- **(Inadimplência x Renda anual)**  
  Quanto maior a renda da pessoa, menor é a chance dela ser inadimplente.

- **(Valor total do empréstimo x Renda anual)**  
  Quanto maior a renda, maior tende a ser o valor de crédito oferecido.
"""
