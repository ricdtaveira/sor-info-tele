
# Criação e Manutenção das Imagens

A criação de uma imagem no Docker pode ser feita das seguintes formas: 
1) Criação de uma imagem a partir de um Dockerfile
2) Criação de uma imagem a partir de uma imagem base.   

  
## Criação de uma Imagem a partir do Dockerfile

Etapas da instalação:
1) Instalar o pacote  Docker a partir de um script de instalação baixado do site do Docker. Adiciona na maquina local um repositório Docker e inicia a instalação do Docker.
2) Inicializar a execução do Docker 
3) Verificar se o Docker está executando com o comando ps
4) Verificar os containers que estão executando localmente.


```bash 
  curl -sSL https://get.docker.com | sh 
  /etc/init.d/docker start
  ps -ef | grep docker
  docker ps
```

  
## Criação de uma imagem a partir de uma imagem base

Instalar o Docker usando o snap.
1) Executar o comando de install no snap
2) Executar 

```bash 
  sudo snap install docker
  sudo docker info
  sudo docker run hello-world
  sudo docker images
```
