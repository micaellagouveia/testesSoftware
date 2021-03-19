# Capítulo 9 - Métodos Estruturados de Verificação

Os testes de verificação devem garantir a qualidade de todas as etapas do desenvolvimento de sistemas. A qualidade será obtida através da correta construção de documentos e a adequada realização das atividades previstas no processo corporativo de engenharia de software. Portanto, os testes de verificação devem concentrar-se em dois aspectos bem distintos: as atividades de verificação que focalizam as documentações, as chamadas revisões, e as que avaliam as atividades, as chamadas auditorias. As duas situações são consideradas métodos estruturados, pois possuem planejamento, regras de condução e necessitam de profissionais qualificados para desempenhar essas funções e acompanhar seu progresso.

<div align='center'>
    <img src='books/alexandre_bartie/imgs/figura-9-1.png'>
</div>

## 9.1. Revisões

A revisão é um processo “humano” de análise de determinado documento. Esse processo requer pessoas adequadamente treinadas para desempenhar seus papéis durante a condução das atividades de verificação. Existem muitas formas de organizar as sessões de revisões, sendo que cada uma delas possui suas características e particularidades. Para cada fase do processo de criação de documentos poderemos aplicar um tipo diferente de revisão: na fase de elaboração inicial do documento, poderemos aplicar a revisão isolada, cujo objetivo é fazer validações parciais do documento. Na fase de validação do documento poderemos aplicar a revisão formal, cujo objetivo é validar o documento finalizado com todos os grupos interessados. Na fase de divulgação, poderemos aplicar as reuniões de acompanhamento, cujo objetivo é garantir a leitura do documento por todas as pessoas-chave envolvidas.

<div align='center'>
    <img src='books/alexandre_bartie/imgs/figura-9-2.png'>
</div>

### 9.1.1. Revisões Isoladas

Esse é um método de verificação pouco explorado mas muito eficiente na detecção prematura de erros de definições e soluções registradas. Trata-se de uma verificação individual do material produzido, executada por alguém diferente do autor, que tem por objetivo revisar e identificar o maior número possível de problemas.

A idéia aqui é antecipar a revisão dos documentos com entregas de versões ainda não acabadas, para que sofra análise e julgamento sobre os tópicos já abordados. Isso possibilita correções nos documentos durante sua fase de concepção.

Essas revisões permitem o contato antecipado dos revisores com as documentações que estão sendo geradas, o que auxilia na familiaridade com o formato de como determinadas regras estão sendo organizadas e registradas.

O grande cuidado que devemos tomar aqui é para que as revisões não ocorram apenas de forma unilateral. Como a ação dos revisores será isolada, poderá um único revisor propor mudanças que prejudiquem uma visão integrada do problema. Como o autor pode ter essa visão de conjunto mais apurada, o revisor pode interpretar a negativa de mudanças como uma imposição do autor a alterações em seu trabalho.

Nesse caso, o autor deverá fazer uma rápida reunião para decidir qual caminho trilhar. Se essas situações tornarem-se muito recorrentes, as ações de revisões isoladas podem prejudicar o andamento de concepção do documento, atrasando os trabalhos. Isso indica que as áreas envolvidas não estão compreendendo a extensão dos problemas que estão sendo abordados. Neste caso, o melhor a fazer é propor uma reunião na qual seja explicado o propósito dos trabalhos para todo o grupo de revisores, de forma a não permanecerem dúvidas estruturais em relação à solução que está sendo documentada.

Outro grande problema aqui é a chamada “revisão superficial” dos documentos. Isso ocorre quando o revisor não está preparado para interpretar o documento ou tem pouca iniciativa para realizar sugestões ou mesmo críticas. A tendência neste caso seria apenas uma revisão superficial do documento, como erros gramaticais e sugestões estéticas, não sendo analisado o conteúdo das decisões apontadas, dando um falso parecer de qualidade sobre o documento. Quando executadas nesse formato, essas revisões serão pouco eficientes e detectarão poucos erros.

### 9.1.2. Revisões Formais

As revisões formais são as mais efetivas e bem estruturadas técnicas existentes de verificação. Baseiam-se em reuniões com um grupo de profissionais responsáveis em identificar falhas presentes em documentos gerados nas diversas etapas do desenvolvimento. A identificação de erros é obtida através da análise e discussão de tópicos presentes na documentação.

As revisões têm regras próprias que devem ser respeitadas, objetivando o maior sucesso da condução desses trabalhos, que visam à identificação do maior número possível de erros nas documentações.

O autor do documento estará presente somente para responder às dúvidas e eventuais questões levantadas pelos revisores, não podendo conduzir a reunião. Assim, evitamos que o autor desvie de assuntos complicados e omita trechos da documentação que não estão adequadamente finalizados. Com a participação limitada do autor, o documento poderá ser analisado de uma perspectiva diferente, possibilitando identificar de imediato potenciais interpretações equivocados sobre um determinado assunto.

Todos os participantes devem ter estudado e ter afinidade com o documento e assuntos tratados por este. Dessa forma, cada participante deve, individualmente, preparar-se para coletar o maior número possível de informações antes da referida reunião. Os profissionais envolvidos nesse processo devem ter experiências e conhecimentos diferentes, para que todas as decisões sejam analisadas por diversos ângulos, aumentando o nível de análise de cada tópico a ser discutido, uma vez que possuem uma perspectiva diferente dos autores dos documentos. Assim, suas contribuições serão fundamentais para o aperfeiçoamento da solução.

Após a execução das reuniões de revisão, é fundamental documentar tudo que foi discutido, os principais problemas detectados, suas correções e as sugestões de melhoria a serem executadas. Esse material deverá ser produzido pela equipe de garantia da qualidade de software que deverá apresentá-lo aos autores dos documentos. Os autores realizarão as mudanças e irão produzir uma nova versão da documentação, que deverá ser submetida a uma nova revisão, porém com um enfoque somente nos pontos modificados (lembre-se de que a primeira revisão apenas apontou imprecisões que deveriam ser corrigidas e essa nova revisão necessita avaliar se tais mudanças eliminaram os defeitos anteriormente apontados).

### 9.1.3. Reuniões de Acompanhamento

Essa forma de verificação é menos formal do que as reuniões de revisão, uma vez que não necessita de uma adequada preparação por parte dos participantes. Somente o apresentador (que é o autor do documento) prepara-se para a reunião, enquanto que os demais participantes simplesmente comparecem. O objetivo maior dessas reuniões é tornar o documento e o discurso familiar a todos os participantes, enquanto a detecção de erros torna-se uma preocupação secundária.

As reuniões de acompanhamento são interessantes porque permitem envolver um número maior de pessoas do que nas reuniões de inspeção, permitindo que mais pessoas envolvam-se na dinâmica do ciclo de desenvolvimento do software e, consequentemente, possuam mais colaboradores nesse processo.

Esses tipos de reuniões são, invariavelmente, menos eficientes do que as inspeções em termos de detecção de problemas. Isso ocorre pelo despreparo dos participantes e também pelo fato de ser o autor do documento quem conduz a dinâmica da reunião, sendo comum que determinados assuntos sejam estrategicamente não citados para que exista um sentimento de que tudo está indo muito bem. Essas reuniões devem substituir, com vantagens, as famosas “coletas de assinaturas”, que não incentivam os profissionais a debaterem as decisões registradas nos documentos.

Uma forma eficiente de conduzir essas reuniões é distribuindo o material a todos os participantes para que todos possam analisar as documentações em questão. Será agendada uma reunião na qual todos poderão debater dúvidas e divergências existentes e, somente no final desta, caso exista um consenso em relação à condução dos trabalhos e as decisões tomadas, é que efetivamente será realizada a coleta de assinaturas. Para a adequada efetividade desse método de verificação, todos que são afetados por aquelas documentações deveriam estar presentes na lista de assinaturas do documento e comparecer à reunião.

Isso evitaria o chamado efeito retardado: mudar as coisas depois que determinados assuntos já foram encerrados simplesmente porque alguns profissionais não interpretaram adequadamente todas as decisões registradas nos documentos e mesmo assim o assinaram. Na “coleta de assinaturas” é muito comum as pessoas não lerem adequadamente o material disponibilizado.

## 9.2. Auditorias

As auditorias concentram-se nas atividades críticas de um processo de engenharia de software. O principal objetivo das auditorias de qualidade é avaliar se em determinado projeto as diversas equipes estão respeitando o processo de desenvolvimento, se estão registrando os defeitos encontrados, se estão produzindo as atas de reuniões, se estão realizando as reuniões de revisões, se estão realizando as documentações obrigatórias, se estão envolvendo clientes e usuários nos processos e se estão atualizando continuamente o mapa de riscos dos projetos. Enfim, os auditores da qualidade são os grandes “guardiões do processo”.

Esses profissionais devem estar muito atentos às chamadas “quebras de processos”, muito comuns em projetos de desenvolvimento de software. As quebras são muito frequentes em organizações que não possuem etapas bem definidas e ainda estão dando os primeiros passos na criação de um processo corporativo de desenvolvimento de software.

O comportamento de “desrespeitar o processo” é sempre justificado pelos profissionais que estão atuando em projetos de software com a argumentação de que estes são diferentes dos demais e determinados procedimentos, documentos e controles são desnecessários. É verdade que as atuais metodologias pregam que os processos de software devem adequar-se a determinadas categorias de sistemas, exigindo uma flexibilidade dos processos em atender níveis de exigências diferentes em cada situação. Apesar de essa afirmação ser correta, devemos ter cuidado com essa linha de argumentação, pois cada equipe tenderá a definir o que é importante e fundamental em um projeto de software, estabelecendo quais documentos e procedimentos devem ser realizados, criando uma verdadeira confusão metodológica. Somente um grupo que represente o modelo corporativo de desenvolvimento poderá estabelecer as regras do processo de engenharia de software.

Um trabalho de base corrigirá essa falta de processos corporativos. Será necessária a existência de uma equipe de profissionais, preferencialmente a equipe de processos de engenharia de software – SEPG (Software Engineering Process Group), para estabelecer o conjunto mínimo de controles e documentações que deverá ser obrigatório a todos os projetos, e quais categorias de sistemas deverão apresentar controles e procedimentos adicionais. Caso isso não aconteça, os auditores de qualidade não terão parâmetros para conduzir seus trabalhos.

## 9.3. Aplicando o Processo de Verificação

Como vimos, existem várias abordagens que podemos aplicar para a realização efetiva de um processo de verificação de documentos ou mesmo de validação de atividades executadas em determinadas etapas do ciclo de desenvolvimento. Aqui estabelecemos um conjunto de procedimentos e regras que auxiliarão as equipes de qualidade na prática e condução dessas revisões, ampliando as chances de identificação prematura de erros de levantamento e das decisões.

### 9.3.1. Planejando as Reuniões de Verificação

Uma das primeiras decisões a serem consideradas no planejamento das verificações é estabelecer o alvo dos trabalhos e definir o grupo que participará das atividades a serem realizadas. Todos os membros do grupo devem ser orientados em relação às regras e objetivos a serem alcançados com as atividades de verificação.

É recomendável que esse grupo seja heterogêneo, com profissionais de diferentes áreas, habilidades e especialidades, permitindo que as análises e discussões sejam aplicadas sobre várias perspectivas diferentes, garantindo uma revisão do documento sob as várias dimensões do problema.

No planejamento dos trabalhos deverá ser considerado o número de profissionais que desempenharão os papéis de revisores dos documentos. O dimensionamento será em função da complexidade, importância e impacto que esse documento poderá trazer a determinadas áreas da empresa. Poucos revisores deixam o processo pouco eficiente, pois teremos pouca diversidade de opiniões e, consequentemente, poucos elementos que subsidiarão a equipe para decidir se determinado documento está adequado ou não. Em contrapartida, muitos revisores poderão deixar as reuniões longas e pouco produtivas, reduzindo a eficiência das atividades de revisões. Muitos profissionais geram um excesso de divergência de opiniões que resultam em muitas discussões e poucas conclusões, o que deve ser evitado. Um número adequado de revisores gira em torno de quatro a sete profissionais.

### 9.3.2. Preparando os Profissionais

Feito o planejamento adequado das reuniões, é necessário preparar os participantes para que recebam o máximo de informações possíveis sobre o tema a ser discutido na reunião. Cabe aos profissionais que estão organizando as reuniões estruturar uma fonte de informações que possibilite agregar conhecimento a todos que estarão participando do processo.

O acesso à documentação que será alvo das revisões também é estratégico para o sucesso dessas atividades. Antes de executarmos as revisões, devemos distribuir os documentos a todos os participantes, dando oportunidade a todos de lerem os materiais e assimilar todos os tópicos a serem discutidos.

Durante esse período de distribuição, os revisores devem estudar os documentos e realizar diversos questionamentos referentes à falta de entendimento, ausência de exemplos ou comentários, à falta de estudos comprobatórios, entre outros pontos. Uma semana é um prazo adequado para um conveniente estudo das documentações, sendo possível estender por algumas semanas, dependendo da carga de serviços e do volume do material.

### 9.3.3. Executando a Verificação de Documentos

Durante as revisões, o profissional que está conduzindo as reuniões deverá garantir que todos os pontos dos documentos foram questionados e avaliados pelos revisores. Se a reunião não for orientada pela estrutura de tópicos do documento, corre-se um alto risco de dispersão dos assuntos, dificultando o controle de cobertura final do documento. Seguir a estrutura do material a ser revisado dá ao grupo uma possibilidade concreta de avaliar se a ordem dos assuntos está adequadamente montada e se existe a necessidade de anexar fontes complementares de informações para fundamentar algumas decisões.

A condução de um processo de verificação segue uma sequência lógica simples. As principais atividades a serem executadas estão listadas abaixo:

- Um tópico é definido e será escopo das discussões.
- Uma questão é levantada por um revisor.
- A questão é discutida e avaliada.
- Os revisores confirmam a existência do defeito.
- O defeito é registrado e detalhado para que seja corrigido pelos autores.
- Outras questões são levantadas até que todas tenham sido analisadas.
- Um novo tópico é identificado até que todos tenham sido discutidos.

Os trabalhos de revisão têm como objetivos a identificação de problemas. Todos os documentos deverão ser analisados com um olhar crítico, explorando e questionando todos os pontos do trabalho. Quando determinada questão é levantada, os revisores devem analisar os motivos do não-entendimento.

Revisões são, muitas vezes, encaradas como críticas aos autores, o que torna essa tarefa mais difícil, porém, devemos entender que nosso propósito está em fazer melhor nosso trabalho, e as revisões estão simplesmente aperfeiçoando o documento. Todos nós temos a ganhar com esse processo, até mesmo o autor, que poderá contar com o apoio de outros profissionais, dividindo a responsabilidade pelo trabalho.

## 9.4. Aplicando Checklist na Verificação

Checklist é um poderoso instrumento a ser aplicado nas revisões de documentos e auditorias de processos de trabalho, pois possibilita direcionar todas as atividades dos testes de verificação, criando uma abordagem única de como avaliar a qualidade de um documento. Esse direcionamento é realizado através de “guias” que orientam as auditorias e inspeções de documentos, reduzindo o grau de subjetividade em relação ao que deve ser avaliado ou não.

A checklist deve ser utilizada como um acessório durante as fases de verificação, pois orienta o profissional a investigar diversos aspectos em relação ao documento ou atividade. Apesar de considerada essencial, devemos ver a checklist apenas como um “guia” que disciplina a atividade.

<div align='center'>
    <img src='books/alexandre_bartie/imgs/figura-9-3.png'>
</duv>

A prática de checklist é muito empregada nas organizações, porém, muitas recomendações obrigatórias são desconsideradas, prejudicando a qualidade de documentos e produtos que estão sendo gerados. O profissional de qualidade poderá empregar essas checklists e avaliar sua aderência com o que está sendo praticado.