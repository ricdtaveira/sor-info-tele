
# Instalação do Docker

A instalação do Docker pode Docker é uma ferramenta para criar e manter containers. Um container armazena serviços de forma isolada do SO host, como: servidor web, gerenciador de banco de dados, aplicação, servidor de mensagens etc. O LXC (LinuX Containers) implementa containers no sistema operacional Linux.  

O LXC funciona como uma virtualização bastante leve comparada às implementações de máquinas virtuais como Virtual Box, VMWARE e outras. O LXC não faz uso de emulação ou suporte a hardware, apenas proporciona a execução de vários sistemas Linux de forma isolada – daí vem a palavra container.

   
## Instalação 1

Etapas da instalação:
1) Instalar o pacote  Docker a partir de um script de instalação baixado do site do Docker. Adiciona na maquina local um repositório Docker e inicia a instalação do Docker.
2) Inicializar a execução do Docker 
3) Verificar se o Docker está executando com o comando ps
4) Verificar os containers que estão executando localmente


```bash 
  curl -sSL https://get.docker.com | sh 
  /etc/init.d/docker start
  ps -ef | grep docker
  docker ps
```

  
## Instalação 2

Instalar o Docker usando o sanp

```bash 
  npm install my-project
  cd my-project
```

    
## Instalação 2

Instalar o Docker em um SO Linux

```bash 
  npm install my-project
  cd my-project
```