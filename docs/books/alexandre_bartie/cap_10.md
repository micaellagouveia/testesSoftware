# Capítulo 10 - Analisando Cada Fase dos Testes de Verificação

Cada fase do projeto de software cumpre uma importante etapa de entendimento do problema e da definição de uma solução mais adequada às necessidades do cliente. Cabe ao processo de qualidade de software garantir que cada etapa está sendo concluída adequadamente para que a etapa posterior seja desempenhada da forma mais tranquila e produtiva possível.

A etapa de verificação tem importância fundamental no processo de qualidade, pois focaliza suas ações nas etapas iniciais do projeto, nas quais geralmente ocorre a maior incidência de defeitos geralmente associados a definições erradas ou a falhas nas decisões realizadas.

<div align='center'>
    <img src='books/alexandre_bartie/imgs/tabela-10-1-1.png'>
</div>

<div align='center'>
    <img src='books/alexandre_bartie/imgs/tabela-10-1-2.png'>
</div>

Normalmente, as etapas de um projeto de software produzem documentos sem que estes sofram uma avaliação direta, o que impede que determinados problemas sejam avaliados por diferentes ângulos, aumentando os riscos das decisões formalizadas serem inconsistentes na sua prática. É nesse ponto que o processo de verificação ganha força e torna-se um importante mecanismo de prevenção de defeitos, pois atua diretamente na fonte das decisões e avalia se determinadas atividades críticas do processo de software estão sendo realizadas.

## 10.1. Verificação de Negócios

Normalmente, a fase de modelagem de negócios não é convenientemente explorada nos projetos de desenvolvimento de software. Como é nessa fase que estabelecemos o primeiro contato com as necessidades, expectativas e exigências do cliente, conseguimos estabelecer uma macrovisão da extensão do projeto e dos principais objetivos a serem alcançados com a construção de um novo software. Atender a essas expectativas é crucial para o sucesso de um projeto de software.

<div align='center'>
    <img src='books/alexandre_bartie/imgs/figura-10-1.png'>
</div>

Assim, espera-se que nessa fase exista uma modelagem de negócios que possibilite a criação da macrovisão, a qual possibilitará um dimensionamento adequado dos recursos humanos, físicos e financeiros necessários para a construção do software e para sua adequada operacionalização. Com essa visão bem definida e os prazos e custos adequadamente projetados, poderemos avaliar se é vantajoso ou não dar prosseguimento ao projeto.

### 10.1.1. Pontos de Verificação

O objetivo dessa fase é garantir que os diversos documentos produzidos tenham total aderência às necessidades apontadas pelos clientes. Muitas vezes, os projetos são iniciados sem que os clientes tenham validado essa macrovisão, fazendo com que a equipe do projeto superestime as necessidades do cliente, criando um “canhão para matar uma única mosca”. O exercício de revisar esses documentos com o cliente possibilita explorar alguns aspectos que podem inviabilizar um projeto de software, fazendo com que o cliente perca uma oportunidade real de negócios devido ao mau dimensionamento do problema.

Abaixo estão relatados alguns pontos que poderiam ser considerados críticos para se avaliar a qualidade desses documentos.

- Avaliar se todas as necessidades, metas e exigências foram listadas.
- Verificar se a modelagem de negócios cobre todas as necessidades.
- Conferir se as projeções realizadas são baseadas em métricas e indicadores confiáveis.
- Avaliar a existência de alternativas a essa solução.
- Avaliar o retorno sobre o investimento em cada alternativa existente (ROI).
- Validar as opções de investimento (árvore de decisão).

### 10.1.2. Um Exemplo de Checklist

Deverá existir uma única checklist para cada documento produzido na fase de verificação da modelagem de negócios. Nesta etapa, é conveniente que todos os documentos gerados sejam revisados pelo cliente, uma vez que serão eles que “pagarão a conta” caso as coisas não sejam adequadamente bem planejadas.

<div align='center'>
    <img src='books/alexandre_bartie/imgs/tabela-10-2.png'>
</div>

<div align='center'>
    <img src='books/alexandre_bartie/imgs/tabela-10-3-1.png'>
</div>

<div align='center'>
    <img src='books/alexandre_bartie/imgs/tabela-10-3-2.png'>
</div>

### 10.1.3. Um Exemplo de Critério de Finalização

Como se trata de uma fase extremamente crítica do projeto de software, é recomendável estabelecer um critério de finalização apoiado no aceite de toda a documentação referente à modelagem de negócios e ao documento que descreve as condições técnicas e financeiras a que será submetido esse projeto; portanto, abaixo estão listados alguns critérios que poderiam ser empregados:

- Modelagem de negócios assinada pelas diretorias e gerências envolvidas.
- Proposta de projeto de software assinada pelas diretorias e gerências envolvidas.

## 10.2. Verificação de Requisitos

Uma vez encerrada a fase de modelagem de negócios, temos um projeto que possui orçamento definido, objetivos e necessidades a serem alcançados, além de uma macro-visão que possibilita definir o escopo do projeto de software com relativa precisão. Portanto, nesta nova fase do processo de engenharia de software, teremos agora a missão de detalhar todos os aspectos funcionais e não funcionais relativos à solução a ser construída, estabelecendo todo o conjunto de especificações de negócio em seu nível máximo de detalhamento.

O sucesso de qualquer projeto de software depende dessa fase de definição dos requisitos. É neste momento que as áreas de negócios e tecnologia detalham e estabelecem a “verdadeira dimensão” do projeto, apontando todos os aspectos a serem implementados. Também é aí que refinamos a expectativa do cliente em relação ao produto, uma vez que o nível de detalhamento possibilita a descoberta de aspectos que não tinham sido previstos. Caso seja necessário, serão rediscutidos custos e prazos com o cliente, para que sejam introduzidas as novas características no projeto do software.

<div align='center'>
    <img src='books/alexandre_bartie/imgs/figura-10-2.png'>
</div>

Os requisitos direcionarão todas as fases posteriores do desenvolvimento do software, estabelecendo um escopo para o produto final. Esses requisitos são registrados sem especificar como serão implementados. Servem também para ajudar a definir a arquitetura e avaliar o sistema à medida que este evolui em seu desenvolvimento.

A qualidade dos requisitos é um importante indicador de uma organização. Bons controles de requisitos estão geralmente associados ao nível de maturidade organizacional. É comum que no avançar do projeto novos requisitos venham a ser incorporados, provocando mudanças e aumento do volume total de trabalho. Gerenciar bem essa demanda adicional de requisitos significa controlar os impactos de tempo e recursos que isso irá demandar, portanto, trata-se de uma fase crítica do processo como um todo.

### 10.2.1. Pontos de Verificação

Nessa etapa, os revisores deverão concentrar-se na identificação de todos os requisitos funcionais e não funcionais de um software. É muito comum nessa fase que os requisitos sejam relatados de forma simplificada, sem que exista real entendimento sobre o item que está sendo listado. Cada requisito deve ser claro o suficiente para que não produza uma interpretação errada sobre sua real intenção, o que provocaria falha na concepção do produto, gerando custo adicional no projeto de software.

Assim, cabe aos profissionais que estão atuando como revisores investigar esses requisitos e garantir sua adequada definição. Abaixo estão relatados alguns exemplos de pontos que poderiam ser considerados críticos na avaliação da qualidade dos requisitos.

- Completo: Todos os requisitos do projeto devem estar documentados.
- Claro: Cada requisito deve expressar seu propósito em relação ao projeto.
- Simples: Cada requisito deve expressar sua essência com uma simples definição.
- Preciso: Cada requisito deve ser exato, não dar margens a dúvidas.
- Consistente: Cada requisito não deve possuir conflitos com outros requisitos existentes.
- Relevante: Cada requisito deve pertencer ao escopo do projeto em questão.
- Testável: Cada requisito deverá fornecer informações que possibilitem quantificar se um determinado item foi adequadamente implementado.
- Factível: Cada requisito deve ser viável em sua implementação, avaliando as condições financeiras, humanas e tecnológicas disponíveis no projeto.

Expressões como ser um software seguro, fácil de usar, fácil de manter, com boa performance, são muitas vezes citadas mas nunca bem explicadas. Cada uma parece ser uma grande armadilha que deve ser desarmada e essa é a missão dos revisores. Quando estamos lendo os requisitos pelo ponto de vista da qualidade, essas afirmações passam a ter valor fundamental, afinal, será através desses parâmetros que iremos avaliar se os requisitos foram adequadamente implementados.

Quando um revisor encontrar a frase “As consultas a pedidos deverão ter uma boa performance”, este logo tentará estabelecer parâmetros mensuráveis, como por exemplo, “As consultas a pedidos (100 usuários simultaneamente em sites diferentes) deverão ocorrer em até 10 segundos”. Dessa forma, estabelecemos um acordo de serviço entre a área de negócios e a de tecnologia, sendo devidamente documentado como um requisito do software.

### 10.2.2. Um Exemplo de Checklist

<div align='center'>
    <img src='books/alexandre_bartie/imgs/tabela-10-4.png'>
</div>

### 10.2.3. Um Exemplo de Critério de Finalização

O critério de finalização da fase de levantamento dos requisitos deve garantir que todos os requisitos foram adequadamente identificados pelo projeto de software. Os requisitos devem refletir todas as características funcionais e não funcionais que o cliente espera receber quando o software está  disponibilizado, funcionando como uma espécie de contrato de serviço. Portanto, as especificações que detalham esses requisitos serão revisadas com a área usuária para que não exista um desvio das expectativas originais do cliente em relação ao software que está sendo desenvolvido. Alguns critérios que poderiam ser empregados para finalizar essa fase são:

- Especificações funcionais criadas e revisadas.
- Especificações não funcionais criadas e revisadas.
- Rastreabilidade entre requisitos e entre necessidades.

## 10.3. Verificação da Análise e Modelagem

Uma vez determinados os requisitos que são esperados, conseguimos produzir uma imagem mais nítida sobre o que deveremos atender, possibilitando a modelagem de uma solução mais aderente e flexível às exigências e expectativas do cliente.

Nessa etapa o objetivo é definir uma solução tecnológica que suporte não somente os requisitos estabelecidos pelo cliente, mas também requisitos de qualidade que deverão ser atendidos pela arquitetura do software a ser modelada. A modelagem de uma boa arquitetura deve contemplar características como flexibilidade (capacidade de absorver mudanças e arranjos diferenciados de processamento), escalabilidade (suportar o crescimento de transações), ser reutilizável (intensificar a reutilização de partes do software). Tudo isso deverá estar inserido no contexto da solução tecnológica que será definida nessa fase.

Muitas vezes, as soluções modeladas nem sempre são adequadas ao longo prazo, evidenciando falhas no processo de definição da arquitetura. As revisões possibilitam validar determinados aspectos críticos de uma solução, avaliando a existência de mecanismos que suportem um alto nível de parametrização, possibilitando assimilar mudanças nos negócios e em tecnologias.

<div align='center'>
    <img src='books/alexandre_bartie/imgs/figura-10-3.png'>
</div>

### 10.3.1. Pontos de Verificação

O objetivo desta fase não está somente na avaliação da aderência da solução tecnológica aos requisitos funcionais e não funcionais estabelecidos pelo cliente, mas também em avaliar a modelagem da solução como um todo. Nessa fase, as revisões devem simular cenários de mudanças que possibilitem avaliar o quanto a solução consegue absorver as modificações de negócios e tecnologias que poderão ocorrer ao longo do tempo, simulando um impacto direto na arquitetura da solução modelada. Abaixo, alguns pontos que poderiam ser avaliados durante esse processo:

- Avaliar se todos os requisitos funcionais e não funcionais contemplam a solução.
- Avaliar se a arquitetura suporta o crescimento e a segurança desejados.
- Avaliar se a arquitetura suporta futuras mudanças de negócios e de tecnologia.
- Avaliar se a arquitetura pode ser operacionalizada em vários ambientes.
- Avaliar as restrições e problemas conhecidos da arquitetura a ser adotada.

### 10.3.2. Um Exemplo de Checklist

Uma checklist de verificação da análise e modelagem deverá existir para cada documento a ser revisado. Caso o projeto esteja utilizando diagramas UML para representar as decisões de modelagem e da arquitetura, poderemos empregar uma checklist que siga as seguintes características.

<div align='center'>
    <img src='books/alexandre_bartie/imgs/tabela-10-5-1.png'>
</div>

<div align='center'>
    <img src='books/alexandre_bartie/imgs/tabela-10-5-2.png'>
</div>

<div align='center'>
    <img src='books/alexandre_bartie/imgs/tabela-10-6.png'>
</div>

### 10.3.3. Um Exemplo de Critério de Finalização

O critério de finalização da fase de análise e modelagem deve garantir que a solução tecnológica que foi modelada atende adequadamente a todos os requisitos dos clientes, além de incorporar características que deixam a arquitetura flexível e aderente a futuras mudanças. Essa arquitetura deverá ser validada com toda a equipe de profissionais, inclusive a equipe técnica do cliente, que discutirá todos os pontos referentes à utilização da solução modelada. Alguns critérios que poderiam ser empregados para finalizar essa fase são: 

- Diagramas estáticos (classes e objetos) criados e revisados.
- Diagramas dinâmicos (estados, sequência e atividades) criados e revisados.
- Diagramas de distribuição (componentes e implantação) criados e revisados.

### 10.4. Verificação da Implementação

Essa fase encerra o ciclo de verificação de testes. Nela, toda a documentação produzida pelas fases anteriores serão transformadas em código de uma determinada linguagem de desenvolvimento. A maioria das organizações começa seu ciclo de verificação nessa fase. Como muitas delas possuem um fraco processo de coleta de requisitos e modelagem de negócio, tal verificação torna-se inócua. Transformar em código especificações ruins, incompletas e imprecisas acarreta produtos não adequados e pouco confiáveis.

<div align='center'>
    <img src='books/alexandre_bartie/imgs/figura-10-4.png'>
</div>

Algumas empresas de software realizam um processo formal de verificação do código produzido. Os testadores avaliam linha por linha em busca de erros, analisam alternativas melhores e mais simples de produzir os mesmos resultados, comentam nomes e declarações não compatíveis com os documentos gerados nas fases anteriores. Enfim, produzem um qualitativo processo de verificação do código-fonte; porém, esse processo pode ser extremamente informal, no qual cada desenvolvedor avalia o código de outro profissional em busca de erros realizados.

### 10.4.1. Pontos de Verificação

O objetivo dessa fase é garantir a qualidade do código-fonte gerado pela equipe de desenvolvimento. Essa qualidade será atribuída pela prática das chamadas “regras da boa programação”, que podem contemplar diversas normas e padrões corporativos seguidos pelas diversas equipes de desenvolvimento. Abaixo estão relatados alguns exemplos de pontos que poderiam ser considerados críticos para avaliar a qualidade dos fontes.

- Comparar os modelos de arquitetura com os códigos-fontes.
- Utilizar ferramenta de análise estática para avaliar a complexidade dos
fontes.
- Avaliar as mensagens apresentadas ao usuário final.
- Inspecionar a existência de rotinas de tratamentos de erros nos pro-
cessos críticos.
- Inspecionar se o volume de comentários é suficiente.
- Inspecionar a legibilidade do código.
- Inspecionar o padrão de nomenclaturas existentes.

### 10.4.2. Um Exemplo de Checklist

Uma checklist da implementação deverá contemplar um único documento a ser inspecionado. No caso de linguagens de programação, alguns pontos da checklist serão específicos de cada tecnologia, enquanto que outros pontos serão comuns a todas as linguagens existentes. No caso de revisões dos bancos de dados, também existirá uma checklist específica para essa verificação.

<div align='center'>
    <img src='books/alexandre_bartie/imgs/tabela-10-7-1.png'>
</div>

<div align='center'>
    <img src='books/alexandre_bartie/imgs/tabela-10-7-2.png'>
</div>

<div align='center'>
    <img src='books/alexandre_bartie/imgs/tabela-10-8.png'>
</div>

### 10.4.3. Um Exemplo de Critério de Finalização

Podemos empregar uma ferramenta cujo objetivo é realizar, de forma automática, inspeções nos códigos gerados pela equipe de desenvolvimento. Essa ferramenta realizará uma análise de normas e padrões relacionada às boas práticas de programação. Também será realizada análise da complexidade do código-fonte produzido pelos programadores, o que permitirá avaliar se os códigos estão sendo bem construídos ou não. O resultado dessa análise será uma lista de não-conformidades que deverá ser analisada pela equipe de desenvolvimento até que os critérios de finalização sejam alcançados, considerando neste momento o código-fonte OK.

#### 10.4.3.1. Análise de Normas e Padrões de Codificação

Será necessário parametrizar a ferramenta com as práticas de codificação da organização, como padrões de variáveis, bibliotecas de uso comum, padrões de internacionalização, regras de portabilidade entre versões de sistemas operacionais, entre outros.

A ferramenta irá melhorar a qualidade final do código-fonte, uma vez que conduz o programador a utilizar padrões conhecidos de trabalho, facilitando o entendimento e, consequentemente, a manutenção dos códigos-fonte.

#### 10.4.3.2. Análise da Complexidade do Código

A ferramenta realiza a análise da complexidade dos códigos-fonte inspecionados, identificando quais rotinas estão com complexidade acima da permitida pelos padrões definidos pela organização. A ferramenta utiliza as métricas de McCabe para determinar o nível de complexidade do código (complexidade ciclomática) e identificar a probabilidade.

<div align='center'>
    <img src='books/alexandre_bartie/imgs/tabela--1.png'>
</div>

Onde:

- Complexidade Ciclomática: é o nível de complexidade de um código-fonte segundo as métricas definidas por McCabe.
- Avaliação da Complexidade: estabelece as categorias de complexidades possíveis a serem atribuídas a um código-fonte segundo os critérios de McCabe.
- Esforço de Manutenção e Teste: dimensiona o esforço necessário para a realização de testes de caixa branca e realização de manutenções nas diversas categorias de complexidades de um código-fonte.
- Probabilidade de Inserção de Erros: dimensiona a possibilidade do risco associado às categorias de complexidades de uma determinada manutenção inserir um novo erro no código-fonte.

Segundo o critério de finalização pela análise de complexidade de código, segundo as métricas definidas por McCabe, somente serão considerados em conformidade os fontes que estiverem de acordo com os critérios estabelecidos pela seguinte tabela:

<div align='center'>
    <img src='books/alexandre_bartie/imgs/tabela--2.png'>
</div>

**Observação**: Notem que esse critério de finalização estabelece um padrão mínimo de qualidade do código-fonte, ou seja, existe uma tolerância para os códigos “difícil” e “moderado” desde que não representem mais de 5% e 20%, respectivamente. No entanto, os códigos categorizados como “muito difícil” e “impossível de testar” não serão aceitos em hipótese alguma. Trata-se de uma regra que está explícita tanto para desenvolvedores quanto para os profissionais da área de qualidade. Cabe aos desenvolvedores produzir códigos segundo esse critério, enquanto cabe aos profissionais de qualidade garantirem que esses valores estão sendo respeitados.
