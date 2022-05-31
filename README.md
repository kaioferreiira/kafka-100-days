# #100DaysOfCode com Apache Kafka

Essa é uma iniciativa de 100 dias com o Kafka. É um desafio que ajuda os desenvolvedores 
a criar hábitos de codificação fortes com um caminho de aprendizado autodirigido. 

As etapas a seguir são para desenvolvedores interessados em trabalhar com streaming de eventos usando
o Apache Kafka®, essa sequencia é baseada em uma curva de aprendizado proposta pela própria Confluence,
mas iremos adaptar conforme necessidade.

Para iniciar o projeto, vamos compartilhar nosso progresso todos os dias nas mídias sociais ( Twitter , LinkedIn – onde quiserermos)
e inclua#100DaysOfCode #ApacheKafka

## As regras básicas são:

1. Aprenda Kafka na prática por pelo menos uma hora, todos os dias, pelos próximos 100 dias
   1. Neste item irei modificar, vou reservar 1h por dia, mas somente por 5 dias na semana, pois vou rever os conteúdos e próximos passos.
2. Tweetar o progresso usando as tags #100DaysOfCode, #ApachaKafka ou #100DaysOfKafka
3. Commitar e deixar registrado o progresso

## Recomendações

1. Tente usar Java, apesar de Kafka ter APIs em outras linguagens, a API Java é a mais rica! 
2. Controle e injeção de dependencia: Para realizar o testes usaremos Java, ao decorrer das atividades precisaremos usar uma ferramenta para o controle de
    dependencias, usarei o[Gradle](https://gradle.org/guides/#getting-started).
3. Tenha o [SDKMan](https://sdkman.io/), instalado, ele vai te possibilitar controlar as versões do Java encontradas na sua máquina. 

## Cronograma

- [X] [**Dia 001**](./dia-001/README.md) - Introdução ao Apache Kafka
- [X] [**Dia 002**](./dia-002/README.md)  - O que são Events?  


[//]: # (  3	Topics	In Kafka, all events are stored in topics—ordered, immutable, append-only logs. Learn how to create and work with Kafka topics.)
[//]: # (  4	Partitions	Kafka topics are made up of partitions, which can be spread across multiple brokers in a cluster. Learn how partitions can help you to increase throughput and scale your applications.)
[//]: # (  5	Brokers	Kafka brokers are fast and easy to scale, due in large part to their simplicity. Learn a few basics about brokers to see why they scale so well.)
[//]: # (  6	Producers	Producers, part of the Kafka client library, make it easy to send events to Kafka topics. They handle things like partition assignment, serialization, compression, and more.)
[//]: # (  7	Consumers	Consumers allow us to read events from Kafka topics so we can use them in our applications. Consumer groups make it easy to share the workload across multiple instances of our application.)
[//]: # (  8	Kafka Connect	Kafka Connect is a no-code integration API provided as part of Kafka. Stream data out of other systems like databases and MQs into Kafka, and from Kafka down to other systems like NoSQL stores and more!)
[//]: # (  9	Kafka Streams	Kafka Streams is a core part of the Kafka ecosystem and provides a Java library for doing stateful stream processing. &#40;Java not your thing? Check out ksqlDB!&#41;)
[//]: # (  10	ksqlDB	ksqlDB is a specialized kind of database that is optimized for stream processing applications, uses SQL, and exposes a REST interface to applications, which can submit new stream processing jobs to run and query the results.)
[//]: # (  11	KRaft	Kafka is replacing ZooKeeper with KRaft, which will make Kafka lighter, faster, and much more scalable. It's still in preview, but you can take it for a spin.)

[//]: # (  - [X] [**Dia 001**]&#40;./dia-001/README.md&#41; - Instale o Apache Kafka &#40;escreva um Dockerfile, ou instale ele localmente&#41; [[1]]&#40;https://vepo.github.io/posts/rodando-o-apache-kafka-localmente&#41;)
[//]: # (- [x] [**Dia 002**]&#40;./dia-002/README.md&#41; - Crie um produtor simples que envia um arquivo texto para um tópico, cada linha deve ser uma mensagem [[2]]&#40;https://vepo.github.io/posts/enviando-mensagens&#41;)
[//]: # (- [X] [**Dia 003**]&#40;./dia-003/README.md&#41; - Crie um consumidor simples que lê as mensagens de um tópico [[3]]&#40;https://vepo.github.io/posts/recebendo-mensagens&#41;)
[//]: # (- [ ] **Dia 004** - Altere o seu produtor para enviar um POJO usando um serializador JSON que você mesmo escreveu. Use [Jackson]&#40;https://www.devmedia.com.br/introducao-ao-jackson-objectmapper/43174&#41;)
[//]: # (- [ ] **Dia 005** - Altere seu consumidor para receber um POJO usando um desserializador JSON que você mesmo escreveu. Use [Jackson]&#40;https://www.devmedia.com.br/introducao-ao-jackson-objectmapper/43174&#41;)
[//]: # (- [ ] **Dia 006** - Crie um nome consumidor com um novo [group.id]&#40;https://kafka.apache.org/documentation/#consumerconfigs_group.id&#41; e veja como os dois consumidores funcionam em paralelo.)
[//]: # (- [ ] **Dia 007** - Adicione ao menos mais uma instância do Kafka e tente conectar no cluster, não somente em um broker. )
[//]: # (- [ ] **Dia 008** - Explore os scripts `kafka-topics` e `kafka-consumer-groups`. Se você usa docker eles estão dentro do seu container, se usa local estão na pasta `bin` do Kafka.)
[//]: # (- [ ] **Dia 009** - Altere as configurações do seu tópico, adicione mais partições e mude o fator de replicação. Verifique as possiblidades. [[4]]&#40;https://vepo.github.io/posts/anatomia-de-um-topico&#41;)
[//]: # (- [ ] **Dia 010** - Rode mais de uma instância do mesmo consumidor para um tópico com mais de uma partição e veja como funciona.)
[//]: # (- [ ] &#40;...&#41;)
