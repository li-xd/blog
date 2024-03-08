---  
share: true  
title: 本地运行 AI  
tags:  
  - 完成  
---  
  
  
#完成   
  
![43.7k star! 轻松在本地运行Llama2、Gemma等多种大模型，无需GPU！ (2024_3_8 上午10_54_45).html](./%E7%94%9F%E6%B4%BB/%E9%99%84%E4%BB%B6/43.7k%20star!%20%E8%BD%BB%E6%9D%BE%E5%9C%A8%E6%9C%AC%E5%9C%B0%E8%BF%90%E8%A1%8CLlama2%E3%80%81Gemma%E7%AD%89%E5%A4%9A%E7%A7%8D%E5%A4%A7%E6%A8%A1%E5%9E%8B%EF%BC%8C%E6%97%A0%E9%9C%80GPU%EF%BC%81%20(2024_3_8%20%E4%B8%8A%E5%8D%8810_54_45).html.md)  
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
![ollama_ollama - Docker Image _ Docker Hub (2024_3_8 上午11_05_58).html](./%E7%94%9F%E6%B4%BB/%E9%99%84%E4%BB%B6/ollama_ollama%20-%20Docker%20Image%20_%20Docker%20Hub%20(2024_3_8%20%E4%B8%8A%E5%8D%8811_05_58).html.md)  
  
```shell  
# 执行命令  
  
docker exec -ti ollama ollama run llama2  
```  
  
