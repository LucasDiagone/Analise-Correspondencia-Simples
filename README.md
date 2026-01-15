📊 Análise de Correspondência Simples (ANACOR)
==============================================

Este repositório apresenta um estudo completo de **Análise de Correspondência Simples (ANACOR)** aplicado a dados categóricos de **perfil de investimento** e **tipo de aplicação financeira**, com foco no entendimento conceitual do método, sua aplicação prática em Python e a interpretação estatística dos resultados.

* * *

🎯 Objetivo do Projeto
----------------------

O objetivo deste projeto é:

* 🔗 Identificar associações entre categorias de variáveis categóricas
* 🧠 Evidenciar padrões de comportamento presentes nos dados
* 👥 Revelar quais categorias tendem a se associar entre si, mais do que o esperado sob a hipótese de independência

A ANACOR é utilizada como uma ferramenta exploratória, voltada para a compreensão de relacionamentos entre categorias e apoio à tomada de decisão.

* * *

📦 Bibliotecas Utilizadas
-------------------------

pip install pandas numpy scipy statsmodels seaborn matplotlib prince

Principais bibliotecas utilizadas:

* pandas, numpy → manipulação de dados
* scipy → teste qui-quadrado
* statsmodels → resíduos padronizados ajustados
* seaborn, matplotlib → visualizações
* prince → Análise de Correspondência

* * *

🔍 Metodologia
--------------

O fluxo da análise seguiu as etapas abaixo:

1️⃣ Análise Exploratória (EDA)

* Leitura da base de dados
* Análise das frequências das variáveis categóricas
* Construção da tabela de contingência (crosstab)

* * *

2️⃣ Teste Qui-quadrado de Independência

* Verificação da existência de associação global entre as variáveis
* Cálculo dos valores esperados sob a hipótese de independência

O teste qui-quadrado justifica estatisticamente a aplicação da ANACOR.

* * *

3️⃣ Resíduos Padronizados Ajustados

* Cálculo dos resíduos padronizados ajustados
* Identificação das combinações de categorias com associação estatisticamente significativa

Regra utilizada:

|resíduo| > 1,96 → associação estatisticamente significativa (α = 5%)

Também foi utilizado um mapa de calor para facilitar a interpretação célula a célula.

* * *

4️⃣ Análise de Correspondência Simples (ANACOR)

* Ajuste do modelo de ANACOR à tabela de contingência
* Decomposição da associação em dimensões ortogonais
* Cálculo dos autovalores, que indicam a importância de cada dimensão

A Dimensão 1 concentrou a maior parte da associação total.

* * *

5️⃣ Mapa Percentual da ANACOR

* Representação gráfica das categorias no plano Dimensão 1 × Dimensão 2
* Interpretação baseada em:
  - Distância ao centro → contribuição para a associação
  - Proximidade entre pontos → associação entre categorias

* * *

📊 Principais Resultados
------------------------

Os resíduos padronizados ajustados indicaram associações estatisticamente significativas, destacando-se:

* Perfil agressivo ↔ Ações
* Perfil conservador ↔ Poupança
* Perfil moderado ↔ CDB

Também foram observadas associações negativas (evitação) entre perfis e aplicações de natureza oposta.

Esses resultados foram confirmados e organizados visualmente pelo mapa da Análise de Correspondência.

* * *

🧠 Interpretação Conceitual
---------------------------

* Valores esperados representam as frequências sob independência e servem como base de comparação
* Resíduos medem o desvio entre valores observados e esperados
* Dimensões são vetores que indicam as principais direções de associação
* Autovalores medem a força de cada dimensão na explicação da associação total

No mapa:

* Dimensão 1 → eixo X (principal padrão de associação)
* Dimensão 2 → eixo Y (padrão secundário)

* * *

✅ Conclusão
-----------

A Análise de Correspondência Simples mostrou-se adequada para investigar associações entre perfis de investimento e tipos de aplicação financeira. O teste qui-quadrado confirmou a dependência entre as variáveis, enquanto os resíduos padronizados ajustados permitiram identificar objetivamente as associações estatisticamente significativas.

A representação gráfica por meio do mapa percentual possibilitou visualizar a estrutura relacional entre as categorias, evidenciando que a maior parte da associação está concentrada na primeira dimensão. Os resultados são coerentes com a teoria financeira e demonstram o potencial da ANACOR como ferramenta exploratória para análise de comportamento, apoio à tomada de decisão e base para estudos posteriores.

* * *
