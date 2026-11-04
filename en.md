---
layout: default
title: Home
permalink: /en/
---
<div style="text-align: right; margin-bottom: 20px;">
  <a href="/" style="text-decoration: none; padding: 8px 12px; border: 1px solid #666; border-radius: 5px;">🇧🇷 Mudar para PT-BR</a>
</div>

# Hi, I'm Iagor 👋

## Portfolio

I'm passionate about technology, automation, and cloud computing. Here I share practical projects that solve real infrastructure and operations challenges.

## Featured project

### 🚀 Resize Disk EC2 Automatically

A Python tool that automates the process of increasing EBS volumes attached to Amazon EC2 instances. It reduces manual work and makes the operation safer by allowing changes to be validated before they are applied.

**What it does:**

- Finds EC2 instances from a list of names;
- identifies the EBS volume attached to each instance;
- reads the current size and calculates the new size;
- increases the volume in GiB through the AWS API;
- supports simulation mode with `--dry-run`;
- logs the operation steps and results, excluding simulations.

**Technologies:** Python · AWS EC2 · EBS · boto3 · botocore · argparse · logging

<a href="https://github.com/iagor1/resize_disk_ec2_automatically" style="display: inline-block; text-decoration: none; padding: 10px 14px; border: 1px solid #666; border-radius: 5px;">View project on GitHub →</a>

### 🔎 Scan Resources Idle AWS

A Python tool that scans the available regions in an AWS account to identify idle EC2-related resources and generate a CSV report. It helps find cost-saving opportunities and keep infrastructure organized.

**What it does:**

- finds stopped EC2 instances;
- identifies unassociated Elastic IP addresses;
- finds available and unattached EBS volumes;
- scans all regions accessible with the configured credentials;
- extracts resource names from the `Name` tag;
- exports results to CSV, separated by resource type;
- supports default credentials or a specific AWS profile.

**Technologies:** Python · AWS EC2 · EBS · Elastic IP · boto3 · CSV

<a href="https://github.com/iagor1/scan_resources_idle_aws" style="display: inline-block; text-decoration: none; padding: 10px 14px; border: 1px solid #666; border-radius: 5px;">View project on GitHub →</a>

### 📊 Grafana Centralized Logs

An infrastructure project built to demonstrate an end-to-end observability deployment. The entire stack runs in Docker containers, from log collection to centralized visualization in Grafana.

**What it demonstrates:**

- collects Docker container logs in real time with Fluent Bit;
- processes and forwards logs to Grafana Loki;
- centralizes log search and visualization in Grafana;
- uses HAProxy as a reverse proxy and service router;
- configures HTTPS with SSL/TLS certificates;
- organizes services with Docker Compose;
- includes parsing, storage, dashboards, and access protection configurations.

**Technologies:** Docker · Docker Compose · Grafana · Loki · Fluent Bit · HAProxy · SSL/TLS

<a href="https://github.com/iagor1/grafana-centralized-logs" style="display: inline-block; text-decoration: none; padding: 10px 14px; border: 1px solid #666; border-radius: 5px;">View project on GitHub →</a>

### 💾 MySQL Dump to S3

A simple shell script that automates backups of MariaDB/MySQL databases running in Docker containers and uploads the compressed files to an Amazon S3 bucket. The script can also be scheduled with `cron`.

**What it does:**

- runs `mysqldump` inside the database container;
- compresses the backup with `gzip`;
- generates filenames with the date and time;
- uploads the `.sql.gz` file to a configured S3 path;
- verifies that the upload completed successfully;
- can be executed manually or on a schedule.

**Technologies:** Shell Script · Docker · MariaDB/MySQL · AWS CLI · Amazon S3 · gzip · cron

<a href="https://github.com/iagor1/send-mysql-dump-to-s3-script" style="display: inline-block; text-decoration: none; padding: 10px 14px; border: 1px solid #666; border-radius: 5px;">View project on GitHub →</a>

## Professional Experience Highlights

### Reduced Deployment Time with Ansible

Reduced deployment time by approximately 80% by improving Ansible templates. I introduced tags to make tasks more efficient and skip unnecessary steps in specific scenarios.

### Contributed to a Custom Image Creation Project

During my internship at TJRO (Court of Justice of Rondônia), I contributed to the creation of customized RHEL 9 images using Packer. This project gave me valuable hands-on experience supporting the infrastructure team.

### Improved the Reverse Proxy Load-Balancing Algorithm

Changed the reverse proxy's load-balancing algorithm to improve product performance and stability. As part of this work, I also created a service-monitoring script in Lua using the HAProxy library, significantly improving how services were monitored across the company.

### Process Automation

Implemented several process automations, primarily with Ansible. For example, I used n8n to send deployment notifications to Discord. I also converted manual processes into code and automation, always focusing on solving the underlying problem with the most appropriate language or tool.