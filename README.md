# Ansible_EMC_ECS
a collection of ansible playbooks for Dell EMC ECS

The playbooks here demonstrate how we can use ansible to interact with Dell EMC ECS.
1. The folder ECSmgmt has example playbooks using the ansible "URI" module with the ECS management API
2. The folder ECSapi has an example playbook using the ansible "AWS_S3" module with ECS S3 Data API

Please note:  The "URI" module with POST opteraion is not idempotent; hence there are always two fucntional tasks in the playbook.
              - The first checks for the desired outcome/state.
              - The second is a "rescure function" in the playbok which is only called in the event the first task fails.
