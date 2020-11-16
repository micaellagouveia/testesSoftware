# Modelling Failures Occurrences of Open Source Software with Reliability Growth

## Resumo:

Os produtos de software de código aberto (OSS) são amplamente utilizados, embora um consenso geral sobre sua qualidade esteja longe de ser alcançado. Fornecer resultados sobre a confiabilidade do OSS - como indicador de qualidade - contribui para lançar alguma luz sobre este problema e permite que as organizações tomem decisões informadas na adoção de produtos OSS ou no lançamento de seu próprio OSS. Neste artigo, usamos uma técnica clássica de Crescimento da confiabilidade do software para modelar ocorrências de falhas entre as versões. Coletamos dados dos sistemas de rastreamento de bugs de três produtos OSS, Mozilla Firefox, OpenSuse e OpenOffice.org. Nossa análise visa determinar e discutir padrões de ocorrências de falha nos três produtos de software de fonte aberta a serem usados ​​para prever o comportamento de confiabilidade de lançamentos futuros. Nossos achados indicam que nos três casos as ocorrências de falhas seguem um padrão pré-determinado, o que mostra: 
- a) uma fase inicial em que a comunidade aprende a nova versão 
- b) após este primeiro período um rápido aumento da taxa de detecção de falhas até 
- c) muito restam poucas falhas e a descoberta de uma nova descoberta de falha é rara. Esta é a fase em que a versão pode ser considerada confiável.

## 1. Introdução

Muitos dos projetos de código aberto não têm recursos para dedicar a testes ou inspeções precisas, de modo que a confiabilidade de seus produtos deve depender de relatórios de falhas da comunidade. Os relatórios são armazenados nos chamados sistemas de rastreamento de bugs, são carregados pela comunidade e moderados por membros internos do projeto de código aberto. Os relatórios são arquivados com várias informações, incluindo a data de upload e a descrição da falha. Quais informações podem ser coletadas desses repositórios e como minerá-los para análise de confiabilidade ainda é uma questão em aberto.

Este artigo propõe um método para minerar repositórios de bugs a fim de determinar padrões de ocorrências de falha que podem ser usados ​​para modelar a confiabilidade de versões passadas, atuais e futuras de um produto de código aberto. Em particular, este trabalho discute se a teoria tradicional do crescimento da confiabilidade do software pode ser prontamente aplicada a dados provenientes de produtos de código aberto. Nossa abordagem se baseia em uma compreensão profunda do sistema de rastreamento de bugs usado por cada projeto de código aberto e uma limpeza precisa dos dados. Especificamente, examinamos os relatórios de usuários em versões de três projetos de código aberto, Mozilla Firefox 1, OpenOffice.org 2 e OpenSuse 3. Para cada projeto e versão, extraímos informações sobre as datas de abertura da edição e o número de relatórios abertos por dia. Ajustamos os modelos tradicionais de crescimento da confiabilidade do software com as séries temporais de falhas ocorridas por dia para cada versão. Repetimos esse procedimento para as versões principais do produto e classificamos os modelos de melhor ajuste resultantes para cada versão por um conjunto de medidas de precisão do modelo e previsão de confiabilidade. Para entender se há um padrão nas ocorrências de falha de um produto, simplesmente contamos o número de vezes que um tipo de modelo é classificado no topo entre todas as versões e por medida de precisão ou previsão.

O artigo está organizado da seguinte forma. A seção 2 consiste no histórico e alguma literatura relacionada ao trabalho. Esta seção apresenta brevemente os Modelos de Crescimento de Confiabilidade de Software e medidas de precisão e previsão. A seção 3 ilustra a amostra de dados e analisa a suposição que fizemos na coleta e análise de dados. A seção 4 apresenta o método de regressão entre versões e definição de padrão. Seção 5, relatórios das descobertas. A seção 6 ilustra a limitação do trabalho e o trabalho futuro. Com a seção 7 concluímos.

## 2. Contexto

A modelagem de ocorrências de falha com Software Reliability Growth (SRG) é uma abordagem clássica em análise estática para confiabilidade de software. No aumento da confiabilidade, presume-se que as ocorrências de falha aumentem com o tempo, de modo que o tempo até a próxima falha também aumenta com o tempo. Este comportamento é modelado com processos estocásticos que descrevem o número cumulativo de falhas ao longo do tempo. A média esperada do processo estocástico define uma função paramétrica do tempo e representa o número total esperado de falhas em qualquer instante do tempo t. Em seguida, os parâmetros da média esperada são determinados por regressão não linear no conjunto de dados real do número cumulativo de falhas ao longo do tempo.

Os maiores desafios no SRG são determinar a expressão matemática da média esperada com um procedimento construtivo ou com regressão em famílias predeterminadas de curvas de tempo. Enquanto o primeiro requer uma compreensão profunda do processo de ocorrência de falhas no ambiente operacional do produto de software, o último se concentra em um estudo ex-post mudando a complexidade da análise para a limpeza de dados, ajuste de modelo e interpretação. Neste artigo, adotamos a última abordagem para o tipo de informação que pudemos reunir com consultas remotas aos dados dos repositórios de código aberto.

Embora essa abordagem pareça mais viável em nosso caso, a mineração de repositórios para confiabilidade de software não é simples. Para entender isso, precisamos lembrar o significado de confiabilidade de software. A confiabilidade do software se refere à capacidade de um sistema de software de seguir determinadas especificações em um determinado intervalo de tempo e em determinados ajustes operacionais. Um sistema apresenta uma falha quando se desvia desse comportamento durante seu uso. Como tal, os melhores indicadores de falhas são os relatórios dos usuários sobre o mau comportamento do sistema durante seu uso. Coletar dados sobre o mau comportamento de uso é difícil, pois depende do feedback dos usuários, que é difícil de rastrear. Como consequência, a maioria dos trabalhos clássicos em SRG tem usado os mesmos bancos de dados de falhas 4, não acessíveis ao público, ou bancos de dados de defeitos descobertos durante testes internos, evitando conclusões adequadas sobre o mau comportamento do sistema real e replicações em diferentes aplicativos domínios.

Hoje em dia, os projetos de código aberto representam uma nova fonte de dados para confiabilidade de software. Eles são abertos a todos e fornecem informações suficientes para executar replicações de análises, mas podem conter informações duplicadas, falta de informações completas e usar localizações de padrões e terminologia. Por exemplo, em nosso caso, não fomos capazes de encontrar nos repositórios informações sobre implantação, perfis de uso do cliente e dados de teste que provaram ser bons preditores de taxas de ocorrência de falhas e padrões de ocorrência de falhas para previsão de sistemas de software. Também tivemos que descartar alguns projetos de código aberto que aparentemente tinham uma grande quantidade de relatórios de usuários, mas que no final - após a limpeza - os dados eram muito escassos para realizar uma análise rigorosa. Mesmo com essas desvantagens, ainda acreditamos que a análise de confiabilidade em repositórios abertos é de grande valor, pois é baseada em relatórios de usuários reais, o esforço é entender se a fonte específica fornece informações adequadas.

Por exemplo, os aplicativos Eclipse, Apache HTTP Server 2, Firefox, MPlayer OS X e ClamWin Free Antivirus foram avaliados por meio de vários modelos, e descobriu-se que a distribuição Weibull se adapta bem na modelagem de projetos mais simples, embora modelos mais complexos sejam alegou ser necessário para Firefox e Eclipse [12]. Em [15], os autores estão interessados ​​em avaliar a confiabilidade de um sistema complexo desenvolvido com uma abordagem distribuída, o desktop Xfce. Usando métodos de suporte à decisão e processos de Poisson não homogêneos (NHPP), os autores mostram como modelar as interações complexas entre os componentes para previsão de confiabilidade de falha. Em [18], vários projetos de software de código aberto foram analisados ​​e se comportam de forma semelhante a aplicativos de código fechado equivalentes. Também neste caso, a distribuição Weibull foi considerada uma forma simples e eficaz de representar o crescimento da confiabilidade do software.

Em nossa pesquisa, após selecionar os projetos de código aberto apropriados e limpar os dados, nosso trabalho fornece uma extensão do trabalho de Li et al ([7]) e Succi et al. ([14]) combinando as duas abordagens - crescimento da confiabilidade do software entre as versões ([7]) e crescimento da confiabilidade e medidas de precisão e predição ([14]) - e replicando o estudo em três OSS diferentes. Repositórios de mineração para falhas de software é um tema quente ([1], [2], [5], [6], [7], [8]), mas pelo nosso conhecimento, não parece haver nenhuma pesquisa que tenha comparado resultados em vários lançamentos e vários OSS por meio de várias medidas de precisão e previsão.

### 2.1 Modelos de crescimento de confiabilidade de software candidato

Usamos os Modelos de Crescimento de Confiabilidade de Software (SRGMs) adotados em ([14]). SRGMs são processos estocásticos descritos por uma variável aleatória de contagem determinada pelo número cumulativo de falhas ao longo do tempo ([13]). A média esperada em um dado momento t desses modelos é definida por uma curva paramétrica em t, µ (t). O objetivo do crescimento da confiabilidade do software é determinar os parâmetros da média esperada. Muitos dos SRGMs que usamos são processos de Poisson cuja probabilidade de massa é definida por uma distribuição de Poisson. O modelo básico deles é o modelo exponencial de Musa ([11]) cujo número esperado de falhas é definido pela expressão paramétrica:

<div align='center'>
    <img src='artigos/static/rossi-russo-succi/formula-01.png'>
</div>

SRGMs podem ser em forma de S ou côncavos, dependendo se eles mudam de concavidade pelo menos uma vez. Os modelos em forma de S têm um estágio inicial de aprendizado no qual a taxa de detecção de falhas, partindo de valores muito baixos, apresenta um primeiro aumento e depois uma diminuição que finalmente se aproxima de zero. Interpretando o modelo com o tempo entre as ocorrências de falha, os modelos em forma de S mostram um ritmo lento inicial de ocorrências de falhas, então um período em que as falhas são relatadas com frequência até quando relativamente poucas falhas permanecem no código e a descoberta de falhas torna-se difícil. Exemplos de modelos em forma de S são os modelos Weibull e Hossain Dahiya. Os modelos côncavos não prevêem tal curva e revelam um bom conhecimento da nova versão lançada. As falhas são descobertas logo após o lançamento em um ritmo acelerado. Exemplos de modelos côncavos são os modelos Goel-Okumoto e Gompertz.

Além disso, os modelos podem ser finitos ou infinitos. Modelos finitos têm uma assíntota horizontal e, portanto, um número total finito de falhas esperado é assumido no produto. O leitor interessado pode encontrar mais detalhes nos artigos de Succi et al., ([14]), e no livro de Lyu, ([10]).

### 2.2 As Medidas de Precisão e Previsão

As medidas de precisão e previsão capturam as propriedades de um SRGM de melhor ajuste. Agrupamos as medidas dois a dois pelo atributo do modelo que queremos investigar. A Tabela 1 os apresenta indicando as referências para leituras posteriores.

Qualidade de ajuste e precisão de ajuste referem-se à modelagem do conjunto de dados, enquanto a capacidade de previsão define a natureza de previsão do modelo. Goodness of Fit expressa a capacidade de um modelo matemático de se ajustar a um determinado conjunto de dados (R 2 e AIC). A precisão de ajuste fornece a extensão (RPF) e a capacidade do modelo de capturar os dados (COF) no intervalo de confiança de 95% do modelo. Em geral, essas duas medidas são usadas em combinação, pois fornecem informações complementares sobre a precisão do modelo. As medidas de capacidade de previsão definem a capacidade de um modelo de prever com antecedência (PA) ou com precisão (AFP) o número total final de falhas.

## 3 Datasets

Selecionamos três produtos de software de fonte aberta bem conhecidos: um navegador da web, Mozilla Firefox, um pacote de escritório, OpenOffice.org e um sistema operacional, OpenSuse. Cada um desses produtos mantém um sistema de rastreamento de bugs aberto à comunidade baseado no Bugzilla 5. Escolhemos esses três projetos de software também porque a estratégia de seu projeto para armazenamento de falhas e a terminologia usada no Bugzilla é bastante semelhante.

Para cada versão encontrada no sistema de rastreamento de bugs, coletamos todos os problemas relatados em nossa data de observação, juntamente com a data em que foram relatados (data de abertura). Para cada projeto de código aberto, consideramos todas as versões principais até meados de 2008, com mais de 40 falhas. Para o OpenOffice.org, conseguimos 13 versões até 2006 (decidimos que eram suficientes para o propósito desta análise). Infelizmente, OpenSuse e Mozilla Firefox não tinham tantos relatórios e versões no momento de nossa coleta de dados e tivemos que limitar as versões a cinco para OpenSuse e três para Mozilla Firefox.

A Tabela 2 ilustra o conjunto de dados coletado e os modelos usados ​​nos conjuntos de dados.

O repositório Bugzilla permite minerar falhas com consultas sofisticadas. Um relatório no Bugzilla é chamado de problema ou bug e pode conter uma grande quantidade de informações que precisam ser eliminadas de acordo com a pesquisa realizada. Para escolher a visão mais adequada para o objetivo da pesquisa, é preciso entender em detalhes o ciclo de vida de um problema. Na Fig. 1, relatamos o ciclo de vida padrão de um relatório enviado a um repositório Bugzilla conforme descrito na documentação 7. 

Embora os três projetos que escolhemos sejam todos suportados por um repositório Bugzilla, descobrimos que sua personalização varia significativamente. Assim, partindo da descrição da Fig. 1., tivemos que nos esforçar ainda mais na homogeneização da terminologia e dos procedimentos usados pelos projetos de código aberto na moderação dos problemas.

<div align='center'>
    <img src='artigos/static/rossi-russo-succi/figura-01.png'>
</div>

### 3.1 Premissas empíricas

Nesta seção, discutimos todas as suposições que fizemos sobre os dados antes de iniciar nossa análise.

Olhando para o número cumulativo de falhas, notamos que em cada versão a taxa de crescimento tende a zero para grandes valores de tempo (Fig. 2, 3 e 4) indicando um limite para o número total de falhas. Por esta razão, decidimos incluir apenas modelos finitos em nossa análise, ([10]).

Após uma inspeção profunda dos repositórios e de sua documentação, decidimos nos concentrar nos problemas que foram declarados "bug" ou "defeito", excluindo qualquer problema que foi chamado de algo como "aprimoramento", "solicitação de recurso", "tarefa ”Ou“ patch ”. Isso teria garantido que nossa análise lidou com as falhas adequadas. Pelo mesmo motivo, consideramos apenas os problemas que foram relatados como fechados ou corrigidos (de acordo com a terminologia do repositório único) após a data de lançamento de cada versão. Ou seja, os relatórios antes da data de lançamento eram, em geral, candidatos a lançamento de teste relacionados e não expressavam a confiabilidade da versão. Pelo mesmo motivo, limpamos o conjunto de dados de problemas que foram declarados como "duplicado", "não corrige" ou "funciona para mim". A Tabela 3 ilustra nossa escolha.

<div align='center'>
    <img src='artigos/static/rossi-russo-succi/tabela-03.png'>
</div>

## 4. O Método

Para cada versão da Tabela 2, coletamos as falhas de acordo com sua data de abertura. Dessa forma, definimos uma série temporal de número cumulativo de falhas por versão. As três imagens a seguir ilustram uma amostra da série temporal e os gráficos de seus SRGMs. Na Fig. 4, também relatamos o intervalo de confiança de 95% do modelo Hossain Dahiya.

<div align='center'>
    <img src='artigos/static/rossi-russo-succi/figura-02.png'>
</div>

<div align='center'>
    <img src='artigos/static/rossi-russo-succi/figura-03.png'>
</div>


Para cada OSS escolhido, ajustamos a média paramétrica esperada dos SRGMs com a série cumulativa real de falhas para cada versão da Tabela 2. Como resultado, obtivemos um conjunto de modelos de melhor ajuste, cada um correspondendo a um tipo de SRGM na Tabela 2. No final, obtivemos 18 SRGMs (6 cada versão) para Mozilla Firefox, 52 SRGMs (4 cada versão) para OpenOffice.org e 25 SRGMs (5 cada versão) para OpenSuse. As Fig. 2, 3 e 4 ilustram as séries temporais e as curvas correspondentes aos modelos de melhor ajuste para uma versão dos três OSS. Classificamos os modelos de melhor ajuste resultantes de cada versão pelas medidas de precisão do modelo e previsão de confiabilidade da Tabela 1.

Um SRGM com desempenho superior para uma determinada medida nas versões de um OSS representa um padrão de confiabilidade para esse OSS. Para determinar o padrão, simplesmente contamos para cada medida de precisão ou previsão da Tabela 1, o número de vezes que um SRGM de melhor ajuste de um determinado tipo supera em todas as versões. Na seção seguinte, discutiremos a existência e o tipo de padrão que encontramos.


<div align='center'>
    <img src='artigos/static/rossi-russo-succi/figura-04.png'>
</div>

## 5. Descobertas

A seguir, relatamos os resultados dos três OSS. O modelo Yamada não está incluído porque sua análise não reporta resultados significativos.

OpenSuse. Para todas as versões do OpenSuse, o modelo Weibull é o melhor em todas as medidas, exceto capacidade de previsão. Assim, podemos dizer que entre as versões ele representa os dados (Qualidade de ajuste), captura a maioria dos dados em pequena área de confiança (precisão de ajuste) e é preciso na determinação do número final de defeitos que determina parcialmente capacidade de previsão. Ou seja, não é o melhor para capacidade de previsão, portanto, não podemos usá-lo para prever o número total de defeitos no início do tempo. Na verdade, não há SGRMs que podem fazer isso, pois nenhum modelo supera as versões em capacidade de previsão.

A predominância do modelo Weibull confirma os achados em ([7]) estendendo o resultado para outras medidas de precisão que não o Critério de Informação de Akaike. Na Tabela 4, relatamos as classificações da versão 11.0.

Mozilla Firefox. O modelo Weibull domina em todas as versões para todas as medidas, exceto a precisão do ponto final e a precisão relativa de ajuste. Novamente, isso confirma e estende os resultados em ([7]). Na Tabela 5, ilustramos os valores das medidas da versão 1.5 do Mozilla Firefox. Os valores em negrito são os melhores. Nesta versão, o modelo Weibull tem o pior comportamento geral em comparação com as outras versões. No entanto, está no topo da classificação em três das seis medidas e com bom desempenho nas demais. O caso excepcional é o RPF que mede a área do intervalo de confiança de 95% ao longo do intervalo de tempo da série. Como medida de precisão, o RPF é subsidiário do CoF e é usado em combinação com ele. Assim, como modelos com baixo CoF são menos relevantes per se, o modelo de Weibull é o mais interessante, embora a razão CoF / RPF não seja a mais alta. O modelo Weibull não é o melhor para previsão, entretanto. Isso é verdade para todas as versões e, em particular, no caso do AFP para a versão 1.5 na Tabela 5.

OpenOffice.org. O modelo Weibull é novamente o melhor modelo em todas as medidas de precisão e previsão. Em particular, para CoF, o modelo supera 70% das vezes entre as versões.

A predominância do modelo Weibull em tantas versões como no OpenOffice.org é definitivamente significativa.

Comparando os resultados das três aplicações, podemos dizer que:

- Para Goodness of fit (R square e AIC) o modelo de Weibull confirma sua superioridade de acordo com o trabalho de Li et al. ([7]). O modelo representa bem os dados e o padrão Weibull pode ser usado para representar versões futuras.

- Para precisão de ajuste, o intervalo de confiança de 95% do modelo Weibull é o melhor na captura de dados dentro de seu intervalo de confiança de 95% (CoF), embora às vezes com uma densidade pobre (ou equivalentemente em um grande intervalo de confiança, RPF). Esta é uma medida de disseminação de dados ao redor do modelo, também levando em consideração sua variação em seu intervalo de confiança. Qualquer variação significativa do modelo ainda representa os dados com precisão suficiente. Isso pode ser útil quando discutimos o tempo de ocorrências nos repositórios de código aberto. O tempo relatado nos repositórios (tempo do calendário) pode não se referir ao tempo real em que o usuário teve uma falha. Pode ter ocorrido algum atraso. Como tal, o resultado para Precisão de ajuste, mesmo que forneça uma resposta positiva para o modelo Weibull, não é completamente satisfatório e uma análise de sensibilidade de Monte Carlo sobre o tempo para cada versão será questão de trabalho futuro.

- Para capacidade preditiva, o modelo Weibull é definitivamente bom para estimar o número total final de falhas (AFP), mas não pode ser usado - como qualquer outro SRGM - para previsão antecipada (PA). Para este propósito, outras abordagens podem ser consideradas em combinação ([1], [8], [9]). A falta de um padrão para PA significa ainda que na maioria das versões dos três OSS há um baixo aumento da taxa de detecção de falha como na Fig. 2 (com ou sem efeito de aprendizagem) de modo que é impossível prever o número total de falhas de uma versão no estágio inicial do processo de relatório de falhas. Assim, o caso da Fig. 3, onde aparece um aumento repentino e precoce da taxa de detecção, é menos frequente nas versões dos três produtos. A Fig. 2 representa melhor os dados, pois após 300 dias o número de falhas ainda está longe de ser próximo ao número total final da versão.

## 6. Limitações e trabalho futuro

Durante nossa inspeção, entendemos que o sistema de rastreamento de bugs é usado regularmente pela equipe interna do projeto. Os membros da equipe interna conhecem melhor o aplicativo, portanto seus relatórios podem não representar relatórios típicos de falha do usuário final. Embora tenhamos usado algumas medidas para limitar esse viés (seção 4.1), como não pudemos diferenciar os problemas relatados pela equipe interna e pelo resto do mundo, não podemos garantir que o conjunto de dados seja um conjunto de dados de falhas relatadas apenas no final -Comercial. Em qualquer caso, como consideramos os relatórios emitidos somente após a data de lançamento, os relatórios dos membros da equipe interna referem-se a um período operacional do OSS e, como tal, contribuem para algo existente para a confiabilidade geral do OSS.

A data do relatório pode não ser exatamente a data da descoberta da falha. Pode ter havido algum atraso no relato dos problemas e - dependendo do repositório - na atribuição da data de abertura durante a moderação do problema. Isso pode criar um ruído no tempo e será assunto para pesquisas futuras.

O número de versões, o número e os tipos de SRGMs e as janelas de tempo das observações são diferentes nos três OSS. Isso ocorreu devido a algumas restrições de tempo, a disponibilidade dos dados nos repositórios e os valores ausentes para as medidas na Tabela 1. Como não pretendemos comparar os três OSS, queremos entender se existe um padrão de confiabilidade em cada OSS, essa diferença não é crucial.

## 7. Conclusões

O objetivo deste artigo foi apresentar uma abordagem para investigar a confiabilidade do OSS com o crescimento da confiabilidade do software. Usamos repositórios on-line abertos para coletar dados de três projetos diferentes. Limpamos intensamente os dados que coletamos para limitar a tendência associada à natureza aberta desses repositórios.

Descobrimos que a teoria clássica do crescimento da confiabilidade do software é apropriada para tais dados e é um bom instrumento para modelar ocorrências de falha entre versões de software.

Descobrimos que o modelo Weibull é o melhor modelo que se ajusta aos dados em todas as versões para cada OSS (Goodness of Fit) com uma baixa porcentagem de outliers (Precision of Fit). Isso confirma os resultados obtidos em ([7]) para o Akaike Information Criterion e revela um padrão comum de confiabilidade de software para os três OSS. Ou seja, o modelo Weibull é o melhor SRGM que representa as ocorrências de falha nos três produtos de código aberto. É um exemplo de curva em forma de S e, como tal, indica uma fase inicial de aprendizagem na qual a comunidade de usuários finais e revisores do projeto de código aberto não reage prontamente ao novo lançamento. Essa lentidão com que as falhas são reportadas pode ter várias causas como, por exemplo, o desconhecimento do projeto ou sua complexidade. Dada a existência de lançamentos candidatos e versões intermediárias, era de se esperar que a comunidade estivesse pronta para relatar as falhas logo após a data de lançamento ao público. Mas a curva de aprendizado é diferente em três OSS.