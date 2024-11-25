FROM maven:3.9.9-eclipse-temurin-21 AS app_build_image
RUN git clone https://github.com/Horpeyemi007/JAVA_SPRING_BOOT_WITH_DOCKER_BUILD.git banking
RUN cd banking/application-files && mvn -B package -DskipTests

FROM openjdk:21-ea-33-oraclelinux7
RUN mkdir -p /home
WORKDIR /home
COPY --from=app_build_image banking/application-files/target/banking-v1.jar /home
COPY wait-for-it.sh /home
RUN chmod +x wait-for-it.sh
# ENTRYPOINT [ "java","-jar","banking-v1.jar" ]