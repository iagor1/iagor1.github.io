---
layout: custom
title: Início
---
<div id="google_translate_element" style="margin-bottom: 20px;"></div>
<script>
  function googleTranslateElementInit() {
    new google.translate.TranslateElement(
      { pageLanguage: 'pt', includedLanguages: 'en,es,fr,de', autoDisplay: false },
      'google_translate_element'
    );
  }
</script>
<script src="https://translate.google.com/translate_a/element.js?cb=googleTranslateElementInit"></script>

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
- registra as etapas e os resultados da operação;
- registra as operações efetivamente executadas, sem contabilizar simulações.

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

### 📊 Grafana Centralized Logs

Projeto de infraestrutura desenvolvido para demonstrar a implantação ponta a ponta de uma aplicação de observabilidade. Toda a stack é executada em contêineres Docker, desde a coleta dos logs até a visualização centralizada no Grafana.

**O que o projeto demonstra:**

- coleta logs de contêineres Docker em tempo real com Fluent Bit;
- processa e encaminha os logs para o Grafana Loki;
- centraliza a busca e a visualização dos logs no Grafana;
- utiliza HAProxy como proxy reverso e roteador dos serviços;
- configura HTTPS com certificados SSL/TLS;
- organiza os serviços com Docker Compose;
- inclui configurações de parsing, armazenamento, dashboards e proteção de acesso.

**Tecnologias:** Docker · Docker Compose · Grafana · Loki · Fluent Bit · HAProxy · SSL/TLS

<a href="https://github.com/iagor1/grafana-centralized-logs" style="display: inline-block; text-decoration: none; padding: 10px 14px; border: 1px solid #666; border-radius: 5px;">Ver projeto no GitHub →</a>

### 💾 MySQL Dump to S3

Um shell script simples para automatizar o backup de bancos MariaDB/MySQL executados em contêineres Docker e enviar os arquivos compactados para um bucket Amazon S3. O script também pode ser agendado com `cron`.

**O que o script faz:**

- executa o `mysqldump` dentro do contêiner do banco;
- comprime o backup com `gzip`;
- gera nomes de arquivo com data e hora;
- envia o arquivo `.sql.gz` para um caminho configurado no S3;
- verifica se o upload foi concluído;
- pode ser executado manualmente ou de forma agendada.

**Tecnologias:** Shell Script · Docker · MariaDB/MySQL · AWS CLI · Amazon S3 · gzip · cron

<a href="https://github.com/iagor1/send-mysql-dump-to-s3-script" style="display: inline-block; text-decoration: none; padding: 10px 14px; border: 1px solid #666; border-radius: 5px;">Ver projeto no GitHub →</a>

## Highlights na experiência profissional

### Redução de tempo de deploy com Ansible
Reduzido tempo de deploys em aproximadamente 80% apenas fazendo melhorias em templates ansible, foi usado tags pra melhorar a eficácia das tasks e pular etapas desnecessárias em determinadas situações. Tempo de deploy caiu de 3 horas pra 36 minutos.

### Colaborado no projeto de criação de imagens customizadas

Projeto feito no meu estágio no TJRO (Tribunal de Justiça de Rondônia) para a criação de imagens personalizadas do RHEL9, atuei usando packer. Foi um trabalho muito interessante e me ajudou bastante o setor de infra.

### Troca de algoritmo do balanceador de carga do proxy reverso

A troca do algoritmo levou mais performance e estabilidade pro produto. Com essa troca também tive que criar um script de monitoramento de serviços baseado em lua e na biblioteca do Haproxy. Esse script revolucionou a forma de monitorar os serviços da empresa.

### Automatizações

Também fui responsável por várias automatizações no setor, principalmente em ansible, fui responsável por implementar com n8n avisos de deploys no discord visíveis para a empresa inteira por exemplo. Melhorias em processos manuais que foram transformados em código (seja lá pra qual linguagem ou ferramenta o foco é resolver o problema)