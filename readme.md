# Ansible Playbook for an Nginx Server
This is a playbook to setup an nginx server in a remote location. It also setups a new default html homepage for the nginx server.

---

### Prerequisites:
- Have a passwordless ssh connect permission to the Server/Vm. 
- Ansible 

### Steps:

- Change the inventory.ini contents with the your username and remote address.
  
  `
  [$username]@[$IPaddr] 
  `
 
- Then run this command:
  ```sh
   ansible-playbook playbook.yml --check -i inventory.ini
  ```
- If the Checks are alright run this command:
  ```
   ansible-playbook playbook.yml -i inventory.ini
  ```  

**Now your nginx server must be running well with the custom html page**  

---
*Note - The playbook is only tested on Ubuntu 24.04lts VM's*