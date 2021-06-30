
# Criação e Manutenção das Imagens

A instalação do Docker será apresentada abaixo com dois formatos.   

  
## Instalação 1

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

  
## Instalação 2

Instalar o Docker usando o snap.
1) Executar o comando de install no snap
2) Executar 

```bash 
  sudo snap install docker
  sudo docker info
  sudo docker run hello-world
  sudo docker images
```

    
## Instalação 2

Instalar o Docker em um SO Linux

```bash 
  npm install my-project
  cd my-project
```