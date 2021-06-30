
# Instalação do Docker

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
1) Chamar o sudo 
2) Informar a senha do usuário
3) Testar a instalação com o comando docker info
4) Chamar a execução do container hello-world
5) Verificar novamente o ambiente do docker com o comando docker info
6) Mostar as imagens depositadas no repositório com o comando docker images.

```bash 
  sudo snap install docker
  sudo docker info
  sudo docker hello-world
  sudo docker info
```

    
## Configurar o acesso do Docker sem o uso do sudo 

Instalar o Docker usando o snap.
1) Verificar os grupso cadastrados no Linux 
2) Informar a senha do usuário
3) Testar a instalação com o comando docker info
4) Chamar a execução do container hello-world
5) Verificar novamente o ambiente do docker com o comando docker info
6) Mostar as imagens depositadas no repositório com o comando docker images.

```bash 
  cat /etc/groups | docker
  sudo docker info
  sudo docker hello-world
  sudo docker info
```