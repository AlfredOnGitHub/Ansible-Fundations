Ansible Fundations 1.

Cool stuff that I like to do with Ansible.

Right now, this will do quite a few things:

- Create user ansible, gid 10250 group wheel
- Check if system is updated
- Update system if needed
- Reboot the server if needed
- Check if httpd and python are installed individually
- Install these services if needed
- Install and start firewalld
- Enable persistently 80/TCP 443/TCP
- Change sshd port to XXXX and restart sshd #Comented. Use it if you want to.
- Ensure Selinux is enforced
- Change /var/www/html/\* to selinux context httpd_sys_rw_content_t
- Put (or create) index.html into /var/www/html/index.html and restart the service.
- Start the service.
- Check if it is running using the uri module.

You must know that you need a virtualmachine to run this. The files that you actually need to change to make it work are the next following:

- growing.yml
- test/handlers/main.yml
- test/tasks/main.yml
- test/tasks/security.yml
