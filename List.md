# List I Don't Know

## Trunk base development

## How kubernates works

## Integration Test with CI/CD

## GRPC

## Protobuff

## ReactJS

## Kafka
- Kafka is short of message queue
- Book: `Gwen Shapira. “Kafka: The Definitive Guide.”`
- How to start:
  1. Installing Kafka (MacOS)
     1. Install Homebrew: https://docs.brew.sh/Installation
     2. Install Kafka:
        ```console
        $ brew install kafka
        ```
  2. Make sure Kafka and Zookeeper start:
        ```console
        $ brew services list
        kafka     started yourname /Users/yourname/Library/LaunchAgents/homebrew.mxcl.kafka.plist
        zookeeper started yourname /Users/yourname/Library/LaunchAgents/homebrew.mxcl.zookeeper.plist
        ```
  3. Create and verify topic:
        ```console
        $ kafka-topics --create --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --topic test
        Created topic "test".
        ```
        ```console
        $ kafka-topics --zookeeper localhost:2181 --describe --topic test
        Topic:test    PartitionCount:1    ReplicationFactor:1    Configs: Topic: test    Partition: 0    Leader: 0    Replicas: 0    Isr: 0
        ```
  4. Produce message to `test` topic:
        ```console
        $ kafka-console-producer --broker-list localhost:9092 --topic test
        >test
        ```
  5. Consume message from `test` topic:
        ```console
        $ kafka-console-consumer --bootstrap-server localhost:9092 --topic test --from-beginning
        test
        ```

## Kong
https://github.com/ardinusawan/learn-kong-basic

## GraphQL

## Elixir Plug

## Event Sourcing
  - https://tech.zilverline.com/2017/04/07/elixir_event_sourcing
  
## Android
  - Timber: Library for logging
  - ![Lifecycle](https://video.udacity-data.com/topher/2018/November/5be286d0_l4-1803sc-a-share-dialog-and-onpause-onresume-border/l4-1803sc-a-share-dialog-and-onpause-onresume-border.png)
  - [Lifecycle Cheat sheets](https://medium.com/androiddevelopers/the-android-lifecycle-cheat-sheet-part-i-single-activities-e49fd3d202ab)
