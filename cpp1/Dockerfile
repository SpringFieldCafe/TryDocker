FROM ubuntu AS builder

ENV DEBIAN_FRONTEND=noninteractive

RUN apt update


RUN apt install -y build-essential

WORKDIR /usr/src/cpp

COPY main.cpp .

RUN g++ main.cpp -o main

FROM ubuntu

COPY --from=builder /usr/src/cpp/main .

CMD ["./main"]