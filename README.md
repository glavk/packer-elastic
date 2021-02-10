# Build AMI from Packer and Ansible

You need to install Hashicorp Packer and RedHat Ansible. Also you need AWS SDK installed and configured access token in profile `~/.aws/credentials`\
\
Packer creates AMI from Ubuntu 20.04 on M6g instance type (AWS Graviton2 ARM) and provision via Ansible playbook `packer-es.yml` to setup ElasticSearch. \
From this AMI you need to create EC2. \

## Example run builder

```bash
packer build elastic-arm.json
```

## Links

- [Hashicorp Packer](https://https://www.packer.io/)
- [Ansible playbook for ES](https://github.com/elastic/ansible-elasticsearch)
- [M6g instance type](https://aws.amazon.com/en/ec2/instance-types/m6/)
