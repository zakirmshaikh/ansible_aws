# ansible with AWS

This repository is to create AWS VPC, Security Group,Add Ec2 Key Pair, Ec2 Instance

# cat aws.yml
---
- hosts: localhost
  connection: local
  gather_facts: no
  roles:
    - aws-vpc
    - aws-ec2sg
    - aws-ec2key
    - aws-ec2instance


#Edit only to input variables
aws-vpc/vars/main.yaml

#Create Privat key with name
ansible_key

#run
ansible-playbook aws.yml
