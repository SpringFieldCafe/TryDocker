FROM ubuntu:22.04

RUN apt update

ENV DEBIAN_FRONTEND=noninteractive

RUN apt install -y build-essential

WORKDIR /usr/src/cpp

COPY ./main.cpp .


RUN g++ main.cpp -o main

CMD ["./main"]
