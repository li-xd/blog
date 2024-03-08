---
share: true
title: 本地运行 AI
---


#完成 

![[43.7k star! 轻松在本地运行Llama2、Gemma等多种大模型，无需GPU！ (2024_3_8 上午10_54_45).html|43.7k star! 轻松在本地运行Llama2、Gemma等多种大模型，无需GPU！ (2024_3_8 上午10_54_45).html]]
[微信地址](https://mp.weixin.qq.com/s/CqtvMA5jjJivudcHyd2Mag)


- [x] 安装调研 ➕ 2024-03-08 🛫 2024-03-08 📅 2024-03-08 ✅ 2024-03-08

安装地址为 10.10.101.104 「/home/cg/docker/ollama」
##### DOCKER FILE 准备

```yaml
version: "2"
services:
    ollama:
      image: ollama/ollama
      container_name: ollama
      volumes:
        - ./volumes/ollama:/root/.ollama
      environment:
        TZ: Asia/Shanghai
      restart: always
      ports:
        - "11434:11434"
```


[GITHUB 地址](https://hub.docker.com/r/ollama/ollama)
![[ollama_ollama - Docker Image _ Docker Hub (2024_3_8 上午11_05_58).html|ollama_ollama - Docker Image _ Docker Hub (2024_3_8 上午11_05_58).html]]

```shell
# 执行命令

docker exec -ti ollama ollama run llama2
```

