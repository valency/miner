FROM nvidia/cuda:12.2.0-devel-ubuntu22.04

RUN sed -i -e 's/\(archive\|security\).ubuntu.com/mirrors.aliyun.com/g' /etc/apt/sources.list
ENV TZ=Asia/Hong_Kong
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

RUN apt-get update
RUN apt-get -y upgrade
RUN apt-get install -y sudo
RUN echo '%sudo ALL=(ALL) NOPASSWD:ALL' >> /etc/sudoers

COPY aleo_prover .
CMD ["sh", "-c", "echo ${ACCOUNT_ID} && echo cephalon_${GPU_TYPE}_$(hostname) && ./aleo_prover --tcp_server mainnet.aleopool.io:20003 --miner_account ${ACCOUNT_ID} --worker cephalon_${GPU_TYPE}_$(hostname)"]

