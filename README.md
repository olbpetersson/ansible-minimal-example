# Ansible minimal example
This is a minimal example of Ansible. It uses docker (and docker compose) to set up a system 
consisting of:
 - controller (the ansible controller)
 - two nodes (ansible targets, dummy nodes)

## Prerequisites and Installation
You need to have docker and docker compose installed, then run 
**docker-compose up**

## Running
To verify that everything is correctly setup, do:
 **docker exec -ti ansibleminimalexample_controller_1 bash** , you should now be in a bash shell
in the controller container. Execute **ansible -m ping all** and you should see three sucessful pings from the three containers.

## Working with and extending the example
The example is setup to mount the volume "work/" inside the home directory of the controller container. When you've entered bash in the running container, try **ansible-playbook playbooks/touchfile.yml**. This will place a file **removeMe.file** in **/tmp/** on all your nodes. Run **ansible-playbook playbooks/removefile.ylm** to remove the file from all nodes.

## Further reading
https://www.ansible.com/
