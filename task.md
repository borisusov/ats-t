Task To Do:

Ansible (use atom as IDE)
read docs: 
https://www.ansible.com/resources/videos/quick-start-video
https://docs.ansible.com/ansible/latest/user_guide/intro_getting_started.html
https://docs.ansible.com/ansible/latest/user_guide/command_line_tools.html
https://docs.ansible.com/ansible/latest/user_guide/intro_inventory.html
https://docs.ansible.com/ansible/latest/user_guide/playbooks.html
!!! https://docs.ansible.com/ansible/latest/user_guide/playbooks_reuse_roles.html
https://docs.ansible.com/ansible/latest/user_guide/become.html
https://docs.ansible.com/ansible/latest/user_guide/modules.html

Write role:
"apache preparation":
1. Role should work with rhel-based and debian OS
2. update all packages
3. Install epel on rhel-based
4. Install pip, python, zip, unzip, network-tools packages (should be parameter)
5. Install nginx
6. Create directories in /opt/nginx (should be a parameter)
    - test
    - static
    - documents
    - downloads
7. create jinja2 template:
    - html file
    - should display all directories in /opt/nginx
    - all directories list should have links to directories in apache
    - html file should be placed in /opt/nginx/index.html
8. Add nginx config:
    - it should be a template
    - it should use /opt/nginx as a root dir
    - should open /opt/nginx/index.html as an index file (if open http://server - it should display index.html)
9. Create playbook and inventory file to run this role
10. Add some parameters to playbook and run (e.g. change directory)
11. Add parameters to playbook run (command line) and run playbook (https://docs.ansible.com/ansible/latest/user_guide/playbooks_variables.html#variable-precedence-where-should-i-put-a-variable)
