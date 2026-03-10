# Projeto 02 - Criando uma VPC e implementando um Servidor Web com Acesso SSH
 
#### OBJETIVO
Compreender na prática como funciona a comunicação entre recursos dentro de uma VPC, além de aplicar regras de segurança e acesso remoto a uma instância EC2.

#### SERVIÇOS UTLIZADOS
* Amazon VPC
* Amazon EC2
* Internet Gateway
* NAT Gateway
* Security Groups
* PuTTY
* Apache HTTP Server

#### IMPLEMENTAÇÃO
1. Criação de uma VPC personalizada para isolar a infraestrutura.
2. Configuração de subnets públicas para permitir acesso externo.
3. Criação e associação de um Internet Gateway para habilitar conectividade com a internet.
4. Configuração de um NAT Gateway para permitir saída de recursos privados.
5. Definição de tabelas de rotas para direcionar o tráfego da rede.
6. Criação de Security Groups controlando acesso HTTP e SSH.
7. Lançamento de uma instância EC2 dentro da VPC criada.
8. Configuração de acesso SSH utilizando chave .ppk via PuTTY.
9. Implantação de uma aplicação web acessível via navegador.

#### EVIDÊNCIA


#### SCRIPT
```bash
#!/bin/bash
#Install Apache Web Server and PHP
yum install -y httpd mysql php
#Download Lab files
wget https://aws-tc-largeobjects.s3.us-west-2.amazonaws.com/CUR-TF-100-RESTRT-1/267-lab-NF-build-vpc-web-server/s3/lab-app.zip
unzip lab-app.zip -d /var/www/html/
#Turn on web server
chkconfig httpd on
service httpd start
```

#### APRENDIZADO
_Este laboratório permitiu compreender como estruturar uma rede isolada dentro da AWS utilizando VPC, subnets e tabelas de roteamento. Também reforçou a importância dos Security Groups no controle de acesso e demonstrou o processo de acesso remoto seguro via SSH utilizando chave .ppk no PuTTY. Além disso, foi possível implantar uma aplicação web simples e validar o funcionamento do servidor por meio do navegador._
