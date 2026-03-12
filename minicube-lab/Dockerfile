FROM arm64v8/ubuntu:22.04

RUN apt-get update && apt-get install -y \
    curl \
    conntrack \
    docker.io \
    sudo \
    ca-certificates

RUN curl -LO "https://dl.k8s.io/release/v1.29.0/bin/linux/arm64/kubectl" \
    && install -o root -g root -m 0755 kubectl /usr/local/bin/kubectl \
    && rm kubectl

RUN curl -LO "https://storage.googleapis.com/minikube/releases/latest/minikube-linux-arm64" \
    && install minikube-linux-arm64 /usr/local/bin/minikube \
    && rm minikube-linux-arm64

CMD ["/bin/bash"]

