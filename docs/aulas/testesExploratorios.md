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
| - | Demonstrações de venda, de uso do produto | - | - |


| Tour FedEx | Tour fora do horário comercial | Tour Coletor de lixo |
|------------|--------------------------------|----------------------|
| Movimentação de dados entre entrada e saída. | Momento de trabalho de manutenção, backup, armazenamento de dados. | Avaliação metódica em blocos |
| Identificar cada característica que infleuncia ou sofre influência nos dados. | Identificar falhas resultantes da execução dessas atividades. | Cobrir determinado objetivo de forma metódica, não dependendo do tempo e verificando o mais óbvio. |
| Identificar possíveis pontos que esses dados são corrompidos no processamento. | - | - |

### Distrito Histórico
* Tem como objetivo testar softwares legado.

| Tour pelo bairro ruim | Tour pelo museu | Tour da versão anterior |
|-----------------------|-----------------|-------------------------|
| Concentrar esforços de testes em áreas com mais concetrações de defeitos. | Código antigo (legado) | Uma vez que houve uma atualização, cenários das versões anteriores devem ser novamente executados. |
| À medida que o teste caminha, outras áreas podem ficar mais problemáticas. | Registros de alterações para consulta de códigos antigos, Código apresenta documentação pobre, alterações difíceis de serem feitas | Validar se a versão atualizada continua a funcionar de forma consistente em relação a anterior. |
| - | Garantir que atualizações recentes sejam devidamente testadas. | - |

### Distrito de Entretenimento

* Testes que envolvem características que não são as principais, mas dão suporte à elas.
* Testes mais leves

| Tour do ator coadjuvante | Tour ao beco | Tour noturno |
|--------------------------|--------------|--------------|
| Caractrísticas periféricas | Locais não populares, indesejáveis, bastidores | Quanto tempo a aplicação pode durar em execução? Quanto tempo até entrar em colapso? |
| Concentração nas características que compartilham a tela com as outras características que serão mais utilizadas. | Testar características menos prováveis de serem utilizadas e menos atrativas do ponto de vista do usuário | Desafiar o software até ele falhar. |
| No decorrer, outras características ganham espaço para o usuário. | Exercitar características poucos exploradas do produto em testes. | Descoberta de erros de acesso à memória, corrompimento de dados, entre outros. |

