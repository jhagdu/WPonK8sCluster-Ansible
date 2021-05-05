WordPressOnK8s
===============

Ansible Role to deploy WordPress over a kubernetes cluster

Requirements
------------

Kubectl should be installed and configured  

Role Variables
--------------

Variables which should be included in additional variable files -  

    # Name of K8s Namespace to be created
    namespace: wpspace

    # Number of replicas to create
    wp_mysql_replicas: 3

    # Service Type
    svc_type: NodePort

Dependencies
------------

Depends on Ansible Collections -
- community.kubernetes (To install it use 'ansible-galaxy collection install community.kubernetes')

Example Playbook
----------------

site_deploy.yml is a additional variable file that contains required variables -

    - hosts: servers
      vars_files:
         - wp_deploy.yml
      roles:
         - jhagdu.wordpressonk8s

License
-------

BSD

Author Information
------------------

Author Name: Aman Jhagrolia  
Contact: https://www.linkedin.com/in/amanjhagrolia143  
