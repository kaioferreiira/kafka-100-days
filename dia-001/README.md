# Dia 001 

Apache Kafka surgiu como uma alternativa eficiente para o consumo de publicação de dados em larga escala.
Mais do que uma  ferramenta de mensageria, definindo e permitindo que sistemas distribuídos possam se comunicar por 
meio de troca de eventos, ela nos permite gerenciar todo seu contexto de message por um Broker(servidor/módulo de mensagens).

Toda comunicação das mensagens e seu broker é gerenciada pelo Zookeeper, uma ferramenta que 
direciona e organiza os fluxos de dados,  salvando, recuperando e manipulando.

#Introdução

Para iniciar nosso entendimento e validação, irei criar um arquivo Dockerfile, contendo uma imagem do Kafka e o
Zookeeper. Dentro da pasta voce encontrara o arquivo [**docker-compose-kafka**](./docker-compose-kafka.yml).

Execute no terminal o comando a seguir para subir localmente o kafka:
```bash
docker-compose -f docker-compose-kafka.yml up -d 
```

Para verificar se ele está em execução:

```bash
$ docker ps -a
CONTAINER ID   IMAGE                 COMMAND                  CREATED         STATUS         PORTS                                                  NAMES
1ba279a1703c   bitnami/kafka:2       "/opt/bitnami/script…"   6 minutes ago   Up 6 minutes   0.0.0.0:9092->9092/tcp                                 dia-001_kafka_1
43636b5b2906   bitnami/zookeeper:3   "/opt/bitnami/script…"   6 minutes ago   Up 6 minutes   2888/tcp, 3888/tcp, 0.0.0.0:2181->2181/tcp, 8080/tcp   dia-001_zookeeper_1

```

Agora vamos interagir com nosso container e plublicar um evento, para isso teremos que entrar no container:
```bash
docker exec -it dia-001_kafka_1 bash 
```

As pastas contendo os arquivos do Kafka estão dentro do diretorio opb -> bitnami -> kafka -> bin:
```bash
/opt/bitnami/kafka/bin
```

Ao seguir o caminho das pastas veremos todos os arquivos de configs do kafka

```bash
!@1ba279a1703c:/opt/bitnami/kafka/bin$ ls
connect-distributed.sh        kafka-configs.sh             kafka-delete-records.sh   kafka-mirror-maker.sh                kafka-server-start.sh               kafka-verifiable-producer.sh     zookeeper-shell.sh
connect-mirror-maker.sh       kafka-console-consumer.sh    kafka-dump-log.sh         kafka-preferred-replica-election.sh  kafka-server-stop.sh                trogdor.sh
connect-standalone.sh         kafka-console-producer.sh    kafka-features.sh         kafka-producer-perf-test.sh          kafka-storage.sh                    windows
kafka-acls.sh                 kafka-consumer-groups.sh     kafka-leader-election.sh  kafka-reassign-partitions.sh         kafka-streams-application-reset.sh  zookeeper-security-migration.sh
kafka-broker-api-versions.sh  kafka-consumer-perf-test.sh  kafka-log-dirs.sh         kafka-replica-verification.sh        kafka-topics.sh                     zookeeper-server-start.sh
kafka-cluster.sh              kafka-delegation-tokens.sh   kafka-metadata-shell.sh   kafka-run-class.sh                   kafka-verifiable-consumer.sh        zookeeper-server-stop.sh

```

Pronto, criamos nosso arquivo docker file contendo o kafka e o zookeeper, nas próximas etapas vamos começar a entender
os conceitos do kafka e aplicar usando nosso servidor local.

