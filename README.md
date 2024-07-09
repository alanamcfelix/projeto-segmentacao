# Ficha Técnica: Projeto de Análise de Dados

## Título do Projeto: Projeto 1 - Segmentação

### Objetivo
O presente projeto tem como objetivo segmentar a base de clientes da loja El Mercado usando a metodologia RFM (Recência, Frequência, Valor Monetário) e identificar insights que possam orientar as estratégias de marketing e retenção de clientes. Dessa forma, pretende-se responder às seguintes perguntas: como podemos segmentar os clientes com base em seus padrões de compra? Quais são as características dos diferentes segmentos de clientes? Quais são as principais conclusões e recomendações para a empresa com base nos resultados da análise?

### Equipe
Trabalho realizado individualmente.

### Ferramentas e Tecnologias
As principais ferramentas e tecnologias utilizadas no projeto foi o Google Sheets, que foi utilizado para análise de dados, manipulação de planilhas e criação de gráficos e tabelas; as ferramentas de comunicação colaborativa como o Slack e o Zoom para colaboração e compartilhamento de informações entre as alunas da Laboratoria; por fim, a ferramenta Google Slides (ou Google Apresentação) de apresentação para criar e compartilhar os resultados da análise.

### Processamento e análises
O processamento e análise do projeto se deu seguindo os marcos propostos pelo programa. Inicialmente, a primeira etapa consistia na importação dos dados para o ambiente de análise a ser utilizado, nesse caso, a ferramenta Google Sheets. Em seguida, utilizando a fórmula IMPORTRANGE, todos os dados foram importados e o próximo passo consistiu em identificar e tratar os valores nulos ou vazios dentro da planilha de dados. Nesse caso, foram encontrados 24 clientes sem os dados de renda anual e 7 transações sem a identificação do cliente que realizou a compra. Para o primeiro caso, foi utilizado a mediana, entendendo que a mesma representa o valor do meio de um conjunto de dados, ou melhor, divide os dados em duas partes iguais. Nesse sentido, a fórmula foi utilizada para preencher com um valor que não ficasse muito distante da realidade dos dados contidos ali. Para o segundo caso, optou-se por removê-los, visto que não comprometeriam a integridade dos dados. Após tratar os valores nulos, a próxima etapa consistiu em identificar e remover os valores duplicados: toda a planilha foi selecionada, em seguida, no menu “Dados” utilizou-se a ferramenta “limpeza de dados” e “remover cópias”. Após identificar e gerenciar esses dados que se encontravam fora do escopo da análise, o próximo passo foi unir as tabelas utilizando UNIQUE+QUERY e PROCV, com os principais dados a serem utilizados para a análise posterior. A partir daí, foram criadas novas variáveis: calculou-se a recência, frequência e valor monetário para cada cliente com base em suas transações e em seu valor gasto. Para isso, calculou-se a recência, representando o tempo desde a última compra de cada cliente; a frequência, representando o número de compras realizadas por cada cliente e o valor monetário total gasto por cada um deles. Após isso, buscou-se unir as informações dos clientes em relação ao nível de escolaridade, idade, número de filhos, estado civil, renda anual e quantos deles responderam a campanha de marketing realizada pela empresa, e, por fim, quais os produtos mais comprados. Ao visualizar essas novas variáveis categóricas, buscou-se compreender e aplicar fórmulas de quartis, decis e percentis para dividir os clientes em grupos com referência ao RFM. Neste projeto, optou-se apenas pelo cálculo de quartis e percentis, sendo utilizado o percentil como referência para atribuir as pontuações para cada cliente. Realizados os cálculos, o próximo passou consistiu em segmentar esses clientes, lhes atribuindo pontuações para cada métrica RFM com base nos percentis dos dados, como mencionado anteriormente. Assim, combinou-se as pontuações RFM para formar um código RFM para cada cliente. Após atribuir as pontuações, os clientes foram segmentados em:

- Campeões: Comprou recentemente. Compra com frequência. E gasta muito!
- Clientes fiéis: Gasta um bom dinheiro. Com frequência.
- Lealdade potencial: Clientes recentes. Gastaram uma boa quantia. Compraram mais de uma vez.
- Clientes Recentes: Comprou recentemente. Mas não com frequência.
- Promissor: Compradores recentes. Mas não gastaram muito.
- Precisam de atenção: Recência, frequência e valores monetários acima da média. (Pode não ter comprado muito recentemente).
- Prestes a “hibernar”: Abaixo da média da Recência, Frequência e valores monetários. (Os perderá se não for reativado).
- Em risco: Gastou muito dinheiro e comprou com frequência. Mas há muito tempo. (Precisa trazê-los de volta)!
- Não posso perdê-los: Fez grandes compras e com frequência. Mas há algum tempo.
- Hibernando: A última compra foi feita há algum tempo. Pouco gasto e baixo número de pedidos.
- Perdido: Recência, frequência e pontuação monetária mais baixas.

#### A tabela referência utilizada para segmentação desses clientes

| Segmento | Intervalo do valor R | Média de F e M |
| -------- | -------------------- | -------------- |
| Campeões | 4 a 5                | 4 a 5          |
| Clientes fiéis | 2 a 5           | 3 a 5          |
| Lealdade potencial | 3 a 5       | 1 a 3          |
| Clientes Recentes | 4 a 5        | 0 a 1          |
| Promissor | 3 a 4               | 0 a 1          |
| Clientes que precisam de atenção | 2 a 3 | 2 a 3   |
| Prestes a “hibernar” | 2 a 3     | 0 a 2          |
| Em risco | 0 a 2                | 2 a 5          |
| Não posso perdê-los | 0 a 1     | 4 a 5          |
| Hibernando | 1 a 2              | 1 a 2          |
| Perdido | 0 a 2                 | 0 a 2          |

Dessa forma, as tabelas utilizadas no projeto representam uma forma de visualizar onde cada cliente se encontra e como a empresa pode se relacionar da melhor forma. Realizada essa etapa, o próximo passo consistiu em representar esses dados por meio de tabela resumo e gráficos com os resultados obtidos. Por fim, foi selecionado as principais informações relevantes que existem na técnica RFM, com o objetivo de responder às questões levantadas no objetivo do projeto. Após isso, foi criada uma apresentação com os resultados, conclusões e recomendações.

### Resultados e Conclusões
Os resultados da análise por segmentação RFM sugeriram insights valiosos em relação ao comportamento e às características dos clientes. Ao segmentá-los em grupos com base na recência, frequência e valor monetário, conseguiu-se identificar padrões claros de compra e engajamento de cada um deles. A análise feita aqui permitiu uma compreensão mais profunda dos diferentes perfis de clientes, desde os mais engajados e lucrativos até aqueles que correm o risco de se tornarem inativos, como no caso dos clientes Prestes a “hibernar” e “Em risco”, que estão abaixo da média da recência, frequência e valores monetários, mostrando sinais de diminuição no engajamento. Nesse caso, pode ser recomendado estratégias direcionadas para reativar esses clientes e evitar a perda deles.
Também foi identificado segmentos específicos de clientes com alto potencial de compra, como por exemplo, os "Clientes Fiéis" e "Lealdade Potencial", que podem se beneficiar de programas de fidelidade e ofertas personalizadas. Ainda nesse sentido, a análise também possibilita uma base para personalizar mensagens de marketing e comunicação com os clientes, adaptando-as às necessidades e comportamentos específicos de cada segmento.

### Limitações/Próximos Passos
Uma limitação pensada durante a análise foi a da falta de dados demográficos e/ou detalhes demográficos dos clientes, pois incorporar esses dados poderia enriquecer ainda mais a segmentação e personalização das estratégias de marketing. Para os próximos passos, seria viável considerar a exploração de outras técnicas de análise, como análise de coorte ou modelos de previsão de churn, o que foi recomendado também pelo programa.

### Links de interesse
[Projeto Segmentação - Slide de apresentação](https://docs.google.com/presentation/d/1OmYArE8WBQ184lDLPVf77FEOqEcrcCVVAdObrOelF3U/edit?usp=sharing)

[Projeto Segmentação - Base de dados](https://docs.google.com/spreadsheets/d/1wrfeF8Nc6OG8oVf1QkZqndDF1Nd2LL3KMJBVaDOOTzg/edit?usp=sharing)

[Projeto Segmentação - Vídeo de apresentação](https://www.loom.com/share/838bb52f48c348539a5d5f5288d3f0a0?sid=58b84a1d-a983-4998-920d-a233d1f30655)
