# Capítulo 8 - Entendendo os Testes de Verificação

Quando uma organização não possui um processo formal de testes de verificação, muitas fases de um projeto são encerradas sem que determinados pontos tenham sido totalmente “estressados” ou mesmo levantados. São buracos que ganharão dimensões enormes à medida que o projeto avança em suas novas fases. Somente quando parte do produto estiver disponível é que esses “pontos não analisados” serão novamente pauta de discussões, provocando reestruturações no projeto e inevitáveis retrabalhos.

Portanto, é missão dos testes de verificação avaliar se toda a documentação gerada e todas as atividades que estão sendo desempenhadas são conduzidas adequadamente, gerando um modelo de software aderente às necessidades dos clientes, pautadas em definições claras, com regras e objetivos compreendidos por todos os grupos que estão participando do ciclo de desenvolvimento. Esses testes avaliam a qualidade de todo o processo que está suportando o projeto de software, validando se todas as documentações e atividades geradas estão dentro de um padrão desejável, reduzindo os riscos de falhas de interpretação que seriam inseridas no produto de software no momento de sua construção.

## 8.1. Estruturando um Processo Sistemático de Verificações

Na maioria das organizações de software, existem aplicações práticas dos conceitos que envolvem os chamados testes de verificação, que focalizam as documentações e atividades executadas durante as etapas do ciclo de desenvolvimento; porém, o que observamos é que essas organizações minimizam a importância desse tipo de atividade, aplicando os conceitos apenas em alguns poucos documentos produzidos durante o ciclo de desenvolvimento.

Além de um escopo reduzido, essas atividades são realizadas sem qualquer planejamento e formalização, sendo opcional a presença de pessoas-chave para avaliar os levantamentos e decisões registradas nas documentações. Os testes de verificação devem ser sistematizados, planejados e devidamente aplicados, de forma a se tornarem parte integrante do processo de engenharia de software, e conduzidos por uma equipe independente da área de desenvolvimento (preferencialmente pela área de Garantia da Qualidade do Software), de forma a garantir maior eficiência e nível adequado de profundidade nesses trabalhos. Se esse processo estiver nas mãos de profissionais de desenvolvimento, será pouco eficiente na detecção de defeitos, sendo as reuniões simplesmente informativas. Uma área independente conduzirá esse processo com total autonomia, sendo mediador entre o cliente (aquele que necessita das informações documentadas com um alto nível de qualidade) e o fornecedor (aquele que gerou a documentação e tem outras mil coisas pendentes para fazer).

Muitas pesquisas afirmam que o simples hábito de realizar revisões já garante um alto nível de detecção de defeitos, porém, é fato que esse número pode ser muito mais expressivo se estabelecermos a sistematização e o planejamento desses trabalhos. Assim, a verificação feita de forma estruturada, com objetivos bem definidos, período estipulado e a participação de pessoas com visões diferentes do problema tende a ser mais efetiva do que um simples processo de revisão casual.

## 8.2. Aumentando a Eficiência das Verificações

Inspeções e revisões técnicas são termos comuns e bem familiares à maioria das pessoas. Isso porque não é incomum encontramos organizações que aplicam essas técnicas dentro de seu processo de desenvolvimento de software. Dessa forma, a primeira impressão é acreditarmos que esses métodos não são muito eficientes nem adequados para detecção de problemas, uma vez que essas mesmas organizações são grandes fábricas de erros. Então, onde está o problema com esses procedimentos de inspeção que deixam passar tantos furos nas definições e soluções encontradas?

O problema está em como tais atividades estão sendo realizadas. Não devemos somente realizar a tarefa, mas fazê-la da forma mais adequada possível. As verificações devem obedecer a regras para que todos os objetivos das reuniões sejam alcançados, todos os profissionais tenham a oportunidade de participar e que todos os pontos a serem discutidos tenham sido adequadamente esgotados pelos revisores. Essas regras permitirão maior eficiência dos trabalhos de verificação, pois disciplinam tais atividades. Somente dessa forma, as atividades de verificação passarão a ser um instrumento fundamental na detecção de erros do processo de desenvolvimento de software.

### 8.2.1. Profundidade das Análises e Discussões

Quando as organizações aplicam inspeções e revisões técnicas estão, na maioria das vezes, em busca de erros de padronização, ou seja, verificando se os documentos e atividades estão sendo feitos dentro de um modelo estabelecido. Apesar de isso ser importante, faz com que o revisor permaneça na superfície do problema. O revisor não somente tem que examinar se os documentos foram gerados na cor, tamanho e nomenclaturas desejados, mas se estes estão coerentes, possuem nomes e definições claras, se suas estruturas estão bem definidas e flexíveis, e até avaliar se não existia um jeito mais simples e fácil de alcançar o mesmo produto final. Dessa forma, uma peça burocrática do processo torna-se um elemento que agrega mais valor ao produto final.

### 8.2.2. Uniformidade das Atividades

Outro fator importante é como individualmente cada revisor está conduzindo seus trabalhos. Caso não existam regras claras do que deve ser ou não analisado, cada revisor encontrará um jeito próprio de abordar o problema e focalizar no que este acredita ser fundamental. Estruturar os trabalhos do revisor e treiná-los adequadamente são tarefas fundamentais ao sucesso dessas atividades.

A utilização de checklists auxilia na uniformização e padronização do que será avaliado e dos padrões esperados em cada documentação. Esse instrumento orienta os trabalhos dos revisores e possibilita uma forma única de abordar os documentos e atividades a serem auditadas.

### 8.2.3. Continuidade e Freqüência

É comum que as atividades de verificação somente ocorram nos estágios iniciais do projeto, pois são as fases em que é gerado o maior número de documentos e registros de informações. No entanto, é natural que o projeto sofra a inserção de melhorias ou mesmo uma reestruturação de aspectos fundamentais do negócio, de modo a interferir nas estruturas e definições estabelecidas. Isso significa que os projetos estão sendo modificados sem que ocorra uma nova onda de revisões com o objetivo de avaliar se o que está sendo proposto está coerente e que todos os impactos da mudança estejam bem claros a todas as áreas envolvidas. As atividades de verificação devem ser executadas sempre que o projeto sofrer mudanças, de forma a manter a integridade das documentações e, conseqüentemente, garantir que todas as decisões tomadas sejam devidamente analisadas e compartilhadas pelas áreas interessadas.

### 8.2.4. Revisores Experientes

Os revisores devem ser profissionais experientes que possuam afinidade com os documentos e materiais que estão sendo colocados em discussão. Se a verificação for aplicada a documentos que retratam o domínio do problema, os revisores devem conhecer a fundo as características do negócio para poder confrontar o documento com as definições nele estabelecidas. Se o documento retratar a arquitetura da aplicação, os revisores devem conhecer profundamente as tecnologias envolvidas e os impactos gerados pela escolha de determinada configuração de softwares e hardwares.

As reuniões de verificações de documentos podem ser uma excelente escola para profissionais que necessitam assimilar um conhecimento específico sobre um determinado assunto do projeto de software, porém, devemos ter claro que profissionais inexperientes contribuem muito pouco para as atividades de verificação. Devemos considerar que o maior objetivo das revisões é possibilitar a identificação de erros e que o processo de capacitação e aprendizado deve ser visto como um ganho secundário.

### 8.2.5. Presença de um Moderador nas Reuniões

Se estamos dispondo de tempo e recursos para revisar as documentações geradas durante o processo de desenvolvimento, devemos garantir que esse esforço está sendo adequadamente utilizado. A presença de um moderador torna as reuniões mais produtivas, uma vez que sua principal missão é manter o processo dentro do foco e dos propósitos da reunião.

O moderador não deveria ter a responsabilidade de revisar os documentos, sob pena de prejudicar seu desempenho como condutor das reuniões. Sua atribuição é garantir que todos os pontos estão recebendo a devida atenção por todos os participantes e propiciar aos revisores iguais oportunidades de expor seus pensamentos e comentários. Bons moderadores ampliam as chances de sucesso das revisões, pois aumentam as incidências de detecção de problemas.

### 8.2.6. Revisões Curtas e Bem Focadas

As revisões são mais efetivas quando são curtas e bem direcionadas. Quanto mais longas as reuniões, maior será a dispersão dos revisores, uma vez que serão introduzidos muito mais tópicos para revisar. As revisões deveriam durar por volta de duas horas e ter um conjunto de assuntos reduzidos e relacionados. Isto facilita o trabalho do grupo de revisores, auxiliando-os na condução dos trabalhos. Se um documento for muito longo, é recomendável dividir a revisão em várias sessões, com foco bem reduzido. Isso permitirá ao processo de verificação ser muito mais efetivo.

### 8.2.7. Identificar Problemas, Não Resolvê-los

Uma das razões para que as revisões falhem em sua intenção de encontrar problemas e inconsistências nos documentos é o fato de os participantes estenderam suas discussões não somente para o problema, mas para sua resolução. A resolução de um problema requer investigação, análise e reflexão detalhada, o que não é possível durante uma reunião de revisão. Quando um problema é identificado, devemos estabelecer quem irá estudá-lo e corrigi-lo. A revisão deverá estar focada em identificar os problemas, não em resolvê-los.

Se determinado problema requerer discussão mais profunda, uma nova reunião deverá ser marcada para a discussão desse ponto. Isso permitirá aos participantes terem um tempo para refletir e analisar alguns aspectos que não estavam suficientemente claros. O mais importante é fazer com que as reuniões tenham ritmo e não fiquem presas a determinados assuntos.

### 8.2.8. Concluir as Revisões

Em processos de verificação pouco formais, é comum que após a execução de revisões nenhum documento seja gerado. Quando isso ocorre, perdemos parte da história das decisões do projeto de desenvolvimento. Isso porque um documento mostra a situação final, mas não apresenta a justificativa de tais definições ou soluções terem sido apresentadas. É muito comum que decisões tomadas no passado sejam novamente contestadas no futuro, o que requer documentação que justifique determinadas decisões. O relatório de conclusão das verificações deve estabelecer os motivos da mudança de decisões e definições dos documentos, exatamente para podermos justificá-los e rastreá-los no futuro.

## 8.3. Papéis Existentes em uma Reunião de Verificação

Durante a execução das reuniões de verificações, diversos papéis deverão ser aplicados para o adequado desempenho das atividades. Cada profissional deverá ter consciência do papel que está desempenhando, quais são seus objetivos e seus limites. Deverão entender que a reunião somente terá êxito se cada profissional desempenhar adequadamente o papel o qual foi designado.

### 8.3.1. Moderador

O moderador tem por objetivo fazer cumprir a agenda estabelecida na reunião. Deve manter os revisores dentro do tópico em discussão, evitando desvios na condução dos trabalhos. O moderador deve trazer as discussões paralelas para o grupo e possibilitar a todos participar igualmente dos debates.  Preferencialmente, deve ser um profissional da área de qualidade.

### 8.3.2. Escrivão

O escrivão mantém registrados todos os pontos de discussão e documenta as ações estabelecidas pelo grupo para posterior execução. Um escrivão não poderá assumir a tarefa de revisar os documentos, sob pena de falhar nos registros enquanto está participando de discussões sobre o documento. Apesar de ser sempre colocado em segundo plano, o escrivão exerce um importante papel nas reuniões. Ele cuidará da memória da reunião, registrando os pontos discutidos, as divergências e decisões tomadas pelo grupo, que serão resgatadas no futuro, caso haja falhas detectadas nas próximas etapas do desenvolvimento.

### 8.3.3. Autor

O autor é o criador do documento a ser revisado. O autor deve explicar o documento e fornecer informações fundamentais à compreensão do conteúdo do material (caso o documento não seja auto-explicativo, isto já indica a necessidade de melhoria). Um aspecto importante é não focar as discussões no autor, mas sim no documento. Isso significa que o autor somente inicia o processo de discussão, dando uma rápida visão e explanação sobre o documento, responder questionamentos quando solicitado e esclarecer dúvidas dos revisores. Além disso, ele apenas acompanha os trabalhos de revisão.

### 8.3.4. Revisor

São os profissionais que estarão única e exclusivamente voltados para a discussão do documento e identificação de problemas. Os revisores deverão respeitar as regras da reunião e a condução dos trabalhos pelo moderador. Deverão evitar debater assuntos que não estão na agenda da reunião e se esquivar de discussões paralelas. Devem focar o entendimento e a melhoria do documento, não a discussão propriamente dita.