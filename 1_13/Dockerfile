FROM ubuntu:26.04
EXPOSE 8080
WORKDIR /usr/src/app
COPY . .
RUN apt-get update && apt-get install -y wget tar && \
    wget https://go.dev/dl/go1.16.15.linux-amd64.tar.gz && \
    rm -rf /usr/local/go && \
    tar -C /usr/local -xzf go1.16.15.linux-amd64.tar.gz
ENV PATH=$PATH:/usr/local/go/bin
RUN go build
CMD ["./server"]