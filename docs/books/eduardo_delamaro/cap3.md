# Capítulo 3 - Teste Baseado em Modelos


## 3.1. Introdução

Uma especificação é um documento que representa o comportamento e as características que um sistema deve possuir. Ela pode ser definida de diversas formas. Por exemplo, pode-se criar um documento que descreve textualmente o comportamento em uma linguagem natural. Um risco potencial com a descrição textual é a possibilidade de se incluírem inconsistências na especificação, uma vez que as linguagens naturais geralmente são ambíguas e imprecisas. O uso de outras formas de especificação torna-se importante em contextos nos quais tais imprecisões podem causar problemas.

É importante notar que o uso de linguagem natural não é, por si só, um problema. Afinal, o que é necessário é a precisão e o rigor da especificação. Por exemplo, uma descrição textual feita de forma rigorosa e clara pode ser mais fácil de se compreender e implementar do que uma especificação formal complexa. 

A modelagem permite que o conhecimento sobre o sistema seja capturado e reutilizado durante diversas fases de desenvolvimento. Boa parte da atividade de teste é gasta buscando-se identificar o que o sistema deveria fazer. Ou seja, antes de se perguntar se o resultado está correto, deve-se saber qual seria o resultado correto. Um modelo é muito importante nessa tarefa, pois, se bem desenvolvido, captura o que é essencial no sistema. No caso de modelos que oferecem a possibilidade de execução (ou simulação, como é muitas vezes o caso), o modelo pode ser utilizado como um oráculo, definindo a linha que separa o comportamento adequado do comportamento errôneo. Contudo, utilizar o modelo como oráculo coloca a seguinte questão: como saber que o modelo está correto? Ou seja, o modelo torna-se um artefato que deve ser testado tanto quanto o próprio sistema. Uma vez verificado o problema de o modelo estar ou não adequado (ou, ao menos, aumentada a confiança de que ele esteja), ele é extremamente valioso para o teste, servindo tanto como oráculo quanto como base para a geração de scripts e cenários de teste.

Durante a realização dos testes, um grande obstáculo é determinar exatamente quais são os objetivos de teste, ou seja, quais itens serão testados e como. Em geral, especificações não rigorosas deixam grande margem a opiniões e especulações. A forma da especificação pode variar de um grafo de fluxos de chamadas intermódulos a uma guia de usuários. Uma especificação clara é importante para definir o escopo do trabalho de desenvolvimento e, em especial, o de teste. Se a única definição precisa de o que o sistema deve fazer é o próprio sistema, os testes podem ser improdutivos. 

A criação de modelos não é uma nova habilidade que deve ser adquirida. Os testadores sempre constroem um modelo, ainda que informal. (De outra forma, não haveria como determinar se o comportamento foi aceitável.) O ponto é qual é o formato do modelo. Um modelo informal ou que está apenas na cabeça do testador dificulta a automatização dos testes. Para escrever um script de teste ou um plano de teste, o testador deve entender os passos básicos necessários para usar o sistema.


## 3.2. Máquinas de Estados Finitos

Uma Máquina de Estados Finitos é uma máquina hipotética composta por estados e transições. Cada transição liga um estado a a um estado b (a e b podem ser o mesmo estado). A cada instante, uma máquina pode estar em apenas um de seus estados. Em resposta a um evento de entrada, a máquina gera um evento de saída e muda de estado. Tanto o evento de saída gerado quanto o novo estado são definidos unicamente em função do estado atual e do evento de entrada. Uma Máquina de Estados Finitos pode ser representada tanto por um diagrama de transição de estados quanto por uma tabela de transição. Em um diagrama de transição de estados, os estados são representados por círculos e as transições são representadas por arcos direcionados entre estados. Cada arco é rotulado com a entrada que gera a transição e a saída que é produzida, usando o formato entrada:saída. Em uma tabela de transição, os estados são representados por linhas, e as entradas, por colunas.

Uma vez que, pela própria definição, o conjunto de estados atingíveis em uma Máquina de Estados Finitos é finito, é possível responder a quase todas as questões sobre o modelo, o que permite a automatização do processo de validação. No entanto, a classe de sistemas que podem ser modelados por uma máquina de estados finitos é consideravelmente limitada. Mesmo para os casos nos quais a modelagem é possível, o modelo resultante pode ser excessivamente grande. Por exemplo, a impossibilidade da representação explícita da concorrência leva à explosão combinatória do número de estados. Com o propósito de aumentar o poder de modelagem, foram propostas várias extensões às Máquinas de Estados Finitos.

Diz-se que a MEF é completamente especificada se ela trata todas a entradas em todos os estados. Caso contrário, ela é parcialmente especificada. Para máquinas parcialmente especificadas o teste de conformidade é fraco. Caso contrário, ele é forte. Quando as transições não especificadas de uma MEF são completadas com fins de realização dos testes, diz-se que assume uma suposição de completude.

Uma MEF é minimal (ou reduzida) se na MEF não existem quaisquer dois estados equivalentes. Dois estados são equivalentes se possuem as mesmas entradas e produzem as mesmas saídas.

Uma MEF é determinística quando, para qualquer estado e para uma dada entrada, a MEF permite uma única transição para um próximo estado. Caso contrário, ela é não-determinística.


## 3.3. Sequências básicas

Os métodos de geração de casos de teste são fortemente baseados em algumas sequências básicas, as quais são utilizadas para se obter um resultado parcial importante.

### 3.3.1. Sequências de sincronização

Uma sequência de sincronização para um estado s (expressa por SS(s)) é uma sequência de símbolos de entrada que leva a MEF ao estado s, independentemente do estado original da MEF. 

A sequência de sincronização é útil em situações nas quais se deseja garantir que a MEF vá para um estado em particular. Por exemplo, uma sequência de sincronização pode ser utilizada para posicionar a MEF no estado inicial sem a necessidade de uma operação de reset. Contudo, deve-se ter em mente que a sequência de sincronização da MEF não é necessariamente uma sequência de sincronização para a implementação, uma vez que a implementação pode conter falhas.

### 3.3.2. Sequência de distinção

Um sequência de distinção (DS) é uma sequência de símbolos de entrada que, quando aplicada aos estados da MEF, produzem saídas distintas para cada um dos estados. Ou seja, observando-se a saída produzida pela MEF como resposta à DS, pode-se determinar em qual estado a MEF estava originalmente.

Uma DS pode não existir. Isto é, não existe uma sequência capaz de distinguir todos os estados. Existem outras sequências que podem ser utilizadas nesse caso, como as UIO e o conjunto W, apresentados nas seções seguintes.

### 3.3.3. Sequências UIO

Como pôde ser observado na seção anterior, nem todas as MEFs possuem DSs. Entretanto, mesmo nessas situações, pode-se fazer a distinção entre um estado e os demais. Para isso, usa-se uma Sequência Única de Entrada e Saída (UIO). Uma UIO é utilizada para verificar se a MEF está em um estado particular. Assim, para cada estado da MEF, pode-se ter uma UIO distinta. Isso é verdade apenas se forem consideradas tanto as entradas como as saídas. A sequência de entradas da UIO de um estado pode ser igual à sequência de entradas da UIO de outro estado. Assim, pode-se concluir que se uma MEF possui uma DS, ela também possui UIOs para todos os seus estados. Contudo, em geral, pode-se obter UIOs mais curtas.

### 3.3.4 Conjunto de caracterização

Um conjunto de caracterização é um conjunto de sequências de entrada que podem, em conjunto, identificar qual era o estado original.

## 3.4. Geração de sequências de teste

Uma sequência de teste, nesse contexto, é uma sequência de símbolos de entrada derivada da MEF que são submetidos à implementação correspondente para verificar a conformidade da saída gerada pela implementação com a saída especificada na sequência de teste. Os métodos mais clássicos para a geração de sequências de teste a partir de MEFs são:

**Método TT (Transition Tour)** Para uma dada MEF, o transition tour é uma sequência que parte do estado inicial atravessa todas as transições pelo menos uma vez e retorna ao estado inicial. Permite a detecção de erros de saída, mas não garante erros de transferência, ou seja, erros em que a transição leva a MEF a um estado diferente do qual ela deveria levar.

**Método UIO (Unique input/output)** Produz uma sequência de identificação de estado. Não garante cobertura total dos erros, pois a sequência de entrada leva a uma única saída na especificação correta, mas isso não é garantido para as implementações com erro.

**Método DS (Sequência de distinção)** Uma sequência de entrada é uma DS se a sequência de saída produzida é diferente quando a sequência de entrada é aplicada a cada estado diferente. A desvantagem desse método é que a DS nem sempre pode ser encontrada para uma dada MEF.

**Método W** É um conjunto de sequências que permite distinguir todos os estados e garante detectar os erros estruturais, sempre que a MEF for completa, mínima e fortemente conexa.

### 3.4.1. Método TT

O método TT é relativamente simples, quando comparado com os outros três métodos. Ele gera um conjunto de sequências que passam por todas as transições da MEF, ou seja, as sequências geradas cobrem todas as transições.

Em alguns casos, o conjunto de sequências é unitário, isto é, uma única sequência passa por todas as transições. Contudo, para algumas MEFs, pode não ser possível calcular uma única sequência. Por exemplo, a MEF pode possuir dois conjuntos de estados tais que, uma vez entrando em um deles, não se consegue chegar a um estado do outro conjunto, o que pode ser considerado um caso particular de MEF não completamente conexa. Nesse caso, pode-se utilizar um conjunto com mais sequências.

### 3.4.2. Método DS

O método DS utiliza a sequência de distinção DS para gerar as sequências de teste. São utilizadas também as sequências de sincronização. Assim, sua aplicabilidade fica condicionada à existência dessas sequências para a MEF em questão.

### 3.4.3. Método UIO
[...]

### 3.4.4. Método W
[...]

### 3.5. Comparação entre os métodos

Alguns aspectos tornam-se bastante importantes para a seleção de um determinado método de geração de sequências de teste, tais como as propriedades que o método exige que a MEF satisfaça, a aplicabilidade e o comprimento das sequências geradas.

A Tabela 3.8 apresenta um resumo comparativo de todas as propriedades necessárias à aplicação de cada método, assim como as sequências necessárias. Podemos observar que o método TT é o menos exigente.

Quanto à aplicabilidade, o método W é o que pode ser aplicado a qualquer MEF, uma vez que toda MEF minimal possui um conjunto de caracterização. Caso a MEF não seja minimal, ela pode ser reduzida para uma MEF minimal equivalente. Os demais métodos exigem que determinadas sequências existam, tais como a sequência de distinção, o que nem sempre é verdadeiro, mesmo para MEFs minimais.


Para MEFs completamente especificadas, os métodos UIO, DS e W são capazes de detectar falhas nas saídas de todas as transições. Dessa forma, eles são capazes de detectar erros de transferência (próximo estado incorreto), de operação (símbolo de entrada ou saída da transição incorretos) e de estados em excesso ou falta.

<div align='center'>
    <img src='books/eduardo_delamaro/static/tabela-3-8.png'>
</div>

## 3.6. Considerações finais

A utilização de modelos para auxiliar a condução de testes traz diversas vantagens. A possibilidade de se eliminar a ambiguidade, ou ao menos reduzi-la, auxilia na elaboração mais rigorosa das expectativas que o sistema deve satisfazer. Pode-se, portanto, obter maior rigor.

A possibilidade de automação é outra vantagem (talvez, a mais importante). Diversos métodos podem ser utilizados para sistematicamente derivar casos de teste a partir do modelo. Nesse capítulo, apresentamos uma visão geral sobre o teste baseado em modelos, assim como alguns métodos de geração de casos de teste. Os métodos apresentados foram escolhidos entre os mais importantes. Contudo, essa é uma linha de pesquisa ainda muito intensa, na qual se tentam resolver vários problemas tanto de ordem teórica quanto de ordem prática que
surgem da aplicação desses métodos em problemas reais. Por exemplo, em muitos casos, os modelos não apresentam as propriedades necessárias. Assim, os métodos e/ou os modelos devem ser adaptados ou estendidos.

