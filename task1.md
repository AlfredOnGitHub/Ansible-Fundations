# Ansible basic usage

## Constraints: make sure to not use "command/shell" modules unless is STRICTLY necessary

- Create user ansible, gid 10250 groups ansible,wheel
- Update system
- Install httpd
- Install and start firewalld
- Enable persistently 80/TCP 443/TCP
- Change sshd port to 3105 and restart sshd
- Ensure Selinux is enforced
- Change /var/www/html/* to selinux context httpd_sys_rw_content_t
- Put (or create) index.html into /var/www/html/index.html and restart the service.

## Make sure all changes can survive to a system reboot

## Idempotency is *MANDATORY* 
