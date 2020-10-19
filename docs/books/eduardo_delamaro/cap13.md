# Capítulo 13 - Confiabilidade

## 13.1. Introdução

Com o constante desenvolvimento da tecnologia, os sistemas computacionais têm sido requisitados em quase todas as áreas da atividade humana. Especificamente nos últimos anos, softwares específicos foram desenvolvidos para aplicações críticas, como sistemas de controle de usinas nucleares, sistemas de controle aeroespacial, controle de processos na área médica e muitas outras áreas de risco no campo industrial. A natureza de sistemas computacionais em termos de precisão de tempo e em termos de comportamento repetivivo faz do software ideal para áreas nas quais um simples engano pode causar efeitos extremamente danosos.

Essa crescente dependência em relação ao software tem conscientizado tanto os usuários, que cada vez mais exigem softwares confiáveis, como também a industria de software, no sentido de desenvolver produtos de alta qualidade.

O desenvolvimento de software que atende as exigências dos usuários, com o nível de confiabilidade exigido é um tarefa extremamente difícil. Essa dificuldade é devido o fato de software ser uma entidade lógica que não possui termos de valor concreto que definem a qualidade do produto.

A confiabilidade é uma característica que tem sido extensivamente considerada na análise da qualidade do software, pois se um software não é confiável, pouco importa se outras características da qualidade são aceitáveis.

Ao atribuir-se um grau de confiabilidade ao software, o objetivo é quantificar alguns aspectos desse software que, devido à presença inevitável de defeitos (bugs), está sujeito a falhas durante seu período de utilização. Assim, o estudo da confiabilidade de software caracteriza-se como uma abordagem analítica que está baseada nos conceitos de métricas, medidas e modelos.

De uma maneira geral, um sistema de software é dito confiável se desempenha corretamente suas funções especificadas por um longo período de execução e em um variedade de ambientes operacionais. Essencialmente, existem três maneiras de se alcançar um alto nível de confiabilidade:
- Evitar a introdução de defeitos durante o projeto e o desenvolvimento do programas.
- Fazer uso de estruturas tolerantes a defeitos
- Remover defeitos durante a fase de teste e depuração

As duas primeiras maneiras enquadram-se na abordagem construtiva: consistem em desenvolver software utilizando os métodos, as técnicas e as ferramentas disponíveis. Finalmente, a confiabilidade do software pode ser melhorada pelo teste e depuração, abordagem em que o software é submetido a um intenso processo dinâmico que objetiva a detecção e a remoção dos defeitos restantes.

A primeira consideração na análise de confiabilidade de software é como medir a confiabilidade. Várias métricas foram propostas para responder essa questão. Alguns autores sugerem associar a confiabilidade diretamente ao número de defeitos restantes no software. Assim, a atividade de teste de software é um método primário para se obter a medida de confiabilidade. Para tanto, torna-se necessária a coleta de dados de falhas. Essa coleta compreende:
- 1) Contagem de falhas para o rastreamento da quantidade de falhas observadas por unidade de tempo
- 2) Tempo médio entre falhas que faz o rastreamento dos intervalos entre falhas consecutivas.

De posse desses dados, a engenharia de confiabilidade de software pode desenvolver atividades de estimação e previsão.

A confiabilidade é definida como a probabilidade de que o software não falhe em um dado intervalo de tempo, em um dado ambiente. Logo, é uma medida importante para decidir sobre a liberação do software. A probabilidade de ocorrência de falha serve também como um preditor útil da confiabilidade corrente para o software em operação. Um software considerado altamente confiável quando pode ser utilizado sem receio em aplicações críticas. 

Ao contrário dos demais produtos físicos de engenharia, o software não envelhece e não sofre desgaste por ação do uso ou do tempo. No software defeitos podem ser introduzidos nas várias fases de desenvolvimento e são causados principalmente por problemas no projeto. O crescimento da confiabilidade do software resulta da descoberta e da eliminação de defeitos no software obtidos pela aplicação de um teste intensivo e de qualidade.

Quando um software é reparado, a sua confiabilidade pode tanto aumentar como diminuir, casos novos defeitos sejam inseridos durante o reparo. Assim, o objetivo da engenharia de confiabilidade de software é melhorar a confiabilidade, pois é entendido que o software sempre irá possuir defeitos (bugs).

## 13.2. Fundamentos de confiabilidade de software

A ocorrência de falhas em um software é um evento totalmente imprevisível e, desse modo, deve ser considerada um processo aleatório. Por isso, o estudo da confiabilidade de um sistema resume-se em aplicar a teoria de probabilidade na modelagem do processo de falhas do sistema e na predição da probabilidade de ocorrência de um sucesso.

A teoria de confiabilidade está estreitamente ligada à teoria de probabilidade, e, assim, a confiabilidade é uma característica da qualidade do software que pode ser expressa por meio de números entre 0 (não confiável) e 1 (totalmente confiável). O número de defeitos no software que provocaram as falhas determina uma confiabilidade estável no software. À medida que os defeitos são detectados e removidos, sem a inserção de novos defeitos, o software passa a ter uma menor intensidade de falhas e, por consequência, há um aumento na confiabilidade.

Considerando a ocorrência de falhas no software como um evento aleatório, a atribuição da confiabilidade está associada ao estudo de algumas variáveis aleatórias do processo de falhas. Como exemplo, a confiabilidade de um software pode estar associada ao tempo médio entre a ocorrência das falhas.

A confiabilidade informa se o software está sendo aperfeiçoado (falhando cada vez menos), na medida que se detectam e removem os defeitos. Se os tempos entre as falhas permanecem os mesmo, então a confiabilidade do software continua estável. Se o tempo entre as falhas aumentam, então tem-se um crescimento na confiabilidade do software.

### 13.2.1. Definições

A teoria sobre confiabilidade de software lida com métodos probabilísticos aplicados para analisar a ocorrência aleatória de falhas em um dado sistema de software. Nesta seção são apresentados alguns conceitos que formalizam a teoria da confiabilidade, tais  como: função Confiabilidade, função Taxa de Falhas, função de Falhas Acumuladas, função Intensidade de Falhas, Tempo Médio para Falhas (MTTF) e Tempo Médio entre Falhas (MTBF).

No estudo sobre confiabilidade de software, a variável aleatória de interesse pode ser o tempo T decorrido para a ocorrência de uma falha do software. Por conseqüência, a base dos resultados sobre confiabilidade estará relacionada ao estudo da variável aleatória T , mais especificamente, ao estudo das funções associadas à variável aleatória T, tais como função densidade de probabilidade f(t) e função distribuição de probabilidades acumuladas F(t).

A probabilidade de que haja uma falha no software em decorrência do tempo t é definida como:

<p align="center">
  <img src="books/eduardo_delamaro/static/img-13-0.png" width="500">
</p>

em que f(t) é a função densidade de probabilidade e F (t) é a função distribuição de probabilidades, da variável aleatória T . Por conseqüência, a probabilidade de que não ocorra falha no software até o tempo t é definida como:

<p align="center">
  <img src="books/eduardo_delamaro/static/img-13-1.png" width="500">
</p>



#### 13.2.1.1. Função Confiabilidade

Na literatura clássica, a definição sobre confiabilidade amplamente adotada é: probabilidade de operação livre de falhas de um software, em um tempo e ambiente especificados.

Assim, a função Confiabilidade, também chamada de função de sobrevivência de um software, é definida como:

<p align="center">
  <img src="books/eduardo_delamaro/static/img-13-2.png" width="500">
</p>

Quando uma base de tempo é determinada, as falhas no software podem ser expressas por várias funções, como: função Taxa de Talhas, função de Falhas Acumuladas, função Intensidade de Falhas, tempo médio para falhas (MTTF) e tempo médio entre falhas (MTBF).

Para determinar o comportamento de falhas no software, basta observar o comportamento de uma dessas funções. Ou seja, para determinar a forma funcional do modelo que representa o comportamento das falhas no software, é só determinar a forma funcional de apenas uma dessas funções. O comportamento das demais funções pode ser explicitamente determinado. Alguns modelos de confiabilidade de software são determinados por suposições no comportamento da taxa de falhas, outros são determinados por suposições no comportamento da função de Falhas Acumuladas.

#### 13.2.1.2. Função Taxa de Falhas

Para descrever o ritmo de ocorrência das falhas em um sistema, a taxa de falhas é um conceito bastante utilizado. Teoricamente, a taxa de falhas é definida como a probabilidade de que uma falha por unidade de tempo ocorra num intervalo [t, t + Δt], dado que o sistema não
falhou até o tempo t. Na prática, a taxa de falhas é a razão entre o incremento do número de falhas e o incremento de tempo correspondente. Assim, usando a probabilidade condicional, tem-se que:

<p align="center">
  <img src="books/eduardo_delamaro/static/img-13-3.png" width="500">
</p>

A taxa de falhas instantânea, Z(t), também conhecida como taxa de risco associada à variável aleatória T , é definida como:

<p align="center">
  <img src="books/eduardo_delamaro/static/img-13-4.png" width="500">
</p>

Ou seja, a taxa de risco é definida como o limite da taxa de falhas quando o intervalo Δt tende a zero (Δt → 0).

A taxa de risco é uma taxa de falhas instantânea no tempo t, dado que o sistema não falhou até o tempo t. Embora haja uma pequena diferença entre a taxa de falhas e a taxa de risco, normalmente usa-se Z(t) como taxa de falhas.

A taxa de falhas se altera ao longo do tempo de vida do sistema. A Figura 13.1 ilustra o comportamento da taxa de falhas de alguns sistemas.

A Região I, conhecida como fase de depuração, representa as falhas iniciais do sistema. Nessa região a taxa de falhas tende a decrescer com o tempo.

A Região II, conhecida como período de vida útil do sistema ou fase de operação, representa as falhas causadas por eventos aleatórios ou por condições de stress do sistema. Nessa região a taxa de falhas permanece constante com o tempo.

A Região III representa a fase de desgaste do sistema, caracterizada pelo crescimento na taxa de falhas em função do tempo.

<p align="center">
  <img src="books/eduardo_delamaro/static/fig-13-1.png" width="600">
</p>

A confiabilidade de software é semelhante à confiabilidade de hardware, tendo em vista que ambas são processos probabilísticos e podem ser descritas por distribuições de probabilidades. Contudo, a confiabilidade de software é diferente da confiabilidade de hardware no sentido de que o software não se desgasta com o tempo, ou seja, a confiabilidade não decresce com o tempo. Conseqüentemente, a Região III não se aplica à confiabilidade de software. No software, geralmente, a confiabilidade cresce na fase de teste e na fase de operação, desde que as falhas sejam removidas quando detectadas. No entanto, pode ocorrer um decréscimo na confiabilidade devido a alterações abruptas no ambiente de operação do sistema ou modificações incorretas na manutenção.

Considerando-se que o software é constantemente modificado em seu ciclo de vida, tornase inevitável a consideração de que a taxa de falhas seja variável.

Diferentemente dos defeitos de hardware que, na maioria das vezes, são defeitos físicos, os defeitos de software são defeitos de projeto, difíceis de visualizar, classificar, detectar e remover. Como resultado, a confiabilidade de software é muito mais difícil de se medir e analisar. Normalmente, a teoria de confiabilidade de hardware está fundamentada na análise de processos estacionários porque somente os defeitos físicos são considerados. Contudo, com o crescimento da complexidade dos sistemas e a introdução de defeitos no projeto, a teoria de confiabilidade de software baseada em processos estacionários torna-se inconveniente. Isso torna a confiabilidade de software um problema desafiante que requer o emprego de vários métodos.

A taxa de falhas ideal para o software é decrescente. A Figura 13.2 dá uma idéia de seu comportamento em função do tempo.

Ao se observar o comportamento da taxa de falhas em algum ponto, por meio de evidência estatística, é possível prever o comportamento da taxa de falhas em um tempo futuro. Com isso, os modelos de confiabilidade de software podem prever o tempo adicional necessário para o teste do software até que se atinja o objetivo especificado – a taxa de falhas desejada. Pode-se também estimar a confiabilidade ao término do teste.

<p align="center">
  <img src="books/eduardo_delamaro/static/fig-13-2.png" width="500">
</p>

Quando se considera crescimento de confiabilidade, uma medida usual é a confiabilidade condicional. Dado que o sistema teve n−1 falhas, a confiabilidade condicional é a função de sobrevivência associada à n-ésima falha do sistema. A confiabilidade condicional é de interesse quando o sistema está em fase de desenvolvimento, período em que se observa o tempo para a próxima falha. Quando o sistema está liberado e em fase operacional, o interesse passa a ser o intervalo de tempo livre de falhas e, nesse caso, os instantes de falha não são necessariamente condicionados às falhas anteriores. O interesse é a confiabilidade em um dado intervalo de tempo, independentemente do número de falhas ocorridas anteriormente.

#### 13.2.1.3. Função de Falhas Acumuladas

A função de Falhas Acumuladas, também denominada função Valor Médio, é uma maneira alternativa de caracterizar a ocorrência aleatória das falhas em um software. A função de Falhas Acumuladas descreve o crescimento da curva de Falhas Acumuladas e, assim, considera o número de falhas ocorridas no software até um tempo t. A função Valor Médio é uma maneira alternativa de representar o processo de falhas no software, e, assim, o comportamento futuro pode ser estimado por uma análise estatística do comportamento dessa curva de crescimento.

Teoricamente, o número de falhas acumuladas até o tempo t pode ser representado por uma variável aleatória M(t) com um valor médio μ(t). Isto é, μ(t) representa a função valor médio do processo aleatório.

A Figura 13.4 representa um comportamento típico da função Valor Médio.

O processo aleatório pode ser completamente especificado, assumindo-se uma distribuição de probabilidades para a variável aleatória M (t) para algum t.

Como M (t) assume somente valores inteiros, as correspondentes distribuições de probabilidades devem ser do tipo discretas. As distribuições de probabilidades Poisson e Binomial são bastante utilizadas para descrever o processo aleatório M(t).

<p align="center">
  <img src="books/eduardo_delamaro/static/fig-13-3.png" width="500">
</p>

#### 13.2.1.4. Função Intensidade de Falhas

A função Intensidade de Falhas λ(t) representa a taxa de variação instantânea da função Valor Médio. Isto é, representa o número de falhas ocorridas por unidade de tempo. Por exemplo, pode se dizer que houve 0,01 falha/hora ou então que houve uma falha a cada 100 horas.

A função Intensidade de Falhas representa a derivada da função Valor Médio e é um valor instantâneo. A Figura 13.5 ilustra o comportamento da função Intensidade de Falhas.

Observa-se que no início do teste do software a ocorrência de falhas é maior em uma unidade de tempo e, conseqüentemente, a função de Falhas Acumuladas ou função Valor Médio cresce rapidamente. À medida que o teste prossegue, o número de falhas por unidade de tempo tende a diminuir, ou seja, a função Valor Médio cresce mais lentamente. A taxa de variação da função Valor Médio tende a decrescer rapidamente conforme o teste procede. Com isso, a função Intensidade de Falhas tem um comportamento decrescente no tempo. 

#### 13.2.1.5. Tempo Médio para Falhas (MTTF)

A função Tempo Médio para Falhas, MTTF (Mean Time to Failure), representa o tempo esperado para a ocorrência da próxima falha, ou seja, é o tempo durante o qual o software funciona sem falhas. O MTTF é uma medida que pode ser utilizada para caracterizar o modelo de falhas de um sistema de software.

Suponha que um software esteja em teste e que tenham sido encontradas i − 1 falhas. Registrando-se os tempos entre as falhas como t1, t2, t3, ... ti−1, a média desses valores é o tempo médio antes de ocorrer a próxima falha. Um MTTF de 500 significa que uma falha pode ser esperada a cada 500 unidades de tempo.

Considere que cada defeito identificado tenha sido corrigido e que o sistema esteja novamente em execução. Pode-se utilizar Ti para denotar o tempo antes da próxima falha, que ainda será observada. Ti é uma variável aleatória e, quando se fazem declarações sobre a confiabilidade do software, fazem-se declarações de probabilidades sobre Ti.

### 13.2.2. Medição da Confiabilidade

Um meio simples de se medir a confiabilidade de um software é observar o tempo para a ocorrência da próxima falha. Certamente existe uma relação entre a confiabilidade do software e o tempo médio para a ocorrência da próxima falha. Pode-se imaginar que, à medida que o software se torna mais confiável, o tempo médio para a ocorrência da próxima falha tende a aumentar. Da mesma forma, se os tempos para a ocorrência da próxima falha são pequenos, isso significa que o software está falhando bastante e, por conseqüência, sua confiabilidade é baixa. Por outro lado, se os tempos para ocorrência da próxima falha são grandes, o software falha pouco e, por conseqüência, sua confiabilidade é alta. Logicamente, nessa maneira simples de medir a confiabilidade de um software, não se dá a devida atenção às suposições no comportamento das falhas no software.

Nesse contexto, o MTTF é próximo de zero quando a taxa de falhas do software é grande e próximo de 1 quando a taxa de falhas do software é pequena. Utilizando essa relação, pode-se calcular a medida da confiabilidade de um software como: 

<p align="center">
  <img src="books/eduardo_delamaro/static/img-13-5.png" width="200">
</p>

Em um processo de teste do software, à medida que ocorrem as falhas e removem-se os defeitos, a confiabilidade é uma medida que informa se o software está sendo ou não aperfeiçoado. Se os tempos entre as falhas permanecem os mesmos, então tem-se uma con- fiabilidade estável. Se os tempos entre as falhas aumentam, então tem-se um crescimento da confiabilidade do software.

A confiabilidade do software também pode ser medida quando se conhece a distribuição de probabilidades de ocorrência das falhas. Isto é, quando o comportamento da ocorrência das falhas pode ser descrito com uma função Densidade de Probabilidade f(t). Conhecida a função f(t), a confiabilidade pode ser calculada pela Equação (13.2).

Pode-se desejar, também, saber a probabilidade de que o software opere sem falhas em um intervalo de tempo [t1 , t2]. Assim, a confiabilidade do software nesse intervalo pode ser calculada como:

<p align="center">
  <img src="books/eduardo_delamaro/static/img-13-6.png" width="300">
</p>

Pode ser mostrado que:

<p align="center">
  <img src="books/eduardo_delamaro/static/img-13-7.png" width="200">
</p>

### 13.2.3. Função de Confiabilidade

A modelagem sobre a confiabilidade de software normalmente envolve a utilização de uma distribuição de probabilidades do tempo para ocorrência das falhas no software. Dependendo do conjunto de suposições, a função de confiabilidade do modelo pode envolver uma distribuição de probabilidades desconhecida sobre o tempo de falhas no software. Contudo, de uma maneira geral, a maioria dos modelos é fundamentada em distribuições de probabilida des conhecidas na literatura.

Assim, nesta subseção são apresentadas as principais distribuições de probabilidades utilizadas em modelos de confiabilidade de software.

#### 13.2.3.1. Distribuição exponencial

A distribuição exponencial é a distribuição de probabilidades mais conhecida e mais amplamente utilizada devido à sua simplicidade e grande aplicabilidade. A exponencial é um bom modelo de distribuição de probabilidades para descrever o tempo T entre a ocorrência de dois eventos consecutivos.

As funções Densidade de Probabilidade f (t) e Distribuição de Probabilidade F (t) têm as formas:

<p align="center">
  <img src="books/eduardo_delamaro/static/img-13-8.png" width="200">
</p>

<p align="center">
  <img src="books/eduardo_delamaro/static/img-13-9.png" width="200">
</p>

em que t > 0 e λ > 0, λ é um parâmetro. A Figura 13.6 ilustra o comportamento da função Densidade de Probabilidades Exponencial.

<p align="center">
  <img src="books/eduardo_delamaro/static/fig-13-6.png" width="600">
</p>

A região hachurada na Figura 13.6 representa a probabilidade de não ocorrência de falhas até o tempo t o . Observa-se que para pequenos intervalos de tempo é grande a probabilidade de não ocorrência de falhas. Por outro lado, para grandes intervalos de tempo é pequena a probabilidade de não ocorrência de falhas.

O emprego da distribuição exponencial deve ter a hipótese de que o sistema tem uma taxa de falhas constante. Seu uso é recomendado quando o software tem uma taxa de falhas constante, isto é, na Região II da Figura 13.1 anteriormente discutida.

Para uma certa classe de modelos de confiabilidade de software, a suposição é que o número de falhas acumuladas em um tempo t segue uma distribuição de Poisson, ou seja, é regida por um processo de Poisson, e que o tempo entre falhas segue uma distribuição exponencial. Dessa forma, muitos modelos de confiabilidade de software admitem que o tempo de falha do software ou então o tempo entre falhas segue uma distribuição exponencial.

É evidente que a distribuição de probabilidades não diz quando as falhas ocorrem. No entanto, ela fornece informações sobre o processo aleatório de ocorrência das falhas.

#### 13.2.3.2. Distribuição de Weibull

A distribuição de probabilidades de Weibull, como outras distribuições, tem uma grande aplicação em confiabilidade devido à sua adaptabilidade. Dependendo dos valores dos parâmetros, pode-se ajustar a muitos conjuntos de dados sobre falhas. Ao utilizar essa distribuição, assume-se que, no processo de falhas do software, a variável aleatória T (tempo entre falhas) segue a distribuição de Weibull.

<p align="center">
  <img src="books/eduardo_delamaro/static/fig-13-7.png" width="200">
</p>

#### 13.2.3.3. Distribuição Gamma

A distribuição Gamma tem propriedades semelhantes às da distribuição de Weibull. Com variações nos parâmetros, essa distribuição pode-se ajustar a vários conjuntos de dados de falhas. A função Densidade de Probabilidades f(t) tem a forma:

<p align="center">
  <img src="books/eduardo_delamaro/static/fig-13-8.png" width="200">
</p>

## 13.3. Modelos de Confiabilidade

Na seção anterior foram vistos os fundamentos da teoria de confiabilidade de software, requisito necessário para o bom entendimento dos modelos de confiabilidade de software. Nesta seção são discutidos aspectos gerais sobre modelos de confiabilidade de software, iniciando com a fundamentação básica da modelagem de confiabilidade de software. As principais classificações dos modelos de confiabilidade de software existentes na literatura são apresentadas de acordo com a visão de cada autor. As três principais abordagens de modelagem de confiabilidade de software são também apresentadas.

### 13.3.1. Modelagem

Um dos aspectos particulares da engenharia de confiabilidade de software que tem recebido a maior atenção é a modelagem da confiabilidade de software. Para se modelar a confiabilidade de software é necessário considerar os principais fatores que afetam a confiabilidade, que são: a introdução de defeitos, a remoção de defeitos e, finalmente, o ambiente no qual o software é executado.

A introdução de defeitos depende das características do código desenvolvido (código criado inicialmente ou código modificado) e das características do processo de desenvolvimento. As características do processo de desenvolvimento incluem as técnicas de desenvolvimento de software, as ferramentas utilizadas e, por fim, o nível de experiência da equipe de desenvolvimento. Além disso, como Musa e Okumoto observaram, defeitos em software somente podem ser definidos quando são descobertos por meio de uma falha e, assim, não faz sentido contar o número de defeitos em um programa sem que tal programa tenha sido executado por um longo período de tempo. Em geral, muitos pesquisadores de confiabilidade de software têm considerado esse problema modelando a falha no software em vez de defeitos no software.

A remoção de defeitos no software depende do tempo de operação do software, do perfil operacional e da qualidade da atividade de reparos. Alguns pesquisadores contestam essa dependência em relação ao tempo, afirmando que observar o comportamento do software em função do tempo não faz sentido se não houver o controle do que está sendo executado no código. A observação do tempo é uma herança da confiabilidade de hardware, na qual o tempo é um fator importante do comportamento. O ambiente de operação do software depende diretamente do perfil operacional do usuário.

Dado que alguns fatores são de natureza probabilística e operam no tempo, os modelos de confiabilidade de software geralmente são formulados em termos de processos aleatórios. Em termos gerais, os modelos se distinguem pela distribuição de probabilidade do tempo entre falhas ou distribuição do número de falhas observadas e, também, pela natureza da variação do processo aleatório com o tempo.

Um modelo matemático é chamado de modelo de confiabilidade de software se for utilizado para obter uma medida da confiabilidade do software. Todos os modelos matemáticos de confiabilidade de software são de natureza probabilística e, assim, tentam, de algum modo, especificar a probabilidade de ocorrência de falhas do software. O objetivo final é quantificar a confiabilidade do software de uma maneira tão precisa quanto possível.

Um modelo de confiabilidade de software especifica a forma funcional da dependência do processo de falhas sobre os fatores mencionados, isto é, faz uma descrição probabilística precisa da confiabilidade baseada nas suposições a priori sobre esses fatores que afetam a confiabilidade e, também, baseada nos resultados obtidos pelos dados experimentais. Várias são as formas matemáticas para se descrever o processo de falhas. Uma forma específica pode ser determinada de uma maneira geral ao se estabelecerem os valores dos parâmetros do modelo por estimação – aplicação de procedimentos de inferência estatística aplicados aos dados de falhas; ou por predição – determinação das propriedades do software e do processo de desenvolvimento (pode ser feita antes da execução do software).

Sempre existe uma incerteza na determinação de uma forma específica. Assim, geralmente se expressam os parâmetros em termos de intervalos de confiança. Uma vez que a forma específica do modelo foi determinada, algumas características do processo de falhas podem ser determinadas. Alguns modelos apresentam uma expressão analítica para essas características, que são:

- 1. o número médio de falhas observadas em algum ponto no tempo;
- 2. o número médio de falhas em um intervalo de tempo;
- 3. a intensidade de falhas em algum ponto no tempo;
- 4. a distribuição de probabilidade do tempo entre falhas.

A predição do comportamento futuro pressupõe que os valores dos parâmetros do modelo não se alteram nos próximos períodos. De um modo geral, os modelos de confiabilidade de software estão baseados em uma execução estável do software em um ambiente constante.

As medidas de confiabilidade de software podem ser de grande valor para os engenheiros de software, para os gerentes e para os usuários. Com essas medidas, pode-se avaliar o status de desenvolvimento durante as fases de um projeto e tem-se a possibilidade de monitorar o desempenho operacional do software, podendo-se, ainda, controlar as alterações feitas no software. Finalmente, o entendimento quantitativo da qualidade do software e dos vários fatores que afetam a qualidade enriquece o conhecimento dos processos de desenvolvimento e dos produtos de software.

No entanto, deve ser ressaltado que muitos dos modelos existentes na literatura são testados com dados simulados ou com dados reais que, na maioria das vezes, não foram coletados para tal propósito. O resultado é que algumas suposições básicas desses modelos ou abordagens são violadas. Além disso, é importante salientar que a modelagem de confiabilidade de software é apenas uma das muitas ferramentas da engenharia de software. Como tal, a modelagem não responde a todos os questionamentos relativos à gerência do software. A modelagem de confiabilidade deve ser encarada como uma técnica adicional que ajuda a fazer um julgamento realístico sobre o status do software. Devido às controvérsias existentes sobre qual é o melhor modelo e por causa da incerteza sobre o desempenho das abordagens sobre a modelagem da confiabilidade, deve ser enfatizado que, entre os modelos existentes, recomenda-se aplicar aquele que melhor se ajusta aos dados. A estimativa de confiabilidade pode ser utilizada como mais uma fonte de informação na determinação do status do software.

### 13.3.2. Classificação de Modelos de Confiabilidade

Nesta subseção são apresentadas algumas formas de classificação dos modelos de confiabilidade de software. Cada autor adota um ponto de vista diferente para fazer sua classificação, mas algumas concordâncias têm estreita relação entre si. 

Schick e Wolverton distinguem duas abordagens na modelagem de confiabilidade de software:
- abordagem baseada no domínio dos dados de entrada;
- abordagem baseada no domínio do tempo.

Ramamoorthy e Bastani apresentam um esquema de classificação no qual os modelos se aplicam nas fases do ciclo de vida do sistema. Isto é, modelos aplicáveis na fase de desenvolvimento, na fase de validação, na fase de operação, na fase de manutenção e, finalmente, modelos que se aplicam para medir a correção do software. Nesta classificação, alguns modelos se aplicam a mais de uma fase.

Goel classifica os modelos segundo:
- 1. A natureza do processo de falhas
  - (a) Modelos baseados no tempo entre falhas;
  - (b) Modelos baseados no número de falhas num intervalo de tempo.
- 2. A forma de aplicação dos modelos
  - (a) Modelos de implante de defeitos;
  - (b) Modelos baseados no domínio dos dados de entrada.

Mellor classifica os modelos de confiabilidade de acordo com as hipóteses sobre o mecanismo de falhas e com a estrutura matemática: modelos estruturais, que permitem a combinação da confiabilidade dos módulos na obtenção da confiabilidade global do sistema, e modelos que levam em conta somente o comportamento global do sistema. Nessa segunda classificação os modelos se dividem em modelos de tempo entre falhas e modelos que interpretam falhas como a manifestação de defeitos do sistema, supondo que cada defeito dá origem a uma falha com uma certa taxa.

Musa e Okumoto fazem uma classificação dos modelos em função de cinco atributos diferentes:
- 1. domínio do tempo: tempo cronológico e tempo de execução;
- 2. categoria finita ou infinita: característica do modelo que se relaciona ao número total de falhas que pode ser observado em um tempo infinito de teste;
- 3. tipo: característica do modelo que se relaciona à distribuição do número de falhas observadas no tempo t. Dois tipos de distribuição importantes são Binomial e Poisson;
- 4. classe (somente para modelos de categoria finita): característica do modelo que se relaciona com a forma funcional da intensidade de falhas expressa em termos do tempo (vide a função λ(t) – função Intensidade de Falhas na Equação (13.8)). As principais 
classes são: Exponencial, Weibull, Pareto e Gamma;
- 5. família (somente para modelos de categoria infinita): característica do modelo que se relaciona à forma funcional da intensidade de falhas expressa em termos do número esperado de falhas observadas (λ(μ(t))). As principais famílias são: Geométrica, Linear Inversa, Polinomial Inversa e a família Potência.

Independentemente de qualquer classificação, três abordagens são identificadas na literatura: modelos de implante de defeitos, modelos baseados no domínio dos dados e modelos baseados no domínio do tempo.

## 13.4. Principais Modelos de Confiabilidade

Nesta seção são apresentados alguns dos mais importantes modelos de confiabilidade de software amplamente citados na literatura, tanto do ponto de vista histórico quanto de suas aplicações. Os modelos são apresentados considerando-se as três principais abordagens anteriormente identificadas. São apresentados também os modelos baseados na cobertura do teste, uma abordagem recente de modelos de confiabilidade de software.

O propósito desta seção é apresentar um levantamento dos principais modelos, considerando as abordagens existentes de modelagem e estimação da confiabilidade de software. Não se pretende esgotar o assunto, mas, em uma forma sucinta, apresentar as suposições fundamentais do modelo, os dados necessários para sua aplicação e, finalmente, sua forma funcional. Não se apresentam os detalhes sobre a estimação dos parâmetros de cada modelo nem a dedução matemática de sua forma funcional.

<p align="center">
  <img src="books/eduardo_delamaro/static/tabela-13-5.png" width="700">
</p>

<p align="center">
  <img src="books/eduardo_delamaro/static/tabela-13-6.png" width="700">
</p>

### 13.4.1. Modelos de Implante de Defeitos


