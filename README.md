# 🎵 Projeto Aria.net: Arquitetura Serverless com S3 & Terraform

Este repositório documenta a implementação de uma solução de hosting de alta performance para o portal **Aria.net**, utilizando **Amazon S3** e **Terraform**. O foco principal foi a modernização de infraestrutura com foco em **eficiência financeira (FinOps)**.

---

## 🎯 O Desafio (Business Case)
O cliente Aria.net operava seu portal em instâncias **Amazon EC2** (t3.medium). Esta abordagem gerava custos fixos elevados e necessidade de manutenção constante.

**A Solução:** Migração para uma **Arquitetura Serverless** de Static Website Hosting, reduzindo o **TCO (Total Cost of Ownership)** em aproximadamente **98%**.

---

## 🛠️ Stack Tecnológica & Decisões Técnicas

| Ferramenta | Ícone | Justificativa Técnica |
| :--- | :---: | :--- |
| **Amazon S3** | <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/amazonwebservices/amazonwebservices-original-wordmark.svg" width="45"> | Hosting de objetos com durabilidade de 11 noves e custo-benefício imbatível. |
| **Terraform** | <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/terraform/terraform-original.svg" width="45"> | Provisionamento via IaC para garantir imutabilidade e evitar o "clique-ops". |

---

## 📸 Galeria de Engenharia (Case Study)

### 🔹 Fase 1: Planejamento e Init (IaC Workflow)
*Validação do plano de execução e integridade do código.*
![Terraform I](img/Terraform%20I.png)

---

### 🔹 Fase 2: Automação e Outputs
*Extração automatizada do endpoint público para entrega contínua.*
![Terraform IV](img/Terraform%20IV.png)

---

### 🔹 Fase 3: Segurança e Políticas de Bucket (Compliance)
*Implementação de Bucket Policies restritivas via Terraform (Least Privilege).*
![Terraform V](img/Terraform%20VI.png)

---

### 🔹 Fase 4: Validação Final (Portal Aria.net Live)
*O resultado: Infraestrutura moderna, segura e extremamente econômica.*
![Site Final](img/image_b791f0.png.png)

---

## 🏁 Conclusão
O projeto **Aria.net** prova que a simplicidade técnica, quando bem executada via automação, é o caminho mais curto para a eficiência operacional na Nuvem.

---
*Documentação desenvolvida por Gustavo Gomes | AWS Cloud Portfolio*
