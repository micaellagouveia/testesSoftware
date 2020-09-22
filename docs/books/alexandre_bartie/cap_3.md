# 3. Definindo Qualidade de software

Qualquer decisão tomada durante o processo de desenvolvimento do software pode comprometer sua qualidade final. Se desejarmos produzir software com alta qualidade, é necessário investir em qualidade em todos os pontos do processo.

## 3.1. Dimensão da Qualidade do software

Softwares mal testados provocam prejuízos enormes às organizações. Um simples erro interno do projeto poderá encadear requisições de compras desnecessárias, solicitar manutenções de equipamentos antes do período ideal, produzir estatísticas falsas de produtividade, distribuir rendimentos de forma desproporcional, entre outros. 

É impossível obter um software de qualidade com processos de desenvolvimento frágeis e deficientes, portanto, não é possível estabelecer um processo de garantia da qualidade que não enfoque simultaneamente o produto tecnológico e o processo de desenvolvimento desse software.

Assim, podemos estabelecer duas dimensões fundamentais para atingirmos a qualidade do software: a dimensão da qualidade do processo e da qualidade do produto.

### 3.1.1. Dimensão da Qualidade do processo

Quando estamos diante do desafio de garantir a qualidade de um software, estamos, na verdade, estabelecendo uma cultura de não-tolerância a erros, ou seja, estamos estruturando processos que possuam mecanismos de inibição e impedimentos de falhas, possibilitando que os diversos artefatos gerados durante o ciclo de desenvolvimento tenham procedimentos que avaliam sua qualidade, possibilitando a identificação prematura de defeitos nesses artefatos.

O termo "artefato" nesse contexto deve ser entendido como todos os requisitos levantados, modelos e especificações de negócio, arquitetura física, modelo de dados e classes, distribuição de componentes, análise de custos, projeções financeiras, ou seja, todos os documentos gerados durante o desenvolvimento do software.

### 3.1.2. Dimensão da Qualidade do produto

Todas atividades que tenham por objetivo "estressar" telas e funcionalidades de um sistema informatizado podem ser caracterizadas na dimensão de garantia da qualidade do produto tecnológico.

Apesar de bastantes empregadas nas organizações, o grau de eficiência dessas atividades é assustadoramente baixos, o que incentiva as empresas a substituírem tais atividades pela correção de problemas. Os principais motivos para essa baixa eficiência é a falta de planejamento das atividades de teste, ausência de testes que validem funcionalidades antigas e ausência de um processo de automação dos testes e conferências.

## 3.2. Medindo a Qualidade através dos Testes

O processo de qualidade de software utiliza-se dos testes em todo o ciclo de desenvolvimento, de forma a garantir tanto o processo de engenharia quanto o produto de software desenvolvido.

### 3.2.1. Testes que Garantem a Qualidade do Processo

A qualidade dos processos pode ser medidas através de testes aplicados em documentos gerados em cada fase do desenvolvimento. Como cada etapa deve produzir um conjunto de documentos, é possível estabelecer a qualidade nas várias fases do ciclo de desenvolvimento através da qualidade dos documentos produzidos. Esses testes são conhecidos como testes de verificação.

### 3.2.2. Testes que Garantem a Qualidade do produto

A qualidade dos produtos de software pode ser garantida através de sistemáticas aplicações de testes nos vários estágios do desenvolvimento da aplicação. Esses testes são conhecidos como testes de validação, isso porque, quando construímos uma unidade de software, validamos sua estrutura interna e sua aderência aos requisitos estabelecidos. Avaliamos sua integração com as demais unidades de software, validando as interfaces de comunicação entre componentes. Quando determinado subsistema ou mesmo a solução está finalizada, validamos a solução tecnológica como um todo, submetendo a testes de todas as catergorias possíveis.

Os testes de software, em sua maioria, podem sofrer um alto nível de automação, o que possibilita a criação de complexos ambientes de testes que simulam diversos cenários de utilização. Quanto mais cenários simulados, maior o nível de validação que obtemos do produto, caracterizando maior nível de qualidade do software desenvolvido.

### 3.2.3. Definição Comum de Testes

De forma geral, todas as equipes de desenvolvimento aplicam testes em seus softwares, sejam eles bem planejados e estruturados ou não. O fato é que esses testes não são suficientes para detectar os erros que estão inseridos dentro de uma aplicação. Um dos motivos básicos para que isso ocorra é a forma como esses profissionais encaram os testes de software. Geralmente, esses profissionais encaram as atividades de teste como a avaliação ou comprovação de que tudo está funcionando adequadamente. Essa visão sobre testes não é adequada pois os desenvolvedores são podem está emocionalmente envolvidos com o software projetado e pode existir o desejo de provar que o resultado do seu esforço funciona, quando o objetivo de desenvolver testes é justamente o contrário, é mostrar o mais cedo possível que algo não está funcionando.

### 3.2.4. A Definição Correta sobre Testes

Entender que o objetivo dos testes é "provar que algo não funciona" é um avanço significativo na compreensão de um processo de qualidade de software. Teste é um processo sistemático e planejado que tem por finalidade única a identificação de erros.

### 3.2.5. Limitações dos Testes

Devemos ter em mente que os testes podem ser usados para mostrar a presença de erros, mas nunca sua ausência. A razão óbvia para essa conclusão é o fato de que um processo de qualidade, por melhor que ele seja, não conseguirá cobrir todas as infinitas combinações existentes em um ambiente de execução real.

A qualidade de um software é definida pelo número de requisitos que foram adequadamente testados e estão em conformidade com o especificado. Obter mais qualidade significa aumentar o grau de cobertura e testar novos requisitos e inserir novos cenários que não estavam sendo considerados. Quanto maior a extensão dos testes, maior será a qualidade do software e menor será os riscos de erros, uma vez que mais cenários foram testados e adequadamente validados.


### 3.2.6. Atitude Zero-defeito

Obter um software com zero defeitos é algo inatingível, devido a complexidade envolvida e pelo número altíssimo de situações existentes. Não podemos nos enganar, sempre existirão erros a serem descobertos, porém, o desafio de um processo de garantia de qualidade é justamente tornar esses riscos o mais próximo possível do zero.

A qualidade de software trabalha com o conceito "zero-defeito", que representa a não-tolerância a erros de dentro de um processo de qualidade de software. O objetivo é definir um processo que contenha mecanismos de inibição de defeitos, impedimento que falhas sejam criadas e propagadas para fases seguintes. Um processo que implementa o conceito "zero-defeito" é desenhado para minimizar a incidência de problemas.

## 3.3. Os Pilares da Qualidade de Software