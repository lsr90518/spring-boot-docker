# spring-boot-docker  

### pom.xml作成

ここで新しいバージョンのプラグインを探せば良い
(http://mvnrepository.com/artifact/com.spotify/docker-maven-plugin)
(http://mvnrepository.com/artifact/org.springframework.boot/spring-boot-starter)
http://mvnrepository.com/

### javaクラスを作成

src/main/java/hello/
の下にApplication.javaを作成し、Applicationクラスを作成

### mavenでビルド

mvn install
java -jar target/spring-boot-docker-0.1.0.jar

http://localhost:8080/  
で確認できる。

### make docker

dockerを起動する
起動できない場合は参考を(https://stackoverflow.com/questions/26686358/docker-cant-connect-to-boot2docker-because-of-tcp-timeout/27804765#27804765)

src/main/docker/Dockerfile  
を作成

mvn package docker:build

docker run -d -P lsr90518/spring-boot-docker

http://192.168.99.100:8080/  
ここで確認できる



192.168.99.100はdockerにあるコンテナーのipアドレスで、localhostの場合もありますし。状況によって異なる場合があるはず。
