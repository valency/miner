FROM nvidia/cuda:12.2.0-devel-ubuntu20.04

ENV DOTNET_SYSTEM_GLOBALIZATION_INVARIANT=1

RUN apt-get update
RUN apt-get install -y wget p7zip-full

RUN wget https://unicorn.org.cn/reactor/data/qli-Client-3.1.1-Linux-x64.7z
RUN 7z x qli-Client-3.1.1-Linux-x64.7z -oqliclient

WORKDIR qliclient
RUN chmod a+x qli-Client
CMD ./qli-Client 

