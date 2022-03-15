# ECS656U Coursework - Distributed Systems
Based upon https://github.com/sajeerzeji/SpringBoot-GRPC

-> The REST interface allows matricies to be uploaded as files
-> Files can be in any format
-> The component can accept matricies of arbitrary size but can only accept square matricies, otherwise an error is thrown from the REST interface
-> REST interface also triggers the matrix multiplication and presents the results
-> gRPC client code is integrated within REST interface calling the addBlock and multBlock functions on the gRPC server


Commands for preparing the enviornment (Assuming you are in the main folder e.g. the one with the pom.xml file in it)
1. sudo apt update
2. sudp apt install default-jdk maven
3. (From grpc-server folder) mvn package -Dmaven.test.skip=true
4. (From grpc-server folder) chmod 777 mvnw
5. (From grpc-server folder) ./mvnw spring-boot:run -Dmaven.test.skip=true
6. (From grpc-client folder e.g. seperate ssh connection) mvn package -Dmaven.test.skip=true
7. (From grpc-client folder e.g. seperate ssh connection) chmod 777 mvnw
8. (From grpc-client folder e.g. seperate ssh connection) ./mvnw spring-boot:run -Dmaven.test.skip=true

