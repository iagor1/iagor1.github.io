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
- logs the operation steps and results.

**Technologies:** Python · AWS EC2 · EBS · boto3 · botocore · argparse · logging

<a href="https://github.com/iagor1/resize_disk_ec2_automatically" style="display: inline-block; text-decoration: none; padding: 10px 14px; border: 1px solid #666; border-radius: 5px;">View project on GitHub →</a>