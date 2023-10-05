# :cloud: Projeto-final-do-PB
AWS - Cloud Pratictioner - PB Aws - IF Fluminense - IFMT - UTFPR - UNAMA  | Programa de Bolsas - DevSecOps

#### Grupo 1:
- Bruno Garcia Nazareth 
- Nicolas Meirelles Grisostolo
- Raphael Antunes Marinho de Souza

### CASE:
Nós somos da empresa "Fast Engineering S/A" e gostaríamos de uma solução dos senhores(as), que fazem parte da empresa terceira "TI SOLUÇÕES INCRÍVEIS". Nosso eCommerce está crescendo e a solução atual não está atendendo mais a alta demanda de acessos e compras que estamos tendo. Desde o Início do ano os acessos e compras estão crescendo 20% a cada mês.

**Atualmente usamos:**
* 01 servidor para Banco de Dados Mysql;
* 01 servidor para a aplicação utilizando REACT;
* 01 servidor de web Server e que armazena estáticos como fotos e links.

**Nosso pedido é um ORÇAMENTO com:**
- ESCOPO;
- ARQUITETURA DA NOVA SOLUÇÃO;
- VALORES;
- PRAZO DE ENTREGA;
- CRONOGRAMA MACRO DE ENTREGAS;

Sobre a construção da arquitetura para o futuro website da nossa empresa, precisamos seguir as melhores práticas DevOps.

**O que é requerido na atividade:**
- Ambiente Kubernetes;
- Banco de dados PaaS;
- MultiAZ;
- Segurança de backup de dados;
- Persistência dos dados;
- Balanceamento de carga com healthcheck;
- Segurança (liberar somente o necessário/mínimo acesso possível).
  
Objetivo: Monte a proposta e a arquitetura do que o grupo propõe entregar.

___

## Projeto de Migração para a AWS - Fast Engineering S/A

## Introdução

Este repositório contém a documentação e o escopo do projeto de migração para a AWS de um e-commerce. O projeto tem como objetivo aumentar a escalabilidade e reduzir custos operacionais.

## Motivação do Cliente

Nossa motivação para esta migração é atender a alta demanda de acessos e compras que a Fast Engineering S/A vem tendo.

## Escopo do Projeto

### O escopo do projeto inclui as seguintes etapas:

### 1. ![Emoji-onpremise](https://github.com/RaphaelAntunesMarinhoDeSouza/Images/blob/main/Projeto%20Final/logoon.png) Avaliação da Infraestrutura Atual:

 <div align="center">
  <img src="https://github.com/RaphaelAntunesMarinhoDeSouza/Images/blob/main/Projeto%20Final/Atual.png" width="400px">
   <p><em>Arquitetura Atual</em></p>
</div>

### 2. ![Emoji-AWS](https://github.com/RaphaelAntunesMarinhoDeSouza/Images/blob/main/Projeto%20Final/awslogo.png) Arquitetura da Solução Proposta:

A arquitetura proposta segue as melhores práticas e está de acordo com os pilares da AWS Well-Architected Framework.
    
  **2.1. ![Emoji-pilar](https://github.com/RaphaelAntunesMarinhoDeSouza/Images/blob/main/Projeto%20Final/new.png) Pilares da AWS Well-Architected Framework**
      
  <div align="center">
    <img src="https://github.com/RaphaelAntunesMarinhoDeSouza/Images/blob/main/Projeto%20Final/5697.1673071669.svg" width="450px">
  </div>
  
  **2.2. Migração de Dados:**
  
  Estamos implementando uma migração de banco de dados crucial para o AWS RDS e escolhemos uma abordagem que prioriza a eficiência e a continuidade operacional. Utilizaremos o AWS Database Migration Service (DMS) para assegurar uma transição suave, replicando os dados de forma contínua e mantendo sua integridade. Essa estratégia minimizará qualquer impacto nas operações diárias enquanto aproveitamos os benefícios da escalabilidade e segurança da AWS. Estamos comprometidos em garantir que essa migração seja uma transição tranquila e bem-sucedida.
  
  **2.3. Serviços Utilizados**
  
  - **Amazon EC2:**
    - Amazon EC2 fornece instâncias virtuais sob demanda com configuração personalizável para uma ampla variedade de cargas de trabalho.
    - Escalabilidade sob demanda, permitindo a adaptação rápida às necessidades de computação, sem investimentos antecipados em hardware físico.
  
  - **Amazon CloudFront:**
    - Amazon CloudFront é um serviço de entrega de conteúdo que garante a distribuição eficiente e rápida de conteúdo estático, como imagens e arquivos.
    - Oferece distribuição global eficiente e veloz de conteúdo estático, atendendo à demanda em constante crescimento.
  
  - **AWS WAF:**
    - AWS Web Application Firewall é um serviço de firewall projetado para proteger aplicações web contra ataques comuns.
    - Proporciona proteção avançada contra ameaças, garantindo a segurança de aplicativos da web.
  
  - **Amazon Route 53:**
    - Amazon Route 53 é um serviço DNS que permite registrar e gerenciar domínios, com roteamento de tráfego para recursos AWS, como ELB e CloudFront.
    - Facilita o roteamento de tráfego eficiente e garante alta disponibilidade, direcionando acessos para instâncias e serviços AWS.
  
  - **Amazon S3:**
    - Amazon S3 utiliza Buckets para armazenar e distribuir conteúdo estático, incluindo imagens, vídeos e arquivos, integrando-se ao CloudFront para uma entrega eficiente.
    - Oferece armazenamento seguro e escalável para imagens, vídeos e arquivos.
  
  - **AWS IAM:**
    - AWS Identity and Access Management é fundamental para garantir a segurança e o controle de acesso aos recursos da AWS.
    - Fornece gerenciamento granular de permissões, assegurando que apenas o acesso autorizado seja concedido a recursos críticos.
  
  - **Amazon EKS:**
    - Elastic Kubernetes Service atua como a base da arquitetura, oferecendo orquestração de contêineres por meio do Kubernetes.
    - Proporciona orquestração de contêineres escalável, permitindo a expansão dinâmica e alta disponibilidade da aplicação.
  
  - **VPC:**
    - Virtual Private Cloud isola a infraestrutura na nuvem e fornece controle granular sobre a rede, criando uma rede privada virtual.
    - Cria uma rede VPC, melhorando o controle de tráfego e a segurança da infraestrutura.
  
  - **NACL:**
    - Network Access Control List é uma lista com camadas adicionais de segurança que controlam o tráfego de entrada e saída em sub-redes da VPC.
    - Utiliza NACLs para definir regras de tráfego, reforçando a segurança e o controle na comunicação entre os componentes da aplicação.
  
  - **Amazon RDS:**
    - Relational Database Service hospeda o banco de dados MySQL, oferecendo alta disponibilidade, escalabilidade e backup automático dos dados.
    - Disponibiliza um banco de dados gerenciado com alta disponibilidade, escalabilidade e backup automático.
  
  - **Elastic Load Balancing:**
    - ELB distribui o tráfego entre instâncias do EKS, garantindo um balanceamento de carga eficiente e alta disponibilidade.
    - Realiza o balanceamento de carga entre as instâncias, melhorando a disponibilidade e a eficiência da plataforma de comércio eletrônico.
  
  - **Amazon CloudWatch:**
    - CloudWatch oferece monitoramento e observabilidade para os recursos da aplicação, utilizando métricas e alarmes para monitorar o desempenho dos componentes.
    - Fornece monitoramento detalhado e alertas em tempo real para identificar e resolver problemas rapidamente.
  
  - **AWS DMS:**
    - AWS Database Migration Service é usado para migrar dados do banco de dados MySQL existente para o RDS.
    - Facilita uma migração suave e consistente dos dados para o RDS, minimizando o tempo de inatividade.
  
  - **AWS CloudFormation:**
    - Amazon CloudFormation permite criar e gerenciar infraestrutura como código, automatizando a definição e provisionamento de recursos.
    - Oferece automação e rastreabilidade na criação e atualização de recursos de infraestrutura.   
 
  **2.4. Nova Arquitetura**
  
<div align="center">
  <img src="https://github.com/RaphaelAntunesMarinhoDeSouza/Images/blob/main/Projeto%20Final/Expedia%20Global%20Deals%20Engine%20Architecture2.png" width="600px">
</div>

### 3. Valores

**Link da Calculadora AWS:** https://calculator.aws/#/estimate?id=1243cf457c970e2ca78ce89e69bfbc2ef23b6eb0

### 4. Prazo de Entrega:

### 5. Cronograma Macro de Entregas:
