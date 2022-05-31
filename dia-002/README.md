# Dia 002

#Introdução

Hoje em dia é bem comum e desejável que nossas aplicações se comuniquem de forma assíncrona, queremos mais interoperabilidade em nossos serviços e que eles se comuniquem e realizem informações independentemente, sendo assim, publicar eventos e consumir eventos em um canal de dados  é a forma mais atrativa para essa ideia.

## Oque são eventos?

Eventos são ações, ação de fazer algo, solicitar algo, informar algo, etc, são interações de dados que causam uma reação, e toda reação tem uma ação, para isso existe o fluxo de controle de mensageria do kafka, ele orquestra e manipula esses eventos.

O mais comum quando falamos de eventos em microsserviços, é trazer uma referência a dados publicados em uma fila, esses dados podem ser de N formatos, Json, Avro e etc.

Uma particularidade do Kafka é que ele controla os seus eventos por meio de chave e valor.
Todo evento e informação publicada, tem um formato especificado, que por meio deste formato  o Kafka consegue fazer a serialização e desserialização dos dados.

A chave de um evento Kafka não é necessariamente um identificador exclusivo de cada ação, como seria a chave primária de uma linha em um banco de dados relacional, mais provável que seja o identificador de alguma entidade no sistema, como um usuário, pedido ou um determinado dispositivo conectado.
