# Citrix-Netscaler-Backup-Ansible-Playbook
Ansible playbook to backup MPX, VPX series Netscaler load balancers

This ansible playbook creates backups on given netscaler host ip addresses, downloads it to local directory, compress all files to one zip file and sends by email, deletes local backup files older then given days.

Needs credentials on /etc/ansible/hosts:

  Example ansible hosts:
  
  [netscalers:vars]
  
  nitro_user=nsroot
  
  nitro_pass=nsroot
  
  email_username=mymail@gmail.com
  
  email_password=mypassword
  
  [netscalers]
  
  10.172.84.98
  
  10.172.84.99
  
  10.172.212.[3:31:2]
  
  ============================================
  
  Usage:
    
    ansible-playbook netscaler-backup.yml
