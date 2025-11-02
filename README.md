# ☁️ Desafio AWS — EC2, EBS, S3 e Lambda Foundations  

## 🎯 Objetivo do Desafio
Consolidar os conhecimentos adquiridos nas aulas práticas da **Formação AWS Cloud Foundations (DIO)**, aplicando conceitos de gerenciamento de instâncias EC2 e integração com os serviços **EBS**, **S3** e **Lambda Foundations**.  

Este repositório reúne o material prático e o diagrama da arquitetura desenvolvida, servindo como apoio para estudos futuros e para comprovar domínio dos serviços básicos de computação na nuvem AWS.

---

## 🧠 Conceitos Aplicados
- **Amazon EC2 (Elastic Compute Cloud):** instâncias virtuais para execução de aplicações.  
- **Amazon EBS (Elastic Block Store):** volume de armazenamento persistente anexado à EC2.  
- **Amazon S3 (Simple Storage Service):** armazenamento de objetos usado para backups, logs e AMIs.  
- **AWS Lambda Foundations:** automação serverless para criação de snapshots e backups.  

---

## 🧩 Arquitetura Desenvolvida

### 💬 Descrição
A arquitetura foi criada para representar um ambiente completo de **automação de backup e gerenciamento de instâncias EC2** na AWS:

1. O **usuário** acessa a instância **EC2** por navegador ou SSH.  
2. A **EC2** gera dados e logs, armazenando-os em um **volume EBS**.  
3. O **Lambda Foundations** é responsável por automatizar a **criação de snapshots** e **backups**.  
4. Os artefatos são enviados ao **S3**, que também pode disparar eventos **(triggers)** para novas execuções da função Lambda.  

---

## 🖼️ Diagrama da Arquitetura

![Arquitetura AWS – EC2, EBS, Lambda Foundations e S3](images/Desafio%20AWS%20Instâncias%20EC2.drawio.png)

> **Figura:** Representação visual da integração entre EC2, EBS, Lambda Foundations e S3 no ambiente AWS Cloud.

---

## ⚙️ Etapas do Laboratório

### 1️⃣ Criação da Instância EC2
- Tipo: `t3.micro` (free tier elegível).  
- Sistema Operacional: **Amazon Linux 2023**.  
- Configurações:
  - Criação de **key pair (.pem)**.  
  - Grupo de segurança liberando portas 22 (SSH) e 80 (HTTP).  
  - Associação de **volume EBS (10 GB)**.

### 2️⃣ Anexar e montar o EBS
```bash
lsblk
sudo mkfs -t xfs /dev/xvdf
sudo mkdir /dados
sudo mount /dev/xvdf /dados
