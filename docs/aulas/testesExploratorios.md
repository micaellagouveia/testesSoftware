# Testes Exploratórios

Abordagem de aprendizagem simultânea. Simultâneo aprendizado, design e execução de testes; isto é, os testes não são definidos previamente em um plano de teste estabelecido, mas são dinamicamente projeto, executado e modificado.

## Contextos de Uso
* Quando é necessário um feedback ou apredizagem rápida do produto
* Quando não há disponibilidade de tempo para aplicações sistemáticas de testes.
* Auxiliar na investigação de fatores de riscos específicos.
* Maior diversidade de testes
* Na realização de teste de regressão baseados em relatórios de defeitos
* Na construção de testes a partir da perspectiva do usuário, originando-se de um manual de usuário, por exemplo.

## O que podemos identificar nessa fase?
* Aléem de bugs funcionais, podem ser identificados problemas de layout, UX, regras de negócios.

| Vantagens | Desvantagens |
|-----------|--------------|
| Muito usado quando existe pouca ou nenhuma documentação | A sua eficiência depende da experiência/habilidade do testador |
| Aumentam as variações dos testes | Necessitam de certa experiência no domínio |
| Criam novos cenários para testes | Não devem ser levados como principal abordagem de teste |
| Incentiva a discussão do tima sobre os itens | - |

* Eles não são livres de documentação, e sim são feitas ao longo do desenvolvimento dos testes.
* Devem possuir uma boa orientação e objetivo.


## Metáfora do Turista

### Planejamento do teste
* Decomposição do sistema baseado na **intenção** e não em estruturas correlacionadas ao aplicativo em teste.
* Distribuição dos recursos e esforços

![turista](../assets/metaforaTurista.png)

### Distrito de Negócios
* Sistemas que dependem da inicialização e desligamento prontos pra uso.
* 7 tours

| Tour guiado | Tour Monetário | Tour ao Ponto de Referência | Tour Intelectual |
|-------------|----------------|-----------------------------|------------------|
| Seguir manual no usuário | Verificar a coerência das funcionalidades de uma versão demonstrativa do produto com as especificações do sistema. | Orientação é fudamental | Trabalho sobre pressão |
| Executar cada passo descrito, sem desviar. | Razão para visitar a cidade, motivo para comprar o software. | Procure pontos de referência e percorra esses pontos na ordem estabelecida | É diferente para cada aplicação, faça perguntas difíceis para os testes de softwares. |
| Testa a precisão do manual. | Detecta se o que é vendido para os clientes do produto real. | Avaliar a interação entre diferentes caractrísticas do produto quando executado em diferentes sequências. | Detecta defeitos de alta complexidade e até mesmo defeitos simples. |
|  | Demonstrações de venda, de uso do produto | | |


| Tour FedEx | Tour fora do horário comercial | Tour Coletor de lixo |
|------------|--------------------------------|----------------------|
| Movimentação de dados entre entrada e saída. | Momento de trabalho de manutenção, backup, armazenamento de dados. | Avaliação metódica em blocos |
| Identificar cada característica que infleuncia ou sofre influência nos dados. | Identificar falhas resultantes da execução dessas atividades. | Cobrir determinado objetivo de forma metódica, não dependendo do tempo e verificando o mais óbvio. |
| Identificar possíveis pontos que esses dados são corrompidos no processamento. |  |  |

### Distrito Histórico
* Tem como objetivo testar softwares legado.

| Tour pelo bairro ruim | Tour pelo museu | Tour da versão anterior |
|-----------------------|-----------------|-------------------------|
| Concentrar esforços de testes em áreas com mais concetrações de defeitos. | Código antigo (legado) | Uma vez que houve uma atualização, cenários das versões anteriores devem ser novamente executados. |
| À medida que o teste caminha, outras áreas podem ficar mais problemáticas. | Registros de alterações para consulta de códigos antigos, Código apresenta documentação pobre, alterações difíceis de serem feitas | Validar se a versão atualizada continua a funcionar de forma consistente em relação a anterior. |
| | Garantir que atualizações recentes sejam devidamente testadas. |  |

### Distrito de Entretenimento

* Testes que envolvem características que não são as principais, mas dão suporte à elas.
* Testes mais leves

| Tour do ator coadjuvante | Tour ao beco | Tour noturno |
|--------------------------|--------------|--------------|
| Caractrísticas periféricas | Locais não populares, indesejáveis, bastidores | Quanto tempo a aplicação pode durar em execução? Quanto tempo até entrar em colapso? |
| Concentração nas características que compartilham a tela com as outras características que serão mais utilizadas. | Testar características menos prováveis de serem utilizadas e menos atrativas do ponto de vista do usuário | Desafiar o software até ele falhar. |
| No decorrer, outras características ganham espaço para o usuário. | Exercitar características poucos exploradas do produto em testes. | Descoberta de erros de acesso à memória, corrompimento de dados, entre outros. |

### Distrito Turístico
* Pontos para turistas.
* Percursos curtos, teste breve com propósito simples.
* Visitação da funcionalidade.

| Tour do Colecionador | Tour do Empresário Solitário | Tour do Super Modelo |
|----------------------|------------------------------|----------------------|
| Experimentar as funcionalidades | Viagens sozinhas e hospedagem em lugares longes do aeroporto | Diz respeito sobre a aparência e primeiras impressões |
| Colecionar as saídas de software | Visitar/testar as características mais distantes | Foco na interface |
| Visitar todos os locais possíveis e produzir todas as saídas possíveis | Caminhos mais longos | Procurar por defeitos relacionados à interface e a forma que os elementos são apresentados |

| Tour do TOGOF | Tour pelo bar escocês |
|---------------|-----------------------|
| Relacionado ao Go gof - buy one, get one | Não estão localizados nos caminhos tradicionais |
| Tour simples projetado para testar várias cópias de uma mesma aplicação de forma simultânea | Feito para aplicações grandes e complicadas |
| Identificar possíveis problemas de concorrência e compartilhamento indevido de recursos | Verificar se as características mais difíceis de serem encontradas no produto funcionam corretamente |

### Distrito Hoteleiro
* Locais de descanso
* Oportunidade do testador deixar de lado as funcionalidades primárias e dar atenção às características de apoio ou ignoradas.

| Tour pela chuva | Tour do preguiçoso |
|-----------------|--------------------|
| Passeios interrompidos | Sempre existe o desinteressado |
| Uso do botão cancelar | Trabalhar o mínimo possível |
| Testar a não habilidade de limpeza do que foi iniciado | O software deve processar padrões de forma adequada e deve executar o código de manipulação de código em branco |

### Distrito Decadente
* Lugares desagradáveis, mas alguns optam por Visitar
* Testes que precisam ser feitos para que os usuários não passem por momentos incômodos

| O sabotador | Tour antissocial | Tour obsessivo compulsivo |
| - | - | - |
| Intenção de minar a aplicação de todas as maneiras possíveis| Direção oposta, se faz o oposto do que é esperado | Repetir, refazer, copiar a mesma ação várias vezes seguidas
| Procurar por defeitos relacionados com a falta ou escassez de produtos necessários para fazer a ação | Fornecer os dados de entrada menos prováveis e visam avaliar o comportamento do software| Verificar o comportamento do software com a mesma entrada repetida várias vezes
|| Testar capacidade de tratamento de erro da aplicação|
|  | Entradas de tipos errados | 
| | Testar se as mensagens de erro são devidamente mostradas|
|  | Realizar os testes na ordem errada |
|  | Verificar se as sequências inválidas de ações são impedidas pelo software| 

## Níveis de exploração em testes Exploratórios
### Estilo Livre (Freestyle)
O objetivo do teste é fornecido ao testador para que ele possa explorar livremente o sistema.

### Alto grau de exploração
Um ou mais grandes objetivos são fornecidos ao testador, porém o testador pode testar livremente.

### Grau médio de exploração
São fornecidos um ou mais grandes objetivos, entretanto são fornecidas restrições. Podem ser fornecidas fronteiras para limitar o trabalho do testador como objetivos, prioridades, riscos, ferramentas ou funcionalidade que o testador precisa se concentrar e que precisam ser cobertas.

### Baixo grau de exploração
São fornecidas informações e é necessário que alguns passos de testes sejam seguidos e o testador é incentivado a escolher os dados de teste a serem usados nas etapas de testes.

### Totalmente com script
é um teste onde são fornecidos os passos de teste e os dados de teste ao testador, desta maneira não sobra espaço para exploração.