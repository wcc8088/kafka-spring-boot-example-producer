# Spring Boot Kafka Example - The Practical Developer

## original document
https://thepracticaldeveloper.com/spring-boot-kafka-config/

* 위 소스를 변경하여 Producer와 Consumer를 분리.


>
> Producer (8080) --> Kafka (9092) --> Consumer (8081)
> 


https://github.com/wcc8088/kafka-spring-boot-example-producer

https://github.com/wcc8088/kafka-spring-boot-example-consumer

## 실행 방법

1. Kafka를 docker 로 실행 (Port : 9092)
>$> docker-compose up -d

2. Producer 실행 (Port : 8080)
>$> mvn spring-boot:run 

3. Cosumer 실행 (Port : 8081)
>$> mvn spring-boot:run 

4. Consumer 준비 (10초 간 대기 후 응답하면 준비됨)
>$> curl localhost:8081/hello

5. Message 전송 (1번 호출 시 10개의 메시지 전송)
>$> curl localhost:8080/hello
