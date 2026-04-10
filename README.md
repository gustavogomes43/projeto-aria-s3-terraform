# 🎵 Projeto Aria.net: Hosting Serverless com S3 & Terraform

Este repositório documenta a implementação de uma infraestrutura de hospedagem estática utilizando **Amazon S3**, totalmente automatizada via **Terraform**. O foco aqui é performance global e custo próximo de zero.

---

## 🎯 Finalidade e Solução
**A Dor do Cliente:** Necessidade de hospedar um portal institucional com alta demanda de acesso, mas sem orçamento para gerenciar servidores (EC2) ou custos de licenciamento.
**A Solução:** Arquitetura **Serverless** utilizando Static Website Hosting. A infraestrutura é escalável por definição e elimina a manutenção de SO.

---

## 🛠️ Stack Tecnológica & Escolhas Técnicas

| Ícone | Ferramenta | Justificativa |
| :---: | :--- | :--- |
| <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/amazonwebservices/amazonwebservices-original-wordmark.svg" width="35"> | **Amazon S3** | Durabilidade de 99.999999999% e custo-benefício imbatível. |
| <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/terraform/terraform-original.svg" width="35"> | **Terraform** | Garante que as permissões de acesso sejam aplicadas de forma idêntica via IaC. |

---

## 📸 Galeria de Implementação (Estudo de Caso)

### Fase 1: Planejamento e Init
![Terraform Plan](img/Terraform%20I.png)
*Execução do plano garantindo que apenas os recursos necessários serão criados.*

### Fase 2: Configuração de Variáveis e Outputs
![Terraform Outputs](img/Terraform%20IV.png)
*Exposição automática do Endpoint do site após o deploy.*

### Fase 3: Segurança e Políticas de Bucket
![Bucket Policy](img/Terraform%20V.png)
*Implementação de políticas de acesso restrito e controle de Public Access Blocks.*

### Fase 4: Validação Final
![Site Online](img/image_b791f0.png.png)
*O resultado final: Site hospedado com baixa latência e 100% funcional.*

---

## 📈 Benefícios e Resultados
* **Redução de Custos:** Economia de ~98% comparado a instâncias EC2.
* **Manutenção Zero:** Foco 100% no conteúdo, zero preocupação com patches.

---
*Este projeto demonstra o poder do Serverless para otimização de custos e performance.*
