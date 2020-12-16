Sumário

[Introdução 2](#introdução)

[Qualidade dos Dados 3](#qualidade-dos-dados)

[Dados faltantes 3](#dados-faltantes)

[Analise inicial dos dados 3](#analise-inicial-dos-dados)

[Gráficos 6](#gráficos)

[Conclusão 9](#conclusão)

[Bibliografia 10](#_Toc58967324)

# Introdução

A Fundação Universidade Federal da Grande Dourados (UFGD) é uma
instituição federal de ensino superior vinculada ao Ministério da
Educação (MEC) e que tem sede e foro no Município de Dourados, Estado de
Mato Grosso do Sul. \[1\]

Sua missão é gerar, construir, sistematizar, inovar e socializar
conhecimentos, saberes e valores, por meio do ensino, pesquisa e
extensão de excelência, formando profissionais e cidadãos capazes de
transformar a sociedade no sentido de promover desenvolvimento
sustentável com democracia e justiça social e tem como visão ser uma
instituição reconhecida nacional e internacionalmente pela excelência na
produção do conhecimento e por sua filosofia humanista e democrática.
\[1\]

Visando atender a região como um polo de ensino e formação, oferece 88
cursos em diferentes modalidades, incluindo formação presencial, EAD,
mestrado, doutorado, especialização e residência. Conta com um corpo
discente de 9493 alunos, concentrando a maior parte de seus alunos na
graduação presencial (76,5%), pós graduação (16,9%) e graduação EAD
(6,47%). Apresenta também uma força de trabalho de 2233 funcionários,
incluindo 606 docentes efetivos, 73 docentes substitutos e visitantes,
946 técnicos e 608 funcionários terceirizados. \[2\]

O objetivo desse trabalho é analisar o comportamento de consumo elétrico
dessa universidade, calculado com base nas informações dispostas nas
digitalizações das contas de energia disponibilizadas pela universidade
que cobre maior parte dos meses entre os anos de 2015 e 2020 para três
unidades de consumo (UC):

  -- -- -- -- -- --
                 
                 
                 
  -- -- -- -- -- --

**UCNome do CampusDistribuidoraSubgrupoEndereçoUC1**Unidade II UFGD -
FUNDACAO UNIVERSIDADE FEDERAL DA GRANDE DOURADOSEnergisaA4Rod Dourados
Itahum, , Km 12 - Rural - CEP: 79804-970 - Dourados -
MS90021100**2**Reitoria - FUND UNIV FED DA GDE DOURADOSEnergisaA4RUA
JOAO ROSA GOES, 1761 - VILA PROGRESSO \_ DOURADOS - MS -
79825-070743143**3**MoradiaEnergiaA4Rua Joao Ayres da Silva, 100 - Altos
do Indaia - CEP: 79823-672 - Dourados - MS31088821

Dentro das informações disponibilizadas pela UFGD, a UC 1 representa
cerca de 95% do consumo de energia identificado. Nesse estudo,
descartamos a analise dos dados da UC 2 e UC 3.

# Qualidade dos Dados

## Dados faltantes

Dentro das informações disponibilizadas pela universidade, os dados
obtidos refletem o consumo de energia elétrica da UC 1 entre o período
de junho de 2015 e maio de 2020. Em uma análise inicial, é possível
notar que os dados referentes aos meses de janeiro e fevereiro de 2018,
assim como janeiro e fevereiro de 2019 estão faltando, não sendo
preenchidos as informações referentes a esses quatro meses.

Durante o período analisado, também é perceptível a mudança no formato
de publicação das contas da Energisa. Não somente é variações nas
posições das informações como também na identificação dos nomes dos
diferentes consumos, necessitando um olhar cauteloso para evitar a perda
ou erro de interpretação das informações. Ocorre também em alguns
momentos uma incerteza em relação ao consumo de reativos onde, ao
usualmente ser apresentado um fator de potencia de 0,92, alguns meses
não apresentavam dados referentes a energia reativa e um fp de 1.

## 

## Analise inicial dos dados

Em uma analise superficial dos dados, após transferência manual dos
valores a uma tabela de Excel, podemos ponderar algumas conclusões
iniciais a partir das análises a seguir:

**Demanda:**

A UFGD contratou uma demanda fixa de 1150W entre a maior parte de 2015 e
2016. Em junho de 2016 esse valor foi aumentando para 1600W. As demandas
registradas em ponta no período total variaram entre 326,88 e 889,92W,
enquanto a demandas fora de ponta registradas variaram entre 336,96 e
1496,16W.

Sem realizar uma análise estatística nesses valores, é notável que a UC1
teve períodos de grande diferença entre a demanda disponível e o real
consumo, fato que gerou grandes encargos a universidade.

Com fim de comparação, descartando o ano de 2020 devido a pandemia
global causada pelo vírus Covic-19, na menor demanda registrada fora de
ponta (452,16 W registrado no mês de julho de 2015) foram pagos
R\$15.778,00 pela subutilização da energia disponível. No ano de 2019,
para a menor demanda fp registrada de 696,96 W (agosto de 2019) foi
cobrado um valor de R\$ 17.513,50 devido a demanda não consumida fora de
ponta. É então de interesse um olhar mais profundo nos dados para
analisar os encargos relacionados com a demanda

**Reativos:**

Assim como comparado para a demanda, podemos realizar uma analise
superficial nos dados ao verificar os valores obtidos. De maneira
análoga a demanda, tomando o maior registro de energia reativa excedida
em ponta (4973 kVar/h em janeiro de 2017) e fora de ponta (45961kVar/h
em março de 2016) geraram encargos de R\$ 1194,21 e R\$ 9929,87
respectivamente.

Uma média aritmética padrão realizada nos valores registrados de energia
reativa excedida fora de ponta no período, multiplicado pela média das
tarifas aplicadas levariam a um pagamento médio mensal de \$3088,86,
somando cerca de R\$ 160620,62 no período. Embora a utilização da média
aritmética possa dar uma visão simplificada do cenário, é um indicador
que, assim como a demanda, há espaço para uma analise mais significativa
desses dados.

Desta forma podemos observar que existe um argumento plausível para
analise da demanda contratada, assim como outras considerações
relevantes a injeção de reativos na rede e possibilidade de geração e
correção de fp que podem ser avaliados em estudos futuros.

**Consumo:**

Para interpretação inicial, plotamos o gráfico de consumo total da UC 1
ao longo de 2015-2019, excluindo da analise o ano de 2020 devido a
situação de imprevisibilidade diante da pandemia global.

Utilizando uma curva de tendencia baseada em uma função polinomial de
quarto grau (figura 1). Embora obtemos um R^2^ pequeno (0,2298) podemos
utilizar esse modelo para prever o comportamento do consumo nos próximos
2 anos (Figura 2).

[\[CHART\]]{.chart}

Figura 1- Consumo

[\[CHART\]]{.chart}

Figura 2 - Projeção de consumo base 2015-19

No entanto, o crescimento obtido quando utilizando a função de previsão
do Excel apresenta uma variação muito grande, dificultando uma
interpretação do crescimento de consumo. Utilizando uma base de dados
apenas dos valores entre 2015 e 2018 (figura 3), podemos enxergar uma
tendencia de crescimento mais expressiva.

[\[CHART\]]{.chart}

Figura 3 - Projeção de consumo base 15-18

A variação obtida por esse método, no entanto diminui o grau de
confiabilidade da análise. Ferramentas mais sofisticadas de analise
serão utilizadas na segunda parte da avaliação para complementar esse
estudo, procurando fornecer uma análise com maior confiabilidade.

É importante também ressaltar que no ano de 2020 a UC 1 iniciou a
injeção de energia na rede, evidenciado pelos créditos aplicados nas
contas posteriores a fevereiro de 2020. O verdadeiro impacto ainda não
pode ser propriamente mensurado pelo curto tempo em que se iniciou a
geração.

Essa energia provem de geração solar, viabilizado após investimento de
R\$ 4,5 milhões realizado sobre termo de Execução Descentralizada (TED),
via Secretaria de Educação Superior (SESU-MEC), no ano de 2018. \[3\]

A pretensão do projeto é a ampliação da geração solar para atender 100%
do consumo de toda a universidade, incluindo a unidade 1, Fadir e
Fazenda, possibilitando também estudos nessa área. \[3\]

# Gráficos

# 

[\[CHART\]]{.chart}

Figura 4 - Demanda fora de Ponta vs Demanda Contratada

[\[CHART\]]{.chart}

Figura 5 - Consumo de energia em ponta e fora de ponta

[\[CHART\]]{.chart}

Figura 6 - Energia Reativa em ponta e fora de ponta

[\[CHART\]]{.chart}

Figura 7 - Crescimento das Tarifas

[\[CHART\]]{.chart}

Figura 8 - Energia Ativa injetada e Tarifa

# Conclusão

Essa analise buscou preparar os dados fornecidos pela Federação
Universidade Federal de Grande Dourados para posterior estudo de
viabilidade econômica de migração para o mercado livre. Para tal, as
informações foram digitalizadas para uma tabela com o uso do software
Excel.

Um estudo preliminar sobre os dados revelou que há interesse em estudar
a migração para o mercado livre, identificando grandes divergências
entre a demanda contratada e medida.

Ainda que a universidade esteja realizando a implementação de uma
fazenda solar para suprir sua necessidade energética, uma interpretação
do cenário de consumo via mercado livre comparado com auto suficiência
via geração solar pode gerar dados de interesse para estudos futuros.

# Bibliografia

  -- --
     
     
  -- --

\[1\] UFGD, "UFGD - Perguntas Frequentes," \[Online\]. Available:
https://portal.ufgd.edu.br/setor/acessoainformacao/perguntas-frequentes.
\[Acesso em 12 Dezembro 2018\].\[2\] UFGD, "UFGD em Numeros 2018," 2018.
\[Online\]. Available:
https://files.ufgd.edu.br/arquivos/arquivos/78/PLANEJAMENTO/ufgd_diplan.pdf.
\[Acesso em 15 Dezembro 2020\].\[3\] "UFGD economiza quase R\$ 60 mil em
energia com implementação de Usina Solar," \[Online\]. Available:
https://portal.ufgd.edu.br/noticias/ufgd-economiza-quase-r-60-mil-em-energia-com-implementacao-de-usina-solar.
\[Acesso em 15 Dezembro 2020\].
