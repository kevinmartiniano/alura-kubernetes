# alura-kubernetes

## 1 - Criação do ambiente
####  Realizar o build dos dockers e subir a imagem do docker da aplicação 
####  no dockerhub.io
#### 
## 2 - Subir os dockers
####  docker-compose up -d
#### 
## 3 - Entrar no docker do database
####  docker exec -it [nome do container com o banco de dados] bash
#### 
## 4 - Acessar o client do database
####  mysql -u root -p
#### 
## 5 - Executar as queryes à seguir
####  use loja
####  create table produtos (id integer auto_increment primary key, nome varchar(255), preco decimal(10,2));
####  alter table produtos add column usado boolean default false;
####  alter table produtos add column descricao varchar(255);
####  create table categorias (id integer auto_increment primary key, nome varchar(255));
####  insert into categorias (nome) values ("Futebol"), ("Volei"), ("Tenis");
####  alter table produtos add column categoria_id integer;
####  update produtos set categoria_id = 1;
#### 
## 6 - Instalar Minikube
####  sudo apt-get install google-cloud-sdk-minikube
#### 
## 7 - Instalar kubectl
####  sudo apt-get install kubectl
#### 
## 8 - Criar o arquivo yaml do kubernets
#### 
## 9 - Temos alguns exemplos de arquivos yaml na pasta kubernets
#### 
## 10 - Pod
####  Menor objeto do kubernets, normalmente sobe apenas um docker.
#### 
## 11 - Deployment
####  Um objeto que normalmente contém mais de uma réplica de Pod e é 
####  utilizado para escalonar a aplicação, acompanha o estado dos Pods, 
####  cria mais réplicas caso você indique que isso precisa ser feito e 
####  caso um Pod esteja fora do estado esperado, derruba e sobe outro no 
####  lugar.
## 12 - Service
####  Atuação parecida com um balanceador de cargas, você configura o selector 
####  com o nome igual ao do selector do Deployment e ele fica "orquestrando" 
####  qual dos pods será acessado. (Provisiona uma url).
#### 
## 13 - Anotações comandos minikube
####  minikube status (verificar status)
####  minikube start (iniciar minikube)
####  minikube stop (parar minikube)
####  minikube dashboard (painel do minikube)
####  minikube service "nome do service" --url (verificar a url do serviço)
#### 
## 14 - Anotações comandos kubectl
####  kubectl create -f file.yaml
####  kubectl get pods
####  kubectl delete pods aplicacao
####  kubectl config use-context minikube
####  kubectl describe pods
####  kubectl describe pods | grep IP (mostra apenas a linha que contém o endereço IP).
