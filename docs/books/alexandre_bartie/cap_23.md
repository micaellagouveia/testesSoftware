# 23. Medições

Durante o processo de desenvolvimento de um software, vem à tona uma infinidade de dúvidas e questões. Os dilemas que surgem muitas vezes exigem que decisões sejam tomadas e geralmente existe algum risco associado. O objetivo da equipe é obter o sucesso do desenvolvimento do software, e isso implica em minimizar os riscos através de um bom processo de tomada de decisões.

As respostas às deciões estão contidas nas diversas informações que o próprio processo de desenvolvimento está gerando. Basta implantarmos um processo que contemple o registro dessas informações e então utilizá-las da forma mais inteligente possível.

## 23.1. Indicadores de Cobertura

Os indicadores de cobertura fornece o quanto, percentualmente, o produto de software foi adequadamente testado. Essa medida está, na maioria das vezes, relacionada a quantos requisitos de software foram submetidos a testes (_requeriment-based_) ou o quanto das linhas de código foram devidamente testadas (_code-based_).

As duas estratégias citadas são complementares, pois buscam defeitos de naturezas diferentes, portanto, o emprego das duas abordagens ampliará as chances de detecção de problemas, reduzindo os riscos de migração de defeitos.

## 23.2. Indicadores de Eficiência dos Testes

Como serão necessários muitos esforços para alcançar o nível de qualidade esperado, torna-se fundamental a existência de indicadores que possibilitem avaliar o volume de erros detectados em cada etapa do processo. Aqui, nosso enfoque é avaliar a eficiência dos testes estáticos (realizados em documentos) e a eficiência dos testes dinâmicos (realizados em softwares).

### 23.2.1. Eficiência da Verificação

Medir a eficiência da verificação é muito importante, pois as atividades de verificação são trabalhosas e introduzem custos e esforços adicionais no processo. A missão da verificação é conseguir identificar o maior número de erros, de forma a reduzir, ao mínimo, o número de incidências na fases de validação. 

Uma forma para medirmos o nível de eficiência dessa etapa é através do volume de erros ocorridos após o processo de verificação. Maior a incidência de erros revela falta de qualidade das revisões de documentos, necessitando investir melhor nessas atividades. 

<p align="center">
  <img src="books/alexandre_bartie/imgs/indice_eficiencia_verificacao.png" width="200">
</p>

### 23.2.2. Eficiência da Validação

Para que possamos identificar o nível de eficiência da validação, precisamos monitorar o ambiente de produção e registrar todos os erros que ocorrerem nesse ambiente. Muitos erros em produção indicam que as atividades de validação não estão sendo bem planejadas, ou seja, o analista de teste deverá abstrair mais casos de testes, cobrindo um número maior de situações.

<p align="center">
  <img src="books/alexandre_bartie/imgs/indice_eficiencia_validacao.png" width="200">
</p>

## 23.3. Indicadores de Defeitos

Defeitos são falhas de comportamento do software em relação aos requisitos estabelecidos. A qualidade do software determina o quanto esse software está próximo dos requisitos e será através dos defeitos encontrados que determinaremos a distância que teremos de percorrer até atingirmos o patamar de qualidade desejado.

Os defeitos devem ser analisados combinando diversas técnicas e ferramentas, empregando desde simples contagens de defeitos até complexas análises estatísticas. Toda essa estrutura analítica deverá subsidiar os gerentes e profissionais envolvidos no processo de desenvolvimento de software. Será através dessas análises que decisões importantes serão tomadas, como a finalização de uma determinada etapa no processo, a implantação do software no cliente até a negociação de aumentar prazos e recursos do projeto.

Será através dos defeitos do software que estabeleceremos o nível de qualidade do processo de desenvolvimento. Através de relatórios de origens de defeitos podemos identificar os pontos mais frágeis do processo e, dessa forma, direcionar esforços para melhorar a eficiência das etapas, tornando-as mais assertivas e reduzindo os riscos de migração de erros.

O volume de defeitos de um software também proporciona um excelente indicador de confiança do produto. As análises mais comuns de defeitos estão abaixo representadas:
* Distribuição de defeitos por categorias
* Prioridade de resolução de defeitos
* Severidade dos defeitos
* Defeitos por fornecedor
* Defeitos por componente
* Idade dos defeitos
* Comportamento dos defeitos

### 23.3.1. Distribuição de Defeitos por Categoria