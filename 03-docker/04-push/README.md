
# Fazer Push de uma Imagem para o Docker Hub
Após o `commit` das alterações em uma imagem no repositório local é prudente fazer uma cópia dessa
imagem para um serviço na nuvem onde se preserva todo o trabalho na configuração dessa imagem.
O Docker Hub permite a criação de repositórios públicos e/ou privados que hospedam imagens que poderão ser usadas posteriormente.  
Os passos apresentados a seguir definem um ciclo envolvendo as operações necessárias a obtenção de uma imagem até o upload de uma versão modificada para o Docker Hub.

## 1) Criar um repositório no Docker Hub 

A criação de uma conta no Docker Hub antecede a criação de um repositório para que se possa fazer o `push` de uma imagem alterada. Portanto, é necessário proceder da seguinte forma: 

1.1) Acessar o site do Docker Hub. [Docker Hub](https://hub.docker.com/);

1.2) Criar uma conta no Docker Hub. [Criar Conta](https://hub.docker.com/signup);

1.3) Criar um repositório no Docker Hub;

1.4) Fazer o `push` de imagens obedecendo a seguinte nomenclatura: `<conta>/<repositorio>:tag`.    

## 2) Fazer um Pull de uma imagem hospedada no GitHub ou criar uma imagem usando o Dockerfile

Antes de fazer uma alteração na imagem é necessário baixá-la do Docker Hub.

```bash 
  $ docker search ubuntu
  $ docker pull ricdtaveira/ubuntu:latest
  $ docker images
```

## 3) Alterar ou criar uma imagem no Repositório Local

A alteração de uma imagem se faz da seguinte forma:

### 3.1) Instanciar a imagem em um container 
   Chamar o comando `docker run` . A partir daí o prompt do root do container em execução estará pronto para receber comandos para executar a manutenção do container com posterior `commit` da imagem.

```bash 
  $ docker run -i -t ricdtaveira/ubuntu:latest 
  root@a7bc19c594aa:/#
```

### 3.2) Sair do ambiente de execução do container sem parar sua execução.
   Para sair do ambiente de execução de um container e voltar para o ambiente de execução do host onde o docker executa deve ser digitada a seguinte sequência de teclas `ctrl + p + q` no ambiente de execução do container.

```bash 
  root@a7bc19c594aa:/# <ctrl p q>
  $ 
```

### 3.3) Salvar as alterações da imagem com os dados do container em execução
   Observar os containers executando usando o comando `docker ps`.
   Salvar a imagem com as alterações configuradas no container com o comando `docker commit`.
   A imagem salva deve seguir um padrão de nomenclatura do Docker Hub: `user_id/repository_id:tag`.
   Verificar as imagens do repositório local com o comando `docker images`.

```bash 
  $ docker ps
  $ docker commit 8f904350bdcl ricdtaveira/ubuntu:1.0 
  $ docker images
```

### 3.4) Se for necessário alterar o container novamente ...
  Uma nova alteração no container será possível com uma nova entrada no ambiente de execução do container. Para entrar no ambiente de execução do container usar o comando `docker attach <container-id>`. Entrando no ambiente de execução do container seguir com as alterações e executar os passos 3.2 e 3.3 anteriormente descritos.

```bash 
  $ docker ps
  $ docker attach 8f904350bdcl  
  $ /# 
```

### 3.5) Criar imagem com Tag compatível com o repositório no Docker Hub

A partir da imagem alterada mudar o nome dessa imagem de forma a torná-la compatível com a nomenclatura do repositório em que ficará alocada no Docker Hub. A nomenclatura para o Docker Hub é `user_id/repository_id:tag`.

```bash 
  $ docker tag 8f904350bdcl ricdtaveira/ubuntu:latest 
  $ docker images
```
  
### 3.6) Upload da Imagem local para o repositório no Docker Hub

O upload da imagem alterada para o Docker Hub se faz da seguinte forma:  
a) Login no Docker Hub;

b) Execução do comando `push`; 

c) Verificação do repositório no Docker Hub.


```bash 
  $ docker login 
  $ docker push ricdtaveira/ubuntu:latest  
``` 