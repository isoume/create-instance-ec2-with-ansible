# create-instance-ec2-with-ansible

## File create_instance.yaml
In this file, we have multiple parameters :
example of type ec2 instance
- name: Creating an ec2 Instance
    ec2:
      instance_type: t2.micro
      image: ami-03d8059563982d7b0
      key_name: ubuntu-central-1
      region: eu-central-1
      aws_access_key: "{{AWS_ACCESS_KEY_ID}}"
      aws_secret_key: "{{AWS_SECRET_ACCESS_KEY}}"
      group: default
      vpc_subnet_id: subnet-316a8b4d
      assign_public_ip: yes
      wait: yes
      instance_tags:
        Name: tags Instance

## File Credentials.yaml

In this file, we make the AWS_ACCESS_KEY_ID and the AWS_SECRET_ACCESS_KEY to use to connect in this instance
