# apple_ansible_task

# Interview Problems
 
## Ansible
 
Write a playbook (using ansible 2.8 or newer) to:
 
- render a template to your Desktop that outputs a role variable and information about your operating system
- the variable should have a default value in the role and be overridden by the playbook
- the template should use standard ansible jinja2 templating
 
Running the playbook should look something like this:
 
```bash
$ ansible-playbook -i local interview-playbook.yml
 
PLAY [all] *****************************************************************************************************************************************************************************************************************************************************************************************************************************************************************
 
TASK [my-role : get os details] ********************************************************************************************************************************************************************************************************************************************************************************************************************************************
[WARNING]: Platform darwin on host localhost is using the discovered Python interpreter at /usr/bin/python, but future installation of another Python interpreter could change this. See https://docs.ansible.com/ansible/2.8/reference_appendices/interpreter_discovery.html for more information.
 
changed: [localhost]
 
TASK [my-role : render my template] ****************************************************************************************************************************************************************************************************************************************************************************************************************************************
changed: [localhost]
 
PLAY RECAP *****************************************************************************************************************************************************************************************************************************************************************************************************************************************************************
localhost                  : ok=2    changed=2    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0
 
$ cat ~/Desktop/my-template.txt

```
 
## What I am looking for

 
- create an inventory
- write a playbook
- write a custom role
- understand how variables work and are overridden in ansible
- show how basic templating works
