denis@DDA-VirtualBox:~/Ansible$ ansible-playbook nginx.yml

PLAY [NGINX | Install and configure NGINX] *************************************

TASK [Gathering Facts] *********************************************************
ok: [nginx]

TASK [NGINX | Install EPEL Repo package from standart repo] ********************
ok: [nginx]

TASK [NGINX | Install NGINX package from EPEL Repo] ****************************
ok: [nginx]

TASK [NGINX | Create NGINX config file from template] **************************
changed: [nginx]

RUNNING HANDLER [reload nginx] *************************************************
changed: [nginx]

PLAY RECAP *********************************************************************
nginx                      : ok=5    changed=2    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0   

denis@DDA-VirtualBox:~/Ansible$ curl http://192.168.56.2:8080
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN">
<html>
<head>
  <title>Welcome to CentOS</title>
  <style rel="stylesheet" type="text/css"> 

	html {
	background-image:url(img/html-background.png);
	background-color: white;
	font-family: "DejaVu Sans", "Liberation Sans", sans-serif;
	font-size: 0.85em;
	line-height: 1.25em;
	margin: 0 4% 0 4%;
	}

	body {
...
