
# Fazer Push de uma Imagem para o Docker Hub
Após o commit de alterações em uma imagem no repositório local é prudente fazer uma cópia dessa
imagem para um serviço na nuvem onde se preserva todo o trabalho na configuração dessa imagem. O Docker Hub permite a criação de repositórios de públicos e/ou privados que hospedam imagens que poderão ser usadas posteriormente.  

## 1) Criar conta no Docker Hub 

A criação de uma imagem no Docker pode ser feita das seguintes formas: 
1) Criação de uma imagem a partir de um Dockerfile
2) Criação de uma imagem a partir de uma imagem base.   

## 2) Fazer um Pull de uma imagem hospedada no GitHub


## 3) Alterar a imagem no Repositório Local



## 4) Criar imagem com Tag compatível com o repositório no Docker Hub


  
## 5) Upload da Imagem local para o repositório no Docker Hub



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

  
 