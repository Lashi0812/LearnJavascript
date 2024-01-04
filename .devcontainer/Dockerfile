FROM ubuntu
ARG DEBIAN_FRONTEND=noninteractive
RUN --mount=type=cache,target=/var/cache/apt \
    apt-get update && \
    apt-get install -y  build-essential \
                    git \
                    ca-certificates \
                    curl \
                    unzip
RUN curl -fsSL https://deno.land/x/install/install.sh | sh
RUN apt-get install -y python3-pip
RUN pip3 install jupyterlab
ENV DENO_INSTALL="/root/.deno"
ENV PATH="$DENO_INSTALL/bin:$PATH"
RUN deno jupyter --unstable --install
