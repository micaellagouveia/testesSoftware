# Capítulo 22 - Verificação e Validação

Um sistema de software (código fonte, documentação, guia de usuário, 
relatórios, etc) devem ser desenvolvido de modo que atenda as 
demandas dos usuários. Para que esse objetivo seja alcançado é 
necessário etapas de verificação e validação em todo seu 
ciclo de desenvolvimento.

Verificação e Validação (V & V) não são a mesma coisa. Verificação 
de um sistema de software é certificar que o produto está conforme 
os requisitos do projeto. Já Validação vai além da verificação, 
validar um software é certificar que o cliente está satisfeito 
com o produto desenvolvido. 

Especificações de sistema nem sempre refletem aos reais desejos 
e necessidades dos usuários, e mesmo que reflitam, essas 
necessidades podem mudar o decorrer do projeto. Desse modo é 
necessário introduzir etapas de verificação e validação em 
todos os estágios de desenvolvimento, visando diminuir o 
retrabalho.

## Abordagens de V & V

Os processos de V & V podem ser divididos em abordagens estáticas e 
abordagens dinámicas. Abordagens estática são técnicas que analisam 
o sistema de software sem a necessidade de executá-lo. Enquanto que 
as abordagens dinâmicas necessitam de módulos funcionais do 
software, uma vez que é preciso executá-los. 

Alguns exemplos de abordagens estáticas são inspeções de software, 
revisões por pares e auditorias, já abordagens dinámicas são 
testes unitários, testes de integração, testes de estresse e 
testes de segurança.

### Planejamento de V & V

Verificação e Validação é um processo que demanda tempo e 
consequentemente dinheiro. Os envolvidos no desenvolvimento devem 
dividir os esforços tanto em abordagens dinâmicas como estáticas, 
para que assim o produto seja validado e verificado durante todo 
o projeto.

### Inspeções de Software

Inspeções de Software é um processo de V & V estático, cujo objetivo 
é revisar o sistema de softare para encontrar erros, omissões, 
anomalias e contradições. Geralmente as inspeções enfocam o código 
fonte, porém todo subproduto do projeto pode e deve ser inspecionado.

Um exemplo prático é a inspeção dos requisitos do projeto, com o 
objetivo de encontrar contradições entre os requisitos, como 
"O software deve utilizar no máximo 200Kb" e 
"o software deve ser implementado em Python".
Após a inspeção e análise, analistas de sistema podem perceber que 
não é possível atender a ambos os requisitos, já que somente o 
interpretador de Python já consome mais memória que o máximo 
estipulado.

### Análise estáticas automatizadas

As inspeções de software pode ser automatizadas uma vez definido o 
que está procurando encontrar. Um ótimo exemplo são os `linters` 
das linguagens de programação, onde é procurado inconsequências no 
estilo de programação, partes do código que nunca são executadas. 
Outro tipo de análise é automatizada é procura de falhas na folha 
de estilo dos documentos (fontes erradas, numeração incorreta, 
links quebrados, etc). 

Vale ressaltar que por ser uma análise estática, o código em si não 
precisa está em funcionamento, uma vez que não é executado e sim 
analisado.

## Testes dinámicos

Os testes dinámicos atuam diretamente sobre o código do software, 
e portanto é preciso o software já esteja em um estágio de 
desenvolvimento onde é possível executá-lo, mesmo que seja em partes.

O desenvolvimento do software costuma começar com componentes 
independentes, que são agrupados em módulos integrados que 
implementam uma funcinalidade e que quando em conjunto compõe um 
sistema. Desse modo, é lógico que se comece o desenvolvimento de 
testes com os componentes (**testes unitários**) e depois nos módulos 
(**testes de integração**) e por último nos sistemas (**testes de sistema**).

Independente de qual parte do software está sendo testada, o 
objetivo é expor erros e comportamentos indesejáveis, para que assim 
sejam consertados o mais  rápido possível. A principal diferença é 
que **nos testes de integração e nos testes de sistema é possível 
também validar requisitos**. Por exemplo, é possível implementar um 
conjunto de teste que comprove que o CRUD de um sistema está 
conforme especificado.

Os testes dinâmicos podem ser categorizados em **testes de validação** e 
**testes de defeitos**. Nos testes de validação o objetivo é demonstrar 
o software funcionando em conformidade com base em um conjunto de 
entradas válidas, desse modo um teste de validação bem-sucedido é 
aquele que no final o sistema não apresenta anomalias. Já um teste 
de defeitos tem como objetivo expor erros através de sobrecarga de 
sistema, limitação de recurso, entradas corrompidas/inválidas com o 
objetivo de verificar o comportamento do software em situações 
anômalas.



