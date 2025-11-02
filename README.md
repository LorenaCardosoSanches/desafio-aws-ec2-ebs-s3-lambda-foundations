# ☁️ Desafio AWS — EC2, EBS, S3 e Lambda Foundations  

## 🎯 Objetivo do Desafio
Este projeto foi desenvolvido como parte da formação **AWS Cloud Foundations (DIO)**.  
O objetivo é consolidar os conhecimentos sobre **gerenciamento de instâncias EC2** e a integração entre os serviços **EBS**, **S3** e **Lambda Foundations** da AWS.

O repositório documenta, de forma clara e estruturada, todo o processo prático realizado durante o laboratório.

---

## 🧠 Conceitos Aprendidos
- **Amazon EC2 (Elastic Compute Cloud):** serviço de computação que permite criar e gerenciar instâncias virtuais.  
- **Amazon EBS (Elastic Block Store):** fornece armazenamento em blocos persistente para instâncias EC2.  
- **Amazon S3 (Simple Storage Service):** armazena objetos, snapshots, AMIs e logs de backup.  
- **AWS Lambda Foundations:** executa funções automatizadas, como criação de snapshots e backup de dados, sem necessidade de servidores.

---

## 🧩 Arquitetura Implementada

### 💬 Descrição
A arquitetura representa um ambiente automatizado de **backup e gerenciamento de instâncias EC2**:

1. O **usuário** acessa a instância **EC2** (via navegador ou SSH).  
2. A **EC2** gera dados e logs, armazenando-os em um volume **EBS**.  
3. A função **Lambda Foundations** cria **snapshots e AMIs** automaticamente.  
4. Esses arquivos são enviados e armazenados no **S3**, que também aciona eventos *triggers* para novas execuções do Lambda.  

---

## 🖼️ Diagrama da Arquitetura

![Arquitetura AWS – EC2, EBS, Lambda Foundations e S3](images/Desafio%20AWS%20Instâncias%20EC2.drawio.png)

> **Figura:** Arquitetura do ambiente AWS integrando EC2, EBS, S3 e Lambda Foundations.

---

## 💡 Insights e Aprendizados
- A automação com **Lambda Foundations** reduz falhas humanas e otimiza o tempo de administração.  
- **Snapshots** e **AMIs** garantem a restauração rápida do ambiente em caso de falhas.  
- O uso do **S3** com políticas de ciclo de vida auxilia na economia de custos e armazenamento seguro.  
- Documentar e visualizar a arquitetura facilita o entendimento e futuras implementações.  

---

## 🗂️ Estrutura do Repositório
```
desafio-aws-ec2-ebs-s3-lambda-foundations/
│
├── README.md
└── images/
└── Desafio AWS Instâncias EC2.drawio.png
```

---

## 📚 Referências
- [Documentação Amazon EC2](https://docs.aws.amazon.com/pt_br/AWSEC2/latest/UserGuide/concepts.html)  
- [Documentação Amazon S3](https://docs.aws.amazon.com/pt_br/AmazonS3/latest/userguide/Welcome.html)  
- [Documentação AWS Lambda](https://docs.aws.amazon.com/lambda/latest/dg/welcome.html)  
- [Guia AWS Cloud Foundations (DIO)](https://www.dio.me/)

---

## 👩‍💻 Autora
**Lorena Cardoso Sanches**  
Desenvolvedora e entusiasta de Cloud Computing ☁️  
📍 São Bernardo do Campo/SP  
🔗 [linkedin.com/in/lorenacardososanches](https://linkedin.com/in/lorenacardososanches)
