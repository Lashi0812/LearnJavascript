FROM ubuntu
RUN --mount=type=cache,target=/var/cache/apt \
    apt update && \
    apt install -y  build-essential \
                    git \
                    ca-certificates 

