# Aula 2
## Conceitos Fundamentais: V&V, Erro, Defeito e Falha

### **Teste de Software** 
* É um processo destinado a dar certeza que um código do computador faz o que foi projetado. Deve ser previsível e consistente, não oferencendo surpresas aos usuários.
* Testar um programa significa aumentar a qualidade e a confiabilidade do programa.

*Testar é o processo de executar um programa com a intenção de encontrar erros*

### **V&V: Verificação e Validação** 
Garante a qualidade do software. Ocorre em cada estágio do processo de software.
* Verificação da qualidade do produto (técnicas estáticas ou dinâmicas).
* Validação do produto usando as especificações fornecidas pelo cliente.
* Estabelece confiança de que o software está adequado ao seu propósito (termos técnicos -> funcionamento, termos negociais -> requisitos funcionais, não funcionais , de qualidade)

**Verificação**: atividades que auxiliam a avaliar se um produto em uma determinada fase do desenvolvimento satisfaz os requisitos estabelecidos. Atividade mais técnica. (TÉCNICA)

**Validação**: Auxiliam a confirmar se o produto satifaz sua intenção de uso (expectativas do usuário). Atividade que depende de conhecimento do domínio do problema tratado pelo Software. (USUÁRIO)

*É possível fazer um teste unitário com o objetivo de validar?*


### **Produto de Software**

*Conjunto de programas de computador, procedimentos e possível documentação, além de dados associados*


### **Processo x Produto**

Existe relação entre processo e produto, em termos de qualidade. Porém, argumenta que não é o único fator que causa impacto. Por isso, sugere-se aprofundar o estudo na qualidade do produto.

Testar exaustivamente e completamente os testes é algo que, se possível for, é inviável e caro, pois significa que não existem falhas não conhecidas ao final dos testes.

Razões:

* O domínio de possíveis entradas e respectivas saídas de um sistema é muito grande para ser completamente testado;
* O sistema pode possuir um grande número de estados;
* Os problemas tratados pelo sistema podem ser por demais complexos para serem totalmente tratados;
* Pode não ser possível replicar completamente o ambiente onde o sistema vai operar quando em produção;
* Mudanças podem injetar novos defeitos.

### **Erro, defeito ou falha?**

1. Erro: Uma ação humana que pode resultar em um produto com defeitos. Um erro pode levar a inclusão de uma falha no sistema, fazendo com que o mesmo não funcione corretamente.

*O ser humando está sujeito a cometer um erro.*

2. Defeito: Em um sistema pode ocorrer devido a omissão de informações, definição de dados ou comandos/instruções incorretas nos programas, dentre outros fatores. Um defeito é uma consequência de um erro cometido.

*Produz defeito(bug) no código ou documento.*

3. Falha: Uma falha ocorre quando um programa ou um conjunto de programas não se comporta conforme o esperado ou apresenta resultados diferentes dos previstos. 

*Se um defeito for executado, o sistema irá falhar.*

Erro → Defeito → Falha
