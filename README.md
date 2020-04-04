# create-instance-ec2-with-ansible

## File create_instance.yaml <br/>
In this file, we have multiple parameters :<br/>
example of type ec2 instance <br/>
- name: Creating an ec2 Instance <br/>
    ec2: <br/>
      instance_type: t2.micro <br/>
      image: ami-03d8059563982d7b0 <br/>
      key_name: ubuntu-central-1 <br/>
      region: eu-central-1<br/>
      aws_access_key: "{{AWS_ACCESS_KEY_ID}}" <br/>
      aws_secret_key: "{{AWS_SECRET_ACCESS_KEY}}"<br/>
      group: default<br/>
      vpc_subnet_id: subnet-316a8b4d<br/>
      assign_public_ip: yes<br/>
      wait: yes<br/>
      instance_tags:<br/>
        Name: tags Instance<br/>

## File Credentials.yaml<br/>

In this file, we make the de differents parameters <br/>
AWS_ACCESS_KEY_ID Your acces key ID <br/>
AWS_SECRET_ACCESS_KEY to use to connect in this instance
