# Capítulo 4 - Entendendo o Processo de Qualidade de Software

Não é possível conceber um processo de garantia da qualidade de software sem integrá-lo com o ciclo de desenvolvimento de software. Um bom processo de qualidade é aquele que cria uma relação “um-para-um” entre as fases de desenvolvimento e as atividades a serem desempenhadas pela equipe de qualidade. Essa relação bilateral promove a colaboração entre as áreas e reforça a idéia do objetivo comum.

## 4.1. Modelo de Qualidade de Software em “U”

O Processo de Qualidade de Software está decomposto em fases que se organizam em um formato em “U”. Cada fase tem uma numeração indicando a sequência de execução dos testes a serem aplicados. O objetivo do processo de qualidade é garantir que durante o ciclo de desenvolvimento do software produza efetivamente todos os produtos previstos na metodologia empregada e que o aplicativo de está sendo construído esteja adequado com os requisitos documentados. Os testes de verificação visam garantir o processo de engenharia do software, enquanto os testes de validação estão focados na garantia da qualidade do produto de software.

<div align='center'>
    <img src='books/alexandre_bartie/imgs/figura-4-1.png'>
</div>

## 4.2. Formas Básicas de um Teste

O processo de desenvolvimento de software pressupõe dois momentos bem definidos. O primeiro é a fase de coleta de informações de negócios e o planejamento da arquitetura do software. Essa fase caracteriza-se pelo esforço em criar um perfeito entendimento entre o negócio a ser atendido e o software a ser construído. Nesse momento, não existem componentes tecnológicos, mas sim documentos que especificam o comportamento a ser assimilado pelo software a ser construído, como se estivéssemos criando uma grande maquele do projeto de software - é nesse primeiro momento que uma forma básica de teste destaca-se: **os testes de verificação**.

A segunda fase do desenvolvimento do software caracteriza-se pela existência de um componente computacional (seja parte ou um todo de uma solução). Devemos aplicar um conjunto de testes que avaliam a qualidade do produto de software desenvolvido em relação aos requisitos identificados nas fases anteriores - é neste momento que a outra forma básica de teste aparece: **os testes de validação**.

### 4.2.1. Teste = Verificação + Validação

Historicamente, as empresas vêm aplicando seus testes baseando-se nos princípios dos testes de validação. Como já vimos, os erros são criados nas fases iniciais do processo de desenvolvimento, o que torna os custos de não conformidades mais caros, uma vez que estes crescem exponencialmente quando migram de uma fase à outra. Apesar de ser muito positivo algumas empresas construírem ambientes para a realização dos testes de validação, estas não estão dirigindo seus esforços para as fases iniciais do processo de software, portanto, os custos de correções dessas organizações e o número de incidênias de erros nos softwares desenvolvidos serão muito altos nas fases de testes de validação.

Testes de verificação e validação são complementares. Em hipótese alguma estes deverão ser encarados como atividades redundantes. Tanto um quanto o outro possui naturezas e objetivos distintos, fortalecendo o processo de deteção de erros e aumentando a qualidade final do produto. Um bom processo de qualidade de software deverá potencializar essas duas formas de testes de modo que os esforços sejam minimizados e os resultados sejam os mais positivos possíveis.

### 4.2.2. Testes de Verificação

Os testes de verificação podem ser entendidos como um processo de auditoria de atividades e avaliação de documentos gerados durante todas as fases do processo de engenharia de software. As verificações devem ser aplicadas a todos os produtos (documentos, gráficos, manuais, código-fonte, etc) que são produzidos em cada etapa do processo, evitando que dúvidas e assuntos “mal resolvidos” migrem para a próxima fase. Dessa forma, reduziremos os nívels de retrabalho, uma vez que esses defeitos não serão introduzidos nos softwares que serão construídos.

A principal característica dos testes de verificação é o fato de não envolver o processamento de software. Na verdade, essas atividades antecedem a criação do aplicativo, exatamente para garantir que todas as decisões e definições estabelecidas foram adequadamente entendidas e aceitas pelos diversos grupos que integrarão o procecsso de desenvolvimento.

Durante o levantamento e a definição da solução tecnológica, muitas ações deverão ser realizadas para garantir a qualidade das atividades e documentos produzidos em cada etapa do desenvolvimento como a realização de revisões de documentos e auditorias de qualidade.

<div align='center'>
    <img src='books/alexandre_bartie/imgs/figura-4-2.png'>
</div>


Os testes de verificação serão aplicados respeitando os estágios de desenvolvimento:

- Testes na etapa de definição das necessidades e características de negócios a serem atendidas pela solução.
- Testes na etapa de identificação dos requisitos funcionais e não funcionais que a solução tecnológica deverá contemplar.
- Testes na etapa de definição do modelo de arquitetura da solução tecnológica.
- Testes na etapa de construção dos softwares que atenderão às definições da arquitetura estabelecida.

### 4.2.3. Testes de Validação

Os testes de validação podem ser entendidos como um processo formal de avaliação de produtos tecnológicos que podem ser aplicados em componentes isolados, módulos existentes ou mesmo nos sistemas como um todo. Seu objetivo é avaliar a conformidade do software com os requisitos e especificações analisadas e revisadas nas etapas iniciais do projeto.

A característica dos testes de validação é a presença física do software e de seu processamento em um ambiente tecnologicamente preparado para tais atividades. Os testes serão baseados no comportamento do software, segundo diversas condições que serão simuladas, para que sejam comparados com as especificações produzidas pela área de negócios. Na maioria dos casos, esses testes expõem mais sintomas do que propriamente erros, ou seja, a maioria dos defeitos de um software não se apresenta na forma mais explícita, como uma interrupção do processamento ou uma não-execução de uma funcionalidade, mas sim na forma mais camuflada e difícil de diagnosticar, como um ajuste financeiro errado, um cálculo de imposto irregular, uma amortização de financiamento imprecisa ou mesmo alocação de estoque indevida, portanto, os resultados do processamento dos softwares serão os principais pontos de validação.

<div align='center'>
    <img src='books/alexandre_bartie/imgs/figura-4-3.png'>
</div>

Durante o desenvolvimento do software, determinadas categorias de testes serão aplicadas utilizando ferramentas, técnicas e abordagens diferenciadas. As atividades relacionadas a planejamento, modelagem, execução e conferência dos testes de software deverão ocorrer em paralelo às atividades de construção de componentes executáveis.

As validações serão aplicadas respeitando-se os estágios de desenvolvimento:

- Testes em componentes executáveis isolados recém-criados e alterados.
- Testes de interface entre componentes à medida que eles vão sendo integrados.
- Testes em sistema ou módulos completos.
- Aceite de um sistema ou módulos pelos clientes e usuários.
