# Capítulo 6 - Por que os Processos de Qualidade de Software Fracassam

Muitas tentativas de implantação de processos de qualidade de software fracassam. Isso ocorre porque muitos processos foram distorcidos e inadequadamente executados, o que gerou grandes frustações, além de significativos prejuízos financeiros.

## 6.1. Ausência de Gerência de Qualidade Independente

Quando estruturamos uma área de qualidade de software, disponibilizamos uma infra-estrutura que contempla recursos físicos (máquinas, ferramentas), recursos humanos (especialistas em planejamento e execução dos testes) e experiências acumuladas (metodologias, técnicas, conhecimento adquiridos). Quanto melhor for o gerenciamento dessa infra-estrutura, maior serão os resultados a serem adquiridos em função do investimento realizado.

Apesar de todo o investimento realizado na estruturação de ambiente de testes, aquisição de ferramentas e contratação de profissionais, muitas organizações não criam uma área de qualidade de software, deixando o gerenciamento para outra área já existente. A falta de gerenciamento direto sob essa estrutura disponibilizada minimizará os benefícios que poderão ser conseguidos com um processo de qualidade de software.

## 6.2. Ausência de Procedimentos de Testes Automatizados

Apesar de sabermos que um processo 100% automatizado é difícil de se alcançar, devemos investir o máximo que pudermos na automação dos processos de testes. Isso porque a utilização de procedimentos manuais durante o processo de teste não é recomendada, já que se trata de um modelo extenuante e “não confiável“.

Extenuante pelo fato de que todas as vezes que determinada funcionalidade é inserida ou modificada, todas as outras funcionalidades devem ser novamente testadas, o que exige grande esforço de repetição, tornando esta atividade inviável. Para viabilizar os procedimentos manuais, é necessário reduzir o volume de cenários a serem testados, reduzindo o nível de cobertura dos testes e, consequêntemente, aumentando a probabilidade de novos errros não serem identificados. Isso reflete nos custos e na confiabilidade do processo.

Não confiável porque faltam garantias reais sobre como o profissional de testes está operacionalizando tais atividades, não sendo possível garantir que este seguiu criteriosamente as recomendações estabelecidas no planejamento, empregando todos os cenários existentes, executando a sequência correta dos procedimentos de testes, entrando com as informações adequadas às condições que estão sendo testadas e, finalmente, conferindo se ocorreu o comportamento esperado. As interferências humanas no processo tornam o modelo muito frágil, o que pode desacreditar todo o esforço que está sendo realizado.

## 6.3. Qualidade é Sempre Aplicada Tardiamente no Desenvolvimento

A maioria das organizações que “amadureceram” seus processos de desenvolvimento ainda insistem em acreditar que os testes devem ocorrer somente após a produção do software ou quando este estiver parcialmente pronto. Isso equivale a dizer que somente obteremos qualidade na fase posterior ao desenvolvimento; porém, conforme argumentado nos tópicos anteriores, o maior volume de erros concentra-se nas fases iniciais de levantamento e modelagem do software. Mesmo que somente apliquemos testes nas fases finais do projeto, não significa que será dessa forma pelo resto de nossas vidas.

Portanto, inserir os profissionais ligados ao processo de qualidade de software na equipe de desenvolvimento somente reforça o conceito de qualidade como uma única etapa dentro do processo de criação de um software. Devemos ampliar os conceitos de qualidade e aplicar testes em todos os pontos do processo, tornando o processo de engenharia de software mais controlado e confiável, possibilitando o efetivo gerenciamento do projeto de desenvolvimento.

## 6.4. Ausência de Profissionais Capacitados em Qualidade de Software

É muito comum observarmos organizações utilizarem seus profissionais de desenvolvimento para estruturar e organizar processos de qualidade de software. Essa falta de especialização afetará a eficiência do processo de garantia da qualidade de software, podendo comprometer todo o esforço de implantação desses processos na organização.

Muitas vezes, acreditamos que, pelo simples fato de o profissional ter experiência em desenvolvimento, este já está capacitado a desempenhar o papel de “analista de testes”, porém, é necessário lembrar que esse profissional tem um paradigma bem diferente do profissional de desenvolvimento. Enquanto um deve planejar a construção de um software, o outro deve avaliar sua solidez.

Profissionais ligados às atividades de qualidade de software (revisores, auditores, analistas de testes e automatizadores) devem possuir a metodologia totalmente desenhada para atender seu maior objetivo – encontrar falhas em todo o ciclo de desenvolvimento do projeto de software. Para isso, esses profissionais devem direcionar seus esforços em aperfeiçoar essa metodologia, padronizar as documentações e procedimentos de qualidade e reduzir os esforços no planejamento e na operacionalização dessas atividades.

O foco da área de desenvolvimento é produzir o software e nunca garantir a qualidade de software. Cabe a essa área compreender todas as exigências da área de negócios, as disponibilidades e restrições tecnológicas existentes e as demais características operacionais para que o produto tecnológico adapte-se o mais perfeitamente possível aos processos que irá suportar. Deve estar preocupado com uma documentação adequada para garantir que o conhecimento do projeto não permaneça apenas na cabeça de alguns profissionais. Deve atentar à qualidade da solução encontrada, de forma a garantir um projeto mais flexível e pronto para crescer e suportar mudanças. Deve oferecer uma interface amigável, de forma a proporcionar ao usuário facilidade de uso e agilidade operacional. Deve acompanhar as evoluções tecnológicas para manter seu produto sempre “novo” conceitualmente e tecnologicamente, oferecendo cada vez mais recursos e facilidades ao usuário final. Parece que os desenvolvedores – analista de sistemas, administradores de dados, designers e programadores – estão com sua agenda lotada e, portanto, não possuem tempo para garantir que tudo isso esteja funcionando.

## 6.5. Falta de um Modelo Corporativo de Qualidade

Esse sintoma está intimamente ligado à ausência direta de uma gerência de qualidade de software. Sem esse gerenciamento, é comum que cada “projeto de software” encontre sua forma mais particular e “eficiente” de estruturar um processo de garantia da qualidade de software. A falta de um modelo corporativo que discipline esse processo fragiliza qualquer esforço de implantação.

O processo de qualidade deve ser um modelo único que gerencie as diversas atividades que ocorrem nos vários ambientes existentes, de forma a garantir rigorosos processos de qualidade em todas as etapas do desenvolvimento do software. Esse modelo deve contemplar uma gradual assimilação desses conceitos por parte da organização, sob o risco de não se tornar operacional; portanto, o planejamento corporativo e o treinamento dos profissionais para enraizar e melhor absorver os conceitos que serão exigidos durante o processo de implantação são chaves, para o sucesso desse processo.

## 6.6. Foco em Testes Progressivos Aumentam Riscos

Em muitas organizações, as empresas direcionam seus esforços nos chamados testes progressivos. Os testes progressivos somente focalizam as novas implementações realizadas no software, desconsiderando as funcionalidades anteriores.

Essa abordagem é extremamente tentadora, pois reduz drasticamente o esforço de implementação de um ambiente de testes. Em contrapartida, não garante que as antigas funcionalidades continuem comportando-se adequadamente, existindo alta probabilidade de as novas versões inserirem novos defeitos e de estes não serem identificados pelos testes de software, aumentando a incidência de erros no ambiente de produção.

## 6.7. Deficiência no Planejamento dos Testes

O planejamento é um exercício mental que produz uma visão sobre como resolver um conjunto de situações, antecipando os passos de realização de um trabalho. Estudamos o problema, analisamos as soluções, operacionalizamos uma sequência de atividades e prevemos eventuais riscos e insucessos. Dessa forma, estaremos nos preparando para o projeto a ser realizado.

Se pensarmos no curto prazo, o planejamento exigirá maior esforço de trabalho. Maior esforço sempre é sinônimo de maiores custos, maior volume de horas trabalhadas maior número de profissionais envolvidos. No entanto, analisando o ciclo de vida do software e sua expectativa de se manter ativo por um período de cinco anos, temos que planejar as atividades de forma a reduzir os custos de manter esse ambiente de testes operacional por todo esse período. Se negligenciarmos o planejamento, além de aumentar as chances de insucesso na detecção de erros, os custos finais provocados pela ineficiência e inflexibilidade do modelo serão muito mais altos.

É por isso que um bom planejamento deve ter como objetivo uma visão de longo prazo, para que esse investimento realizado seja pago no decorrer dos meses. O planejamento de testes deve valorizar aspectos como reaproveitamento de cenários de testes já realizados, mecanismos de reexecução de testes e conferência de resultados, redução do impacto das mudanças nas documentações/procedimentos de testes já implementados e redução de esforço na manutenção das diversas versões de testes, para cada versão de software existente.

## 6.8. Sob Pressão, os Testes São Sacrificados

Em todos os projetos de desenvolvimento de software é comum encontrarmos uma fase dedicada à atividade de teste de software. No cronograma do projeto, a etapa de testes é descrita como uma fase posterior à codificação do software, já considerado, nesse momento, um produto acabado.

<div align='center'>
    <img src='books/alexandre_bartie/imgs/figura-6-1.png'>
</div>

Por diversas razões, os prazos de entrega de um software são sempre maiores do que o planejado e os custos do projeto extrapolam o orçamento inicial. Com isso, é comum a área de desenvolvimento buscar atalhos, com a finalidade de compensar os atrasos e obter um produto tecnológico o mais rapidamente possível. Os atalhos serão obtidos da redução de tempo dedicado às fases que mais consomem recursos do projeto. Esse tempo ganho será direcionado à etapa de codificação do produto final.

<div align='center'>
    <img src='books/alexandre_bartie/imgs/figura-6-2.png'>
</div>

As primeiras etapas sacrificadas são as de modelagem e estruturação da solução. São fases que, mal feitas, trarão consequências diretas na flexibilidade e manutenção da aplicação. Sem essas fases, o desenvolvimento passa a codificar uma solução “pouco pensada”, sem considerar os diversos aspectos de negócio a longo prazo.

Com o atraso já entrando na casa dos meses, é comum a área de desenvolvimento sacrificar também a etapa dos testes. A fase não é totalmente eliminada, porém perde eficiência em sua principal missão – detecção dos erros. A redução de tempo ocorre eliminando a fase de planejamento de testes, que consome mais da metade do tempo desse processo. Dessa forma, perde-se muito na qualidade dos testes finais, deixando processo de testes caótico e falho.

## 6.9. Ausência de um Ambiente de Testes Isolado

O processo de validação de um software exige um ambiente exclusivo de testes, isolado de qualquer interferência dos demais ambientes de desenvolvimento e produção. A interferência entre ambientes pode comprometer a qualidade dos testes, bem como a confiabilidade das informações e processos executados. Esse isolamento garante que nenhuma atividade externa prejudicará a execução dos procedimentos de testes, aumentando o nível de eficiência dos trabalhos. Nesse ambiente, encontramos equipamentos dedicados, ferramentas de testes já instaladas e sistemas parcialmente instalados com seus respectivos softwares de apoio.

A gestão isolada do ambiente proporciona à área de testes uma autonomia de como e em que momento devemos executar os testes de determinada aplicação. Com isso, em eventuais modificações emergenciais de uma aplicação, poderemos submeter o software a rigorosos procedimentos de testes sem que exista risco de manipulação ou interferência de atividades externas, portanto, mesmo que determinados testes sejam executados no ambiente de desenvolvimento (planejados e executados pelos próprios desenvolvedores), outras categorias de testes (com objetivos diferentes) deverão ser processadas no ambiente de testes, com total isolamento entre ambos.

## 6.10. Transferir o Planejamento ao Analista de Sistemas

Quando o planejamento é feito pelo analista de sistemas e não pelo analista de testes, uma enorme possibilidade de problemas surge. Temos que ter em mente que o profissional de testes não é o analista de sistemas, mas sim o analista de testes. Somente ele tem a percepção e experiência das diversas categorias de testes existentes, sabe como organizá-los e como empregá-los, propiciando mais eficiência na detecção de erros – que é nosso principal objetivo.

O analista de sistemas tem uma tendência natural de produzir testes válidos, ou seja, aqueles já suportados pela aplicação. Ele sabe o que o sistema está consistindo e o que não está. Ele já decidiu o que vale a pena tratar dentro da aplicação. Dessa forma, ele não tentará submeter o software a condições que ele tem consciência de que o aplicativo não terá êxito. Com isso, obteremos um conjunto de testes “viciados”, já que se baseiam em condições já discutidas no desenvolvimento. Já o analista de testes atua com total imparcialidade no planejamento e na criação dos cenários para aplicar na validação do software. Sua missão é criar variações de comportamento no software, nas quais apontem situações não previstas pela equipe. Cabe a esse profissional ir além da percepção do analista de sistemas e planejar testes sob a mais variadas condições existentes no negócio.

## 6.11. Dificultar o Acesso do Analista de Testes ao Software

Quando o analista de testes não possui acesso ao software a ser testado, a qualidade da compreensão do sistema fica comprometida. O software não é apenas o objeto de teste, mas também uma importante fonte de informações. Usando a aplicação, é possível identificar regras de negócio muitas vezes esquecidas nas documentações e pelos analistas de sistemas. É comum descobrirmos regras de negócio, exercitando ações dos usuários – descobrir que somente é possível rentabilizar uma carteira de investimentos após o encerramento das transações comerciais; descobrir que os campos obrigatórios mudam em função do tipo de negociação utilizada; descobrir que somente após a abertura do caixa é possível realizar as transações financeiras.

O software, além de ampliar a compreensão do negócio, auxilia no processo de refinamento e validação do planejamento dos testes. À medida que o analista de testes estabelece determinados cenários e condições para execução, é possível verificar se essas informações têm a qualidade necessária a ser empregada durante a realização dos testes.
