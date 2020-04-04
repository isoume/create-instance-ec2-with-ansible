# create-instance-ec2-with-ansible

## File create_instance.yaml <br/>
In this file, we have multiple parameters :<br/>
example of type ec2 instance <br/>
- name: Creating an ec2 Instance <br/>&nbsp;
    ec2: <br/>&nbsp;&nbsp;
      instance_type: t2.micro <br/>&nbsp;&nbsp;
      image: ami-03d8059563982d7b0 <br/>&nbsp;&nbsp;&nbsp;&nbsp;
      key_name: ubuntu-central-1 <br/>&nbsp;&nbsp;
      region: eu-central-1<br/>&nbsp;&nbsp;
      aws_access_key: "{{AWS_ACCESS_KEY_ID}}" <br/>&nbsp;&nbsp;
      aws_secret_key: "{{AWS_SECRET_ACCESS_KEY}}"<br/>&nbsp;&nbsp;
      group: default<br/>&nbsp;&nbsp;
      vpc_subnet_id: subnet-316a8b4d<br/>&nbsp;&nbsp;
      assign_public_ip: yes<br/>&nbsp;&nbsp;
      wait: yes<br/>&nbsp;&nbsp;
      instance_tags:<br/>&nbsp;&nbsp;
        Name: tags Instance<br/>&nbsp;&nbsp;&nbsp;

## File Credentials.yaml<br/>

In this file, we make the de differents parameters <br/>
AWS_ACCESS_KEY_ID: XXXXXXXXXXXX (Your acces key ID) <br/>
AWS_SECRET_ACCESS_KEY: XXXXXXXXXXXXX (secret key to use to connect in this instance)
