# ☁️ Desafio DIO: Infraestrutura Automatizada com AWS CloudFormation

---

- **Bootcamp:** GFT - Fundamentos de Cloud com AWS
- **Plataforma:** Digital Innovation One (DIO)
- **Autor:** Evelyn Oliveira Bonatto
- **Status:** 🛠️ Concluído

---

## 📌 Descrição do Projeto

Este projeto consiste na automação da implantação de uma infraestrutura de rede e servidor web na AWS utilizando **AWS CloudFormation** como ferramenta de Infraestrutura como Código (IaC).

O desafio tem como objetivo demonstrar na prática o provisionamento declarativo, reprodutível e seguro de recursos na nuvem.

---

## 🏗️ Arquitetura Provisionada

A stack do CloudFormation provisiona automaticamente a seguinte estrutura:

- **Rede (VPC):** VPC com bloco CIDR `10.0.0.0/16`.
- **Roteamento:** Internet Gateway (IGW) atrelado à VPC e tabela de rotas configurada para acesso à internet.
- **Subnet Pública:** Subnet com atribuição automática de IPs públicos (`10.0.1.0/24`).
- **Segurança (Security Group):** Liberação de tráfego de entrada para acesso web via porta `80` (HTTP) e gerenciamento seguro via **AWS Systems Manager (SSM)**.
- **Servidor Web (EC2):** Instância baseada em **Amazon Linux 2023** configurada via `UserData` para instalar e inicializar automaticamente o servidor **Apache (httpd)**.

---

## 📁 Estrutura do Repositório

```text
.
├── template-infra.yml    # Template CloudFormation
├── README.md             # Documentação do projeto
└── images/               # Evidências de execução no console AWS

---

## 📸 Evidências de Execução (Screenshots)

### 1. Stack Criada no CloudFormation

> Status da stack confirmando o provisionamento dos recursos (`CREATE_COMPLETE`).

![CloudFormation Stack Status](./images/01-stack-status.png)

---

### 2. Eventos da Stack (Events)

> Registro dos eventos e criação em sequência dos recursos.

![Eventos do CloudFormation](./images/02-stack-events.png)

---

### 3. Recursos Criados (Resources)

> Visão geral de todos os recursos AWS provisionados pela stack.

![Recursos da Stack](./images/03-stack-resources.png)

---

### 4. Outputs da Stack

> Valores de saída contendo o IP Público e a URL gerada dinamicamente.

![Outputs do CloudFormation](./images/04-stack-outputs.png)

---

### 5. Instância EC2 em Execução

> Detalhes da instância criada associada ao Security Group e VPC.

![Detalhes da Instancia EC2](./images/05-ec2-instance.png)

---

### 6. Servidor Web em Funcionamento

> Validação do servidor Apache rodando no Amazon Linux 2023 acessado via navegador.

![Aplicacao em Execucao](./images/06-web-app.png)

---

## 🔗 Conecte-se Comigo

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/evelyn-bonatto/)
```
