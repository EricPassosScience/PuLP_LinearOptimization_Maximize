# PuLP_LinearOptimization_Maximize

Neste mini-projeto vamos utilizar um dos principais frameworks para otimização linear, o PuLP. Utilizaremos esta excelente ferramenta para tentar resolver o problema de negócio a seguir: 

Aempresa Lua Smart Tech monta e testa dois modelos de smartphones, Lua1 e Lua2. Para o próximo mês, a empresa quer deicidir quantas unidades de cada modelo vai montar e depois testar.

Nenhum smartphone está em estoque desde o mês anterior e, como esses modelos serão trocados depois deste mês, a empresa não quer manter nenhum estoque para o mês seguinte.

Ela acredita que o máximo que pode vernder neste mês são 600 unidades do modelo Lua1 e 1200 unidades do modelo Lua2.

Cada modelo Lua1 é vendido por R$300,00 e cada modelo Lua2 por R$450,00. O custo dos compoentes de um Lua1 é de R$150,00 e para um Lua2 é R$225,00.

A mão de obra é necessária para a montagem e teste. Existem no máximo 10.000 horas de montagem e 3.000 horas de teste disponíveis. Cada hora de trabalho para montagem custa R$11 e cada hora de trabalho para teste custa R$15. Cada Lua1 requer cinco horas para montagem e uma hora para teste. Cada Lua2 requer seis horas para montagem e duas horas para teste.

A Lua Smart Tech deseja saber quantas unidades de cada modelo deve produzir(montar e testar) para maximizar o seu lucro líquido, mas não pode usar mais horas de trabalho do que as disponíveis e não deseja produzir mais do que pode vender.

### Documentação
https://pypi.org/project/PuLP/

https://coin-or.github.io/pulp/

### Parâmetros
- Ai = Número máximo de smartphones modelo tipo i para vender este mês, onde i pertence ao conjunto {Lua1, Lua2}
- Bi = Preço de venda de smartphones modelo tipo i, onde i pertence ao conjunto {Lua1, Lua2}
- Ci = Preço de custo das peças componentes para smartphones modelo tipo i, onde i pertence ao conjunto {Lua1. Lua2}
- Di = Custo de mão de obra de montagem por hora de smartphones modelo tipi i, onde i pertence ao conjunto {Lua1, Lua2}
- Ei = Custo de mão de obra de teste por hora de smartphone modelo tipo i, onde i pertence ao conjunto {Lua1, Lua2}
- F = Número máximo de horas de trabalho de montagem
- G = Número máximo de horas de trabalho de teste
- Hf,i = Horas de montagem necessárias para construir cada modelo de smartphone tipo i, onde i, pertence ao conjunto {Lua1, Lua2}
- Hg,i = Horas de teste necessárias para testar cada modelo de smartphone tipo i, onde i pertence ao conjunto {Lua1, Lua2}

### Variável de Decisão
- Xi = Número de smartphones modelo tipo i a produzir este mês, onde i pertence ao conjunto {Lua1, Lua2}

Também definiremos restrições, para que não tenhamos valores negativos e valores que estão fora dos definidos no problema de negócio. 

### Restrições
- O número de smartphones modelo tipo i a seremn produzidos não pode ser negativo, ou seja, Xi >=0, onde i pertence ao conjunto (Lua1, Lua2).
- O número total de horas de montagem não pode ser maior que o número máximo de horas de mão de obra de montagem disponíveis
- O número total de horas de teste não pode ser maior que o máximo de horas de mão de obra de teste disponíveis.
- O número de smartphones modelo tipo i a serem produzidos não pode ser maior que o número máximo de smartphones modelo tipo i a serem vendidos neste mês, onde i pertence ao conjunto {Lua1, Lua2}
