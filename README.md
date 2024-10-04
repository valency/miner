# Docker Miners

Miners with one click to run.

```bash
docker run -d --restart=always --gpus '"device=all"' --name dynex uiewy/dynex:1.2.8
docker run -d --restart=always --gpus '"device=all"' --name ironfish uiewy/ironfish:19.2.1
docker run -d --restart=always --gpus '"device=all"' --name qubic uiewy/qubic:1.8.7
docker run -d --restart=always --gpus '"device=all"' -e ACCOUNT_ID=bf90200407d64180 -e GPU_TYPE=3060x2 --name aleo uiewy/aleo:1.0.7
```

