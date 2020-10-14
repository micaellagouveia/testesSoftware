# Capítulo 13 - Confiabilidade

## 13.1. Introdução

Com o constante desenvolvimento da tecnologia, os sistemas computacionais têm sido requisitados em quase todas as áreas da atividade humana. Especificamente nos últimos anos, softwares específicos foram desenvolvidos para aplicações críticas, como sistemas de controle de usinas nucleares, sistemas de controle aeroespacial, controle de processos na área médica e muitas outras áreas de risco no campo industrial. A natureza de sistemas computacionais em termos de precisão de tempo e em termos de comportamento repetivivo faz do software ideal para áreas nas quais um simples engano pode causar efeitos extremamente danosos.

Essa crescente dependência em relação ao software tem conscientizado tanto os usuários, que cada vez mais exigem softwares confiáveis, como também a industria de software, no sentido de desenvolver produtos de alta qualidade.

O desenvolvimento de software que atende as exigências dos usuários, com o nível de confiabilidade exigido é um tarefa extremamente difícil. Essa dificuldade é devido o fato de software ser uma entidade lógica que não possui termos de valor concreto que definem a qualidade do produto.

A confiabilidade é uma característica que tem sido extensivamente considerada na análise da qualidade do software, pois se um software não é confiável, pouco importa se outras características da qualidade são aceitáveis.

Ao atribuir-se um grau de confiabilidade ao software, o objetivo é quantificar alguns aspectos desse software que, devido à presença de inevitável de defeitos (bugs), está sujeito a falhas durante seu período de utilização. Assim, o estudo da confiabilidade de software caracteriza-se como uma abordagem analítica que está baseada nos conceitos de métricas, medidas e modelos.

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