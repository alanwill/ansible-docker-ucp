# Ansible Playbook for Docker UCP's networking

Docker UCP requires Engine networking to be [configured](https://docs.docker.com/ucp/networking/) before the cluster is really usable. This is a really tedious task to do on every node and it only gets worse the larger the cluster. This Ansible playbook should do the required work in a few seconds.

This playbook assumes the following tagging structure:

| UCP Component | Tag Key | Tag Value |
| ------------- | ------- | --------- |
| Primary Controller | Name | UCP Controller Master |
| Replica Controllers | Name | UCP Controller Nodes |
| Worker Nodes | Name | UCP Worker Nodes |

If you're running this on EC2 with Ansible's dynamic inventory configured, you can run the playbook with:

`ansible-playbook -i ~/ec2.py site.yml`
`
