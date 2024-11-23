FROM openjdk:21-ea-33-oraclelinux7

RUN mkdir -p /home

COPY . /home

WORKDIR /home

ENTRYPOINT [ "java","-jar","banking-v1.jar" ]

