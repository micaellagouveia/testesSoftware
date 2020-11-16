# Capítulo 5 - Qualidade de Software Incremental 

O desenvolvimento de software deve empregar mecanismos para garantir que os esforços sejam devidamente direcionados a um objetivo comum. Torna-se necessário evidenciar as fases de desenvolvimento para que possamos estabelecer pontos de controle e tornar gerenciável o processo de desenvolvimento, portanto, um ciclo de desenvolvimento é uma representação de como o processo obtém organização e controle nas atividades de construção de software.

## 5.1. Ciclo de desenvolvimento em Cascata

No modelo de desenvolvimento mais tradicional, os processos são estruturados segundo um conjunto de etapas bem definidas que são completadas sequencialmente, sendo que uma etapa alimentará as próximas com decisões, documentos e informações sobre o produto a ser desenvolvido.

Essa abordagem é chamada de processo em cascata (waterfall), pois encadeia sequencialmente as etapas formando degraus de execução. Essa abordagem foi largamente aplicada nas indústrias de software, por sua facilidade de gerenciamento e entendimento por todos os profissionais. Também possibilita manter especialista em cada fase do processo, facilitando o particionamento do trabalho.

<div align='center'>
    <img src='books/alexandre_bartie/imgs/figura-5-1.png'>
</div>

Invariavelmente, essa abordagem resulta em um grande problema quando a etapa de implementação encerra-se e inicianmos a etapa de testes de software. Nesse momento, todas as inconsistências de levantamentos de requisitos, deficiências de análise e modelagem do projeto, e erros na implementação do software estão perigosamente concentrados. Essa concetração de problemas tornará o processo de correção extremamente complexo e de alto risco. Mudanças maciças de documentos e, muitas vezes, aplicar uma reestruturação em todo o projeto. O fracasso dos projetos começa a acontecer nesse ponto, no qual entramos na fase de ingerência do processo.

A ingerência caracteriza-se pela perda de controle das três variáveis mais importantes de um processo de desenvolvimento: **custos**, **recursos** e **prazos**. Os custos começam a crescer, uma vez que nada de novo é desenvolvido e todos os esforços concentram-se em fazer funcionar o que teoricamente já deveria estar funcionando. Os profissionais têm dificuldades de se posicionar em relação a suas atividades e em que situação elas se encontram, impossibilitando qualquer planejamento das atividades, conduzindo os profissionais na simples tarefa de “ir fazendo até fechar todos os buracos”. Os prazos são ampliados em função do número acentuado de retrabalhos realizados. Sucessivas prorrogações são realizadas pela falta de entendimento sobre o quanto o produto está estável. Enfim, a ingerência é o puro “cao organizacional”.

Muitos projetos fracassaram principalmente porque empregaram esse tipo de abordagem que conduz o projeto a centrar suas ações na “realização das tarefas”, sem que nenhum produto “parcial” seja produzido. Isto faz com que clientes, gerentes e profissionais de desenvolvimento não tenham uma referência “concreta” sobre os resultados a serem alcançados, tornando o processo agradável inicialmente e estafante no final.

Devemos entender que a maioria dos profissionais tem dificuldades em lidar com coisas abstratas e as documentações não serão suficientes para saciar tal necessidade. Corremos um grande risco quando não é disponibilizado um produto “parcial” para que ocorra uma avaliação concreta dos resultados alcançados.

<div align='center'>
    <img src='books/alexandre_bartie/imgs/tabela-5-1.png'>
</div>

Sob a perspectiva de gerenciamento do projeto, essa abordagem atende perfeitamente, pois estrutura adequadamente as atividades de forma lógica e gradativa, possibilitando uma sensata operacionalização dos procedimentos de trabalho, porém, sob a perspectiva técnica do projeto, ela não proporciona um mecanismo de aprendizado gradativo nem possibilita mecanismos de correção de rumos durante o processo de desenvolvimento.

## 5.2. Ciclo de Desenvolvimento Iterativo

Necessitamos ter um processo com um encadeamento de atividades similar ao processo em cascata, porém com ciclos curtos de desenvolvimento, de forma a possibilitar reavaliações constantes do projeto e um mecanismo ideal para assimilar conhecimentos de forma gradativa.

Sob o ponto de vista de projeto, o ciclo de desenvolvimento de software passa a ser visto como uma sucessão de iterações, na qual o software ganha sucessivos incrementos de funcionalidades até que atenda à totalidade dos requisitos esperados. Cada iteração deve fornecer unm produto “executável”, devidamente testado e pronto a ser utilizado, resultando em um subconjunto de uma visão completa do sistema. Deve ser operacional, sob a perspectiva das necessidades do cliente, e completo, sob a perspectiva da engenharia do produto construído.

<div align='center'>
    <img src='books/alexandre_bartie/imgs/figura-5-2.png'>
</div>

### 5.2.1. Definindo uma Iteração

Uma iteração direciona todo um esforço de desenvolvimento em direção a uma _release_ específica - um produto estável, que possui um controle de versão e acompanha todos os outros elementos necessários a sua utilização, como modificações do banco de dados, migrações de informações, rotinas de instalação, documentos, entre outros.

Uma iteração é um ciclo de desenvolvimento completo aplicado a uma pequena fração do produto de software. Uma iteração percorre todos os processos envolvidos no decorrer do desenvolvimento, como o gerenciamento de requerimentos, análise e modelagem, implementação e testes de software. Trata-se de um pequeno projeto em cascata inserido dentro de um projeto maior.

### 5.2.2. Definindo uma “_Release_”

Uma _Release_ pode ser interna ou externa. Uma release interna é usado somente pela equipe interna de desenvolvimento como resultado de um ponto de controle ou para uma demonstração a clientes e usuários. Uma release externa é uma versão do produto distribuída para os usuários finais. Uma release não é necessariamente um produto completo, ele pode conter apenas uma fração das funcionalidades que, teoricamente, deveria contemplar. O release deve ser produzido em intervalos regulares para “forçar” a equipe de desenvolvimento produzir “resultados” concretos. Essas versões parciais são estratégicas para o sucesso do desenvolvimento do software, pois permitirão aos usuários e clientes experimentarem uma pequena amostra do que virá a ser o software completo, possibilitando feedback antecipado de eventuais não-conformidades ou desconfortos gerados pelo produto.

À medida que são realizadas as iterações, serão inseridas novas funcionalidades e características ao produto, de forma que o software “cresça” na medida de seu desenvolvimento (incrementos sucessivos). A grande diferença dessa abordagem é o planejamento cuidadoso de cada iteração, para que passamos gerar um release funcional pronto a ser distribuído para nossos clientes e usuários.

## 5.3. Ciclo de Teste Iterativo

Um processo de desenvolvimento possui muitas iterações. Durante uma única iteração, vários componentes serão produzidos e alterados, gerando uma nova versão do componente que deve ser adequadamente testado. Em vada nova iteração, esse componente sofrerá um novo refinamento, exigindo uma nova bateria de testes. Em cada refinamento, novos cenários de teste vão sendo incorporados e armazenados para que sejam futuramente aplicados em futuros estágios do desenvolvimento.

Esses refinamentos implicam contínuos ajustes no planejamento, modelagem, execução dos testes, o que significa que haverá sempre certo nível de retrabalho toda vez que um componente sofrer uma mudança. Enquanto os requisitos não se estabilizarem, não haverá possibilidade de estabilizar os testes.

<div align='center'>
    <img src='books/alexandre_bartie/imgs/figura-5-3.png'>
</div>

A abordagem iterativa dá um grande foco para os testes de regressão. Empregando o exemplo acima é possível verificar como os testes podem ser reaproveitados em cada novo refinamento executado. Na primeira iteração, apenas uma fração da solução está disponível, sendo necessário um pequeno esforço de teste para validar suas funcionalidades. Na segunda iteração, o software ganha novas funcionalidades e parte dos testes é reaproveitada da primeira iteração. Na terceira iteração o mesmo fato se repete, novas funcionalidades são adicionadas e a maioria dos testes executados na iteração anterior é reaproveitada, seguindo esse ciclo sucessivamente até que os requisitos se estabilizem e a solução receba a última bateria de testes.

O fato de a maior parte dos testes se repetir muitas vezes já compensa o esforço de automatização dos testes. A falta de automação dos testes vai se tornando mais crítica à medida que avançamos no desenvolvimento do software e muitas funcionalidades precisam ser testadas. O risco de que as novas alterações tenham comprometido as funcionalidades anteriores tende a aumentar ainda mais à medida que o software vai se tornando mais complexo. Definitivamente, a automação de teste é algo crítico para obtermos um processo que garanta a qualidade do software desenvolvido.

## 5.4. Ciclo de Qualidade Iterativa

O processo de qualidade do software deve garantir todo o ciclo de desenvolvimento de sistemas. O planejamento da qualidade deve começar junto com o planejamento do software, ou seja, desde o início do projeto. A modelagem e a execução das atividades ligadas à garantia da qualidade do software são tão árduas e complexas quanto as atividades de construção de softwares.

Se esse esforço de qualidade não acontecer de maneira efetiva, um longo ciclo de desenvolvimento será necessário, e uma fase inteira de “correções de defeitos” será inserida no cronograma do projeto, dilatando os prazos de entrega do produto. As atividades de desenvolvimiento serão cada vez mais substituídas por atividades de manutenção de erros, reduzindo a produtividade da equipe de desenvolvimento.

Somente com a simples aplicação dos testes de verificação nos documentos gerados em cada iteração planejada no ciclo de desenvolvimento, podemos identificar uma série de inconsistência nas documentações do produto, possibilitando suas correções antes mesmo de executar os testes. Quanto mais cedo um defeito é descoberto, menor será o impacto no planejamento do projeto. 

Cada nova iteração do projeto de desenvolvimento possui seu ciclo independente de qualidade, de forma a garantir os objetivos de cada ciclo de desenvolvimento. As atividades de qualidade deverão considerar a evolução incremental da aplicação, sendo necessário reavaliar constantemente a qualidade dos documentos que necessitam ser adequados em relação às mudanças e inovações inseridas em cada ciclo evolutivo.

Necessitamos avaliar se as novas funcionalidades (geradas através de melhorias ou correções do modelo de negócio) estão sendo adequadamente assimiladas em cada ciclo evolutivo do projeto. É preciso avaliar o impacto e a consistência dos documentos em relação às mudanças inseridas em cada ciclo, de forma que os novos requisitos não invalidem os requisitos existentes nos ciclos anteriores.

<div align='center'>
    <img src='books/alexandre_bartie/imgs/figura-5-4.png'>
</div>

## 5.5. Critérios de Finalização

Um dos aspectos mais importantes a serem estabelecidos durante os procedimentos de qualidade é estabelecer os critérios de finalização dessas atividades, ou seja, determinar quais serão os indicadores que determinarão se determinado documento, atividade ou software alcançou o nível de qualidade desejado.

Os critérios de finalização servirão como uma referência aos grupos de qualidade para aplicarem os procedimentos e somente darem por encerrada uma atividade quando esses critérios forem plenamente satisfeitos. É muito importante estabelecer que, em todas as atividades de qualidade, existirá, ao menos, um critério de finalização definido.

Para termos uma idéia de como devemos empregar os critérios de finalização, daremos alguns exemplos de aplicação prática desse instrumento:

<div align='center'>
    <img src='books/alexandre_bartie/imgs/tabela-5-2.png'>
</div>

<div align='center'>
    <img src='books/alexandre_bartie/imgs/tabela-5-3.png'>
</div>

<div align='center'>
    <img src='books/alexandre_bartie/imgs/tabela-5-4-1.png'>
</div>

<div align='center'>
    <img src='books/alexandre_bartie/imgs/tabela-5-4-2.png'>
</div>
