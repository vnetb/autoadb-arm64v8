### builder
FROM messense/rust-musl-cross:aarch64-musl-arm64 AS builder
ENV DEBIAN_FRONTEND=noninteractive

# RUN apt-get update && apt-get -y install --no-install-recommends \
#       apt-transport-https \
#       software-properties-common \
#       git gcc gcc-c++ tar cmake make \
#     && apt-get -y clean 

RUN git clone https://github.com/rom1v/autoadb.git
RUN cd autoadb/src && cargo build --release -vv

RUN cd autoadb && ls -l
RUN cd autoadb/src && ls -l
