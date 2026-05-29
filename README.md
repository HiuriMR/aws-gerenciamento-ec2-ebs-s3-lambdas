# 🚀 Desafio DIO - Bootcamp GFT Fundamentos de Cloud com AWS 
## Primeiro Módulo - Gerenciamento de Instâncias EC2 na AWS
Este repositório foi criado como parte do **Desafio da DIO** para consolidar conhecimentos em  **gerenciamento de instâncias EC2 na AWS**. Documenta práticas com EC2, EBS, RDS, S3, Lambda e DynamoDB, incluindo anotações, insights e diagramas. Serve como material de apoio para estudos e futuras implementações na nuve

---

## 📖 Entendendo o Desafio

Agora é a sua hora de brilhar e construir um perfil de destaque na DIO!  
Explore todos os conceitos abordados, aplique os conhecimentos adquiridos nas aulas e documente sua experiência para demonstrar sua compreensão dos temas discutidos.

---

## 🎯 Objetivos de Aprendizagem

Ao concluir este desafio, você será capaz de:

- Aplicar os conceitos aprendidos em um ambiente prático.  
- Documentar processos técnicos de forma clara e estruturada.  
- Utilizar o GitHub como ferramenta para compartilhamento de documentação técnica.  

---

## 📦 Entrega do Desafio

Para concluir este desafio, você deverá:

1. Assistir a todas as vídeo-aulas (não pule nenhuma etapa!).  
2. Criar um repositório público no GitHub contendo:  
   - Um arquivo **README.md** detalhado (este documento).  
   - Quaisquer arquivos adicionais relevantes para documentar sua experiência.  
   - Opcionalmente, capturas de tela organizadas em uma pasta `/images`.  
3. Enviar o link do repositório e uma breve descrição clicando no botão **“Entregar Projeto”** na plataforma da DIO.  

---

## 📚 Recursos Úteis

- [Documentação Oficial AWS - Gerenciando Instâncias EC2](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/concepts.html)

---

## 📝 Anotações e Insights

- **EC2** é a máquina virtual na nuvem da AWS.  
- **EBS** funciona como disco rígido/SSD conectado ao EC2.  
- **RDS** é o banco relacional para dados estruturados.  
- **S3 + Lambda + DynamoDB** permitem automação serverless para pós-processamento de arquivos.  

---

## 📊 Diagrama da Arquitetura

Fluxo representado no laboratório:  
**Actor → Web Application → EC2 + EBS + RDS → S3 → Lambda → DynamoDB**

---

# Arquitetura AWS: EC2 + EBS + RDS e S3 + Lambda + DynamoDB

Este projeto descreve uma arquitetura híbrida que combina **infraestrutura tradicional** (EC2, EBS, RDS) com **componentes serverless** (S3, Lambda, DynamoDB).  
O objetivo é mostrar como dados podem ser processados em uma aplicação hospedada em EC2 e, em seguida, enviados para o S3, onde funções Lambda automatizam o processamento e armazenam resultados no DynamoDB.

---

## 🔗 Fluxo de Dados

### 1. Usuário acessa a aplicação
- O **Actor** representa o usuário que interage com a **Web Application**.
- A aplicação roda em uma instância **EC2**.

### 2. EC2 com EBS e RDS
- O **EC2** utiliza volumes **EBS** como discos rígidos para armazenar arquivos e dados temporários.
- O **RDS** é usado como banco de dados relacional para dados estruturados (ex.: usuários, pedidos).

### 3. Transferência de arquivos para o S3
- Arquivos gerados ou manipulados pelo EC2 são enviados para o **S3** usando o **AWS CLI** ou SDK.
- Exemplo de comando:
  ```bash
  aws s3 cp /mnt/ebs/arquivo.txt s3://meu-bucket/


## ✅ Conclusão

Este desafio consolida os conceitos de **infraestrutura tradicional (EC2, EBS, RDS)** e **serverless (S3, Lambda, DynamoDB)**, mostrando como integrar diferentes serviços da AWS em uma arquitetura prática e escalável.
