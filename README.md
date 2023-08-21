# TripleTen-4-Projeto_Megaline


## Qual é o melhor plano?

A atividade consiste em analisar os dados da empresa de telecomunicações Megaline. A empresa oferece aos seus cliente planos pré-pagos, Surf e Ultimate. O departamento comercial quer saber quais dos planos dão mais receita para ajustar o orçamento de publicidade.

Será realizada uma primeira análise dos planos baseados em uma pequena seleção de clientes. Terei dados de 500 clientes da Megaline: que clientes são, de onde eles são, qual plano usam, o número de chamadas que eles fizeram e mensagens que eles enviaram em 2018. O trabalho é analisar o comportamento dos clientes e determinar quais planos pré-pagos dão mais receita. E analisar se a receita média dos usuários da área de NY-NJ é diferente dos usuários de outras regiões.

Os planos são:

Surf

Preço mensal: $20
500 minutos mensais, 50 mensagens de texto, e 15 GB de dados
Depois de exceder os limites do pacote:
    1 minuto: 3 centavos
    1 mensagem de texto: 3 centavos
    1 GB de dados: $10

Ultimate

Preço mensal: $70
3000 minutos mensais, 1000 mensagens de texto, e 30 GB de dados
Depois de exceder os limites do pacote:
    1 minuto: 1 centavo
    1 mensagem de texto: 1 centavo
    1 GB de dados: $7

A empresa Megaline em relação a cobrança:

    Para chamadas, cada chamada individual é arredondada para cima: mesmo se uma chamada tenha durado apenas um segundo, será contado como um minuto.

    Para trafego de web, sessões individuais de web não são arredondadas para cima. Ao invés disso, o total do mês é arredondado para cima. Se alguém usar 1025 megabytes esse mês, eles serão cobrados por 2 gigabytes. Arredonda segundos para minutos, e megabytes para gigabytes.

Primeiramente, será feita uma primeira visualização dos dados das quatro tabelas rebecidas. Procurarei por dados aausentes e outros problemas que possam afetar os resultados da análise. Então os dados serão enriquecidos para melhorar a análise futura.


## Conclusão geral

Primeiramente, foi feito a correção dos tipos de dados e o enriquecimento dos dados. Todas as tabelas que possuiam data tiveram o seu tipo mudado de objcet para datetime. As chamadas e usos de dados com zero foram retiradas das tabelas. Os minutos da tabela df_calls foi arredondado para cima, e na tabela df_net foi criado a coluna gb_used para armazenar a quantidade de gigabyes utilizados.

Em seguida, os dados das tabelas relevantes para a análise foram agregados no dataframe df_final. FOi agregado por usuário e por mês o número de chamadas, os minutos utilizados, a quantidade de mensagens, os dados utilizados, o plano, a região e a receita proveniente daquele mês.

Dessa forma, foi visto através de gráficos o comportamento dos usuários por plano. Foi visto a duração média das chamadas, a quantidade média de mensagens por mês e o uso de dados médio por mês, entre outras visualizações. Foi percebido através da análise que o comportamento dos usuários do plano surf não difere do comportamento do plano ultimate.

Sendo assim, foi análisado o valor médio da receita por plano. Foi encontrado que a parte da receita proveniente do uso adicional de minutos, mensagens ou dados vem majoritariamento dos usuários do plano surf. A receita total média é maior para os usuários do plano ultimate que está em 72 dólares, para o plano surf é de 60 dólares. Também foi identificado que a maior parte da receita é proveniente da região "NY-NJ-PA MSA". Foram feitos testes estatísticos para identificar se a receita média e a soma da receita por região eram populações estatísticas diferentes, em ambos o resultado demonstrou que as diferenças são reais.

Concluo que o melhor plano para ser feito campanha publicitária é o plano ultimate por trazer uma receita média maior. E focar na região "NY-NJ-PA MSA" que provem maior receita.
