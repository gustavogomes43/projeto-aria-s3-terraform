# 🎵 Projeto Aria.net: Arquitetura Serverless com S3 & Terraform

Este repositório documenta a implementação de uma solução de hosting de alta performance para o portal **Aria.net**, utilizando **Amazon S3** e **Terraform**. O foco principal foi a modernização de infraestrutura com foco em **eficiência financeira (FinOps)**.

---

## 🎯 O Desafio (Business Case)
O cliente Aria.net operava seu portal em instâncias **Amazon EC2** (t3.medium). Esta abordagem gerava custos fixos elevados, necessidade de manutenção constante (patching de SO) e complexidade para escalar. 

**A Solução:** Migração para uma **Arquitetura Serverless** de Static Website Hosting, eliminando a gerência de servidores e reduzindo o **TCO (Total Cost of Ownership)**.

---

## 🛠️ Stack Tecnológica & Decisões Técnicas

| Ferramenta | Aplicação | Justificativa Técnica |
| :---: | :--- | :--- |
| **Amazon S3** | Storage & Hosting | Alta durabilidade (11 noves) e custo-benefício imbatível para conteúdos estáticos. |
| **Terraform** | IaC (Infra as Code) | Garante que a infraestrutura seja imutável, replicável e livre de erros manuais. |
| **AWS CLI** | Gestão de Recursos | Utilizado para automação de deploy e sincronização de artefatos. |

---

## 📈 Impacto de Negócio e FinOps
* **Redução de Custos:** Economia estimada de **~98%** em comparação ao ambiente anterior em EC2.
* **Manutenção Zero:** Sem servidores para atualizar, o foco da equipe fica 100% no código da aplicação.
* **Escalabilidade Nativa:** Capacidade de suportar picos de tráfego sem intervenção humana.

---

## 🔒 Segurança e Governança via Código
Diferente de configurações manuais, este projeto implementa segurança por padrão:
* **Public Access Block:** Configurado via Terraform para evitar exposição acidental de dados sensíveis.
* **Least Privilege:** Bucket Policy desenhada para permitir apenas a leitura pública necessária para o site (`s3:GetObject`).

---

## 📸 Galeria de Engenharia (Case Study)

### Fase 1: Planejamento e Init (IaC Workflow)
O processo inicia com a validação do código Terraform, garantindo que o plano de execução esteja alinhado com as necessidades de negócio.
<img src="img/Terraform%20I.png" width="100%">

### Fase 2: Configuração de Variáveis e Outputs
Automação na extração do Endpoint gerado pela AWS, facilitando o processo de entrega contínua.
<img src="img/Terraform%20IV.png" width="100%">

### Fase 3: Segurança e Políticas de Bucket
Implementação da blindagem do bucket, garantindo que o portal esteja online, mas protegido contra acessos não autorizados.
<img src="img/Terraform%20V.png" width="100%">

### Fase 4: Validação Final (Portal Online)
O resultado final: infraestrutura moderna, segura e com performance de baixa latência entregue via automação.
<img src="img/image_b791f0.png.png" width="100%">

---

## 🏁 Conclusão
O projeto **Aria.net** demonstra como a escolha correta de serviços de nuvem e a automação via código podem transformar a agilidade de um negócio, otimizando recursos financeiros e operacionais.

---
*Documentação desenvolvida por Gustavo Gomes para fins de portfólio técnico.*
