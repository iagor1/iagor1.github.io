---
layout: default
title: Início
---
<div style="text-align: right; margin-bottom: 20px;">
  <a href="/en/" style="text-decoration: none; padding: 8px 12px; border: 1px solid #666; border-radius: 5px;">🇺🇸 Switch to English</a>
</div>

# Olá, eu sou Iagor 👋

## Portfólio

Sou apaixonado por tecnologia, automação e computação em nuvem. Neste espaço compartilho projetos práticos que resolvem problemas reais de infraestrutura e operação.

## Projeto em destaque

### 🚀 Resize Disk EC2 Automatically

Uma ferramenta em Python para automatizar o aumento de volumes EBS associados a instâncias Amazon EC2. A solução reduz tarefas manuais e torna a operação mais segura ao permitir validar as alterações antes de executá-las.

**O que o projeto faz:**

- Localiza instâncias EC2 a partir de uma lista de nomes;
- identifica o volume EBS associado a cada instância;
- consulta o tamanho atual e calcula o novo tamanho;
- aumenta o volume em GiB usando a API da AWS;
- permite executar em modo de simulação (`--dry-run`);
- registra as etapas e os resultados da operação.
- loga operações feitas(dry run não conta)

**Tecnologias:** Python · AWS EC2 · EBS · boto3 · botocore · argparse · logging

<a href="https://github.com/iagor1/resize_disk_ec2_automatically" style="display: inline-block; text-decoration: none; padding: 10px 14px; border: 1px solid #666; border-radius: 5px;">Ver projeto no GitHub →</a>

### 🔎 Scan Resources Idle AWS

Uma ferramenta em Python que percorre as regiões disponíveis de uma conta AWS para identificar recursos EC2 sem uso e gerar um relatório em CSV. O projeto ajuda a encontrar oportunidades de redução de custos e manter a infraestrutura organizada.

**O que o projeto faz:**

- localiza instâncias EC2 paradas;
- identifica endereços Elastic IP não associados;
- encontra volumes EBS disponíveis e sem associação;
- consulta todas as regiões acessíveis usando as credenciais configuradas;
- extrai o nome dos recursos pela tag `Name`;
- exporta os resultados em CSV, separados por tipo de recurso;
- permite usar credenciais padrão ou um perfil AWS específico.

**Tecnologias:** Python · AWS EC2 · EBS · Elastic IP · boto3 · CSV

<a href="https://github.com/iagor1/scan_resources_idle_aws" style="display: inline-block; text-decoration: none; padding: 10px 14px; border: 1px solid #666; border-radius: 5px;">Ver projeto no GitHub →</a>