FROM nvidia/cuda:12.2.0-devel-ubuntu20.04

ENV DOTNET_SYSTEM_GLOBALIZATION_INVARIANT=1

RUN apt-get update
RUN apt-get install -y wget unzip

RUN wget https://unicorn.org.cn/reactor/data/qli-client-1.8.7.1-linux-x64.zip
RUN unzip qli-client-1.8.7.1-linux-x64.zip

WORKDIR qliclient
RUN chmod a+x qli-Client
CMD ./qli-Client 

