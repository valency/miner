FROM nvidia/cuda:12.2.0-devel-ubuntu22.04

RUN sed -i -e 's/\(archive\|security\).ubuntu.com/mirrors.aliyun.com/g' /etc/apt/sources.list
ENV TZ=Asia/Hong_Kong
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

RUN apt-get update
RUN apt-get -y upgrade
RUN apt-get install -y sudo
RUN echo '%sudo ALL=(ALL) NOPASSWD:ALL' >> /etc/sudoers

COPY aleo_prover .
CMD ["sh", "-c", "echo ${ACCOUNT_ID} && echo cephalon_${GPU_TYPE}_$(hostname) && ./aleo_prover --pool aleo.asia1.zk.work:10003 --pool aleo.hk.zk.work:10003 --pool aleo.jp.zk.work:10003 --address ${ACCOUNT_ID} --custom_name cephalon_${GPU_TYPE}_$(hostname)"]

