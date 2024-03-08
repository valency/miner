FROM nvidia/cuda:12.2.0-devel-ubuntu20.04

RUN apt-get update
RUN apt-get install -y wget

RUN wget https://unicorn.org.cn/reactor/data/onezerominer-linux-1.2.8.tar.gz
RUN tar -zxvf onezerominer-linux-1.2.8.tar.gz

CMD /onezerominer-linux/onezerominer -a dynex -o hk.dnx.minenow.space:18000 -w XwnC2hupf2CaFBqkTjaeuZ7XPo8npJakfZhJBhbSV52ZFUaQKVRw2rkTDgnM4X3qjsZrgfgojbnGEZRVepMAQYce28bbvWbNv -p `hostname`

