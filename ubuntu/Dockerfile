
FROM ubuntu:22.04

RUN apt update

ENV DEBIAN_FRONTEND=noninteractive

RUN apt install -y build-essential

RUN echo "#include<iostream>">main.cpp
RUN echo "int main()">>main.cpp
RUN echo "{std::cout<<\"hello world\"<<std::endl;">>main.cpp
RUN echo "return 0;}">>main.cpp


RUN g++ main.cpp -o main

CMD ["./main"]


