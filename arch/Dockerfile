FROM alpine AS builder

ENV DEBIAN_FRONTEND=noninteractive

RUN apk add --no-cache g++

WORKDIR /usr/src/cpp

COPY main.cpp .

RUN g++ main.cpp -o main 

FROM archlinux:latest

COPY --from=builder /usr/src/cpp/main .

CMD ["./main"]