# 🎵 Projeto Aria.net: Modernização e Cloud Cost Optimization (FinOps)

[![Terraform](https://img.shields.io/badge/Terraform-1.x-623CE4?logo=terraform)](https://www.terraform.io/)
[![AWS S3](https://img.shields.io/badge/AWS-S3_Serverless-FF9900?logo=amazonaws)](https://aws.amazon.com/s3/)
[![Status](https://img.shields.io/badge/Status-Concluído-success)](#)

## 📝 Visão Geral
O projeto **Aria.net** consistiu na migração estratégica de um portal web de uma arquitetura legada baseada em instâncias EC2 para uma solução **100% Serverless** utilizando **Static Website Hosting no Amazon S3**. 

O foco não foi apenas a migração, mas a implementação de **Infraestrutura como Código (IaC)** para garantir que o ambiente fosse escalável, seguro e totalmente documentado.

---

## 🏗️ Desafio de Negócio vs. Solução Técnica

**Cenário Anterior:** O cliente operava em instâncias EC2 gerenciadas manualmente (SSH), com custos fixos de computação, necessidade de patching de OS e riscos de downtime por falta de redundância.

**Arquitetura Implementada:**
* **Engine de Hosting:** Amazon S3 configurado para entrega de conteúdo estático.
* **Provisionamento:** Terraform com gerenciamento de estado (State Management).
* **Segurança:** Implementação de políticas de acesso restritivas (Bucket Policies) e bloqueio de acesso público indevido via código.

> **Resultado:** Redução de **98% no TCO (Total Cost of Ownership)** e eliminação completa da sobrecarga de gerenciamento de servidores.

---

## 🛠️ Stack Tecnológica & Decisões de Design

| Componente | Ferramenta | Decisão Técnica |
| :--- | :--- | :--- |
| **IaC** | **Terraform** | Escolhido para evitar o "Configuration Drift" e permitir rollbacks rápidos. |
| **Storage** | **Amazon S3** | Escolhido pela durabilidade de 99.999999999% (11 noves) e custo próximo a zero em ociosidade. |
| **Segurança** | **IAM & Bucket Policies** | Aplicação do princípio de **Least Privilege** para garantir que apenas o necessário fosse exposto. |

---

## 🚀 Ciclo de Vida do Projeto (Case Study)

### 1. Governança via Terraform (IaC)
Diferente de uma criação manual, utilizei o Terraform para definir o ciclo de vida do bucket, tags de organização e configurações de index/error documents.
![Planejamento IaC](img/Terraform%20I.png)
![Build do Código](img/Terraform%20IV.png)

### 2. Segurança e Compliance
A maior preocupação em buckets S3 é a segurança. Implementei via código a **Bucket Policy** necessária para o hosting, mantendo o controle granular sobre quem e o que pode ser acessado.
![Políticas de Segurança](img/Terraform%20V.png)
![Output de Endpoint](img/Terraform%20VI.png)

### 3. Entrega Final e Validação
O portal Aria.net agora reside em uma infraestrutura global, resiliente e de baixo custo, acessível através de um endpoint otimizado.
![Site Live](img/image_b791f0.png.png)

---

## 🧠 Lições Aprendidas e Troubleshooting

* **Gerenciamento de Erros:** Configuração de páginas de erro 404 personalizadas para melhorar a UX (User Experience).
* **IaC State:** Entendimento da importância do arquivo `.tfstate` para manter a consistência entre o código e o que realmente existe na AWS.
* **FinOps:** Demonstração prática de como uma mudança de arquitetura (EC2 -> S3) pode salvar centenas de dólares anuais para uma operação simples.

---

## 🎯 Conclusão e Mindset

Este projeto demonstra que a maturidade em Cloud não é sobre usar os serviços mais caros, mas sobre usar os **serviços certos para o problema certo**. A automação com Terraform garantiu que o Aria.net tenha agora uma infraestrutura resiliente, auditável e econômica.

---
**Autor:** [Gustavo Gomes](https://github.com/gustavogomes43) | *Cloud & DevOps Enthusiast*
