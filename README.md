# agnosticlp-ui
Agnostic-LP User Interface

This component will allow you to setup the frontend for your lab development.
It consist in 1 playbook which will use jinjer template to generate static html based on your input definition.

Folders:

-input
Contains a yml definition file for your html structure. It defines how many iframes, content(url) and its style.

File content structure:
List of frames. Each framew will have a name, title, height, width and a public/private url.

-playbooks
Ansible playbook will generate the html based on your input definitions using jinja2 template.

-templates
A jinja2 template file (index.jinja2) already created with a basic structure.
This template will be used by the playbook to generate the static html files based on your input file.

-web_app
All the playbook generated files in form of static html (index.html).  

Steps to setup your environment

Pre-reqs:
* Ansible installed



1- Download the source code from the repository
git clone https://github.com/redhat-gpte-devopsautomation/agnosticlp-ui.git

2- Goto your downloaded source folder: agnosticlp-ui

3- Goto input folder and change the yml file content based on your needs.

4- Run ansible-playbook playbooks/create-ui.yml