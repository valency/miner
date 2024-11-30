# Docker Miners

Miners with one click to run.

```bash
docker run -d --restart=always --gpus '"device=all"' --name dynex uiewy/dynex:1.2.8
docker run -d --restart=always --gpus '"device=all"' --name ironfish uiewy/ironfish:19.2.1
docker run -d --restart=always --gpus '"device=all"' --name qubic uiewy/qubic:3.1.1
docker run -d --restart=always --gpus '"device=all"' -e ACCOUNT_ID=aleo17ncsh2emp39srjtuwaxkhcv2xhye95wqr559s4yxp2avvsxahuzqn4xt7k -e GPU_TYPE=3060x2 --name aleo uiewy/aleo:0.2.4
```

