# O Papel dos Bancos de Dados SQL e NoSQL na Engenharia de Dados

Created: September 19, 2022 6:34 PM
Tags: Estudos

Este arquivo tem como objetivo a conclusão de um artigo para um desafio de projeto proposto pela Digital Innovation One inc. - DIO, com o propósito de registrar alguns conceitos básicos a cerca do papel dos bancos de dados SQL e NoSQL voltados ao contexto de engenharia de dados, mais específicamente.

**O que é um Banco de Dados Relacional (SQL)?**

A AWS Amazon, define como uma coleção de itens de dados com relacionamentos predefinidos entre si. Esses itens são organizados como um conjunto de tabelas com colunas e linhas. As tabelas são usadas para reter informações sobre os objetos a serem representados no **banco de dados.**

A linguagem padrão utilizada para manipulação de registros de dados relacionais é chamado de **SQL**, que significa “***Structured Query Language***”.

Existem no mercado vários sistemas de gerenciamento de bancos de dados utilizados com a finalidade de construir, armazenar e gerenciar esses bancos de dados, dentre eles podemos destacar os SGBD’s Oracle, MySQL e PostegreSQL que hoje, estão entre os mais utilizados.

**Bancos de Dados NoSQL**

Com o avanço da tecnologia e o crescente volume de dados gerados atualmente, os Bancos de Dados Relacionais tiveram limitações relacionados a sua aplicabilidade, mais especificamente, o fato de sua escalabilidade ser vertical, ou seja, baseada na expansão de uma rede a partir da adição de mais energia e memória à unidade de processamento principal do sistema. Nesse contexto, torna muito custoso para se aumentar o volume de processamento e armazenamento de dados, nesse contexto surgiu a necessidade de se criar bancos de dados com escalabilidade horizontal.

Os bancos de dados NoSQL, que tem como tradução literal “***Not Only SQL***” ou “*Não Somente SQL*”, que oferece ao usuário, como o próprio nome já sugere, estruturas que não necessariamente têm relacionamento e rigidez de eschema.

Os bancos NoSQL são divididos em 4 tipos, são eles:

- Orientados à colunas/tabelas (Hbase e Cassandra);
- Orientados à Documentos (Cassandra e MongoDB);
- Orientados à Chave-Valor (REDIS e MemcacheD);
- Orientados à Grafos (Neo4j).

**Os bancos NoSQL vieram para substituir os bancos SQL?**

Essa é uma pergunta muito comum no meio, já que os bancos de dados NoSQL foram criados para essa nova fase de dados, quer dizer que eles irão deixar os bancos SQL obsoletos? E a resposta é não, os sistemas de gerenciamento bancos de dados (**SGBD’s**) SQL ainda são maioria no mercado e continuam sendo a melhor alternativa para o caso de utilizar um modelo que precise de relacionamento e dados estruturados, já que sua tecnologia, na maioria das vezes é mais simples de se implementar e mais barata (para essa finalidade especificamente).

****NoSQL vs SQL:****

| SQL | NoSQL |
| --- | --- |
| Armazenamento de Dados Estruturados por Tabela | Armazenamento de Dados estruturados e não-estruturados por colunas, grafos, chave-valor e documentos. |
| Esquema estático | Esquema dinâmico |
| Maturidade de suporte maior (geralmente pago) | Suporte por comunidade independente (open source) |
| Escalabilidade vertical | Escalabilidade horizontal |
| Pago | Gratuito |
| O desempenho não é alto em todas as consultas. Não suporta pesquisas e cruzamentos muito complexos. | Alto desempenho em consultas |
| Necessidade de predefinição deum esquema de tabela antes da adição de qualquer dado | Altamente flexível (fácil adição de colunas e campos de dados não estruturados) |

**Como encontrar algo armazenado em uma Banco NoSQL, já que ele não é necessariamente estruturado?**

Nos SGBD’s Relacionais, conseguimos realizar nossas famosas *queries,* utilizando a linguagem SQL, para armazenar, consultar e manipular dados e nos SGBD’s NoSQL, como acontece?

O fato de não ter um sistema rígido, torna mais importante a etapa de criação desse banco de dados para que possamos fazer essas consultas de forma correta e torne as informações realmente úteis e cada SGBD tem em sua estrutura uma forma diferente de realizar essas consultas. Não é por que você está utilizando um banco não relacional que não se vê a necessidade de pensar na modelagem do mesmo.

Para o **engenheiro de dados** é fundamental que ele tenha domínio da linguagem SQL e do SGBD’s ao qual a empresa trabalha, pois é a base de seu trabalho.

# Introdução a engenharia de dados

O profissional engenheiro de dados é responsável por:

- Coletar → estruturação de dados
- Processar → processamento dos dados
- Armazenar → visualização das informações
- Consumir → privacidade e aplicação dos dados

Para isso se faz necessário:

- Garantir que os dados estejam disponíveis para a análise de forma segura realizando a coleta, seja em batch ou streaming, de forma a disponibilizar a limpeza e transformação dos dados
- Realizar o processo de ETL e criar pipelines de dados
- arquitetar bancos de dados (SQL e NoSQL) a fim de armazenar e criar repositórios de arquivos que facilitem as consultas
- Prover a disponibilidade desses dados para que sejam consumidos pelas suas respectivas áreas, seja por API’s, arquivos, diretamente de bancos de dados ou relatórios.

Já os dados, por sua vez, têm sua **importância** para a empresa em:

- Aumentar a precisão na tomada de decisão;
- Previsão de cenários futuros com base em dados já coletados;
- Maior eficiência e aumento na produtividade com aplicação geral;
- Diminuição de custos e riscos ao negócio aplicado.
    
    ```
    			DADOS          +           PROCESSAMENTO    =      INFORMAÇÃO
    (Brutos, não organizados e sem contexto)                     (com contexto e baseados em negocios)
    ```
    

**Cultura Data-Driven**
Uma abordagem orientada a dados que significa tomar decisões estratégias com base na análise e interpretação dos dados e permite que as empresas tomem decisões com base em informações relevantes para o negócio aplicado.

**Jornada do engenheiro de dados:**

Aqui podemos acompanhar um jornada, que com base em vários cursos e professores, teriam o básico que todo engenheiro de dados deve ter como competência em seu currículo:

- Linguagem de programação: Python, Scala e R;
- Automação Scripting: Shell (cli) e Crontab (scheduling);
- Conhecimentos em bancos de dados: MySQL, PostgreSQL, MongoDB…;
- Saber realizar pipelines / ETL (extração, transformação e carga de dados): Apache Spark, Spark Streaming, Kafka, Airflow…;
- Ferramentas de Big Data: Data Lake, Data Lakehouse, Apache Hadoop e MLOps;
- E saber Cloud Computing: Google Cloud Plataform, AWS e Azure.

 

> "O valor está em converter os dados em informação!"
> 

**O que é um Pipeline de dados?**
Trata da coleta, ingestão, preparação, processamento e apresentação de dados de forma a transformar os dados armazenados em valor, para consumo ou venda dada uma aplicação já pré-estabelecida.

**DataOPS** :

É uma pratica de gerenciamento de dados colaborativo focada em melhorar a comunicação, integração e automação de fluxos de dados entre gerenciadores de dados e consumidores de dados de uma organização.
O objetivo é entregar valor com mais rapidez, criando entrada previsível e gerenciamento de mudanças de dados, modelos de dados e artefatos relacionados.

![Untitled](O%20Papel%20dos%20Bancos%20de%20Dados%20SQL%20e%20NoSQL%20na%20Engenha%20cbe5c471d53b4e118c7b48598eb53ee3/Untitled.png)

## DATA WAREHOUSE

É uma arquitetura de armazenamento projetada para conter dados extraidos de sistemas de transações, armazenamentos de dados operacionais e fontes externas e combina esses dados em um formulário de resumo agregado adequado para a análise de dados em toda a empresa e relatórios para necessidades de negocios predefinidas.

**OLTP** = Online Transactional Processing
Foco - Operações do dia a dia
Origem - Transações em tempo real da organização
Performance - milissegundos
Volatilidade - Atualizações curtas e rápidas iniciadas pelo usuário
Desing - Normalizado

**OLAP** = Online Analytical Processing
Foco - Suporte a decisão
Origem - bases de dados de sistemas transacionais - OLTP
Performance - minutos/horas
Volatilidade - Geralmente grande devido à agragação de grandes conjuntos de dados
Desing - Desnormalizado

![Untitled](O%20Papel%20dos%20Bancos%20de%20Dados%20SQL%20e%20NoSQL%20na%20Engenha%20cbe5c471d53b4e118c7b48598eb53ee3/Untitled%201.png)

## ETL

ETL (*Extract, Trasnform, Load*) é um processo automatizado que coleta dados brutos, extrai as informações necessárias para análise, transforma em um formato que atende às necessidades de negócios e carrega em um data *warehouse.*

É responsável por fazer a movimentação dos estágios de um *Data Warehouse*.

**Tipos de Movimentação**

- Movimentação de volume de dados:
    - Cargas completas - *truncate* & *load*
    - Cargas incrementais - data/id
    - Frequência (diária, semanal, mensal)
- Pode melhorar significativamente a qualidade dos dados
    - Qualidade e padronização/validação dos dados
    - Metadados (descrevem os atributos dos dados - significado)

**Desafios**

- Escalabiliade - um dos recursos mais importantes
- Acurácia - garantir precisão dos dados
- Manusear fontes de dados diversas - (estruturados/não estruturados)

### Data Marts

É um subconjuto de um data Warehouse orientado para um linha de negócios específica, contêm repositórios de dados resumidos coletados para análise em uma seção ou unidade específica dentro de uma organização, Ex: departamento de vendas, marketing...

![Untitled](O%20Papel%20dos%20Bancos%20de%20Dados%20SQL%20e%20NoSQL%20na%20Engenha%20cbe5c471d53b4e118c7b48598eb53ee3/Untitled%202.png)

### 

Com esse artigo, pudemos passar de forma introdutória alguns conceitos importantes sobre SQL, NoSQL, a profissão de engenheiro de dados e a importância dos dados para essa profissão e para o mercado no geral. Se você chegou até aqui, espero que tenha gostado e se tiver alguma pergunta, dúvida ou opinião, pode entrar em contato comigo, pelas redes no meu README principal, até a próxima!
