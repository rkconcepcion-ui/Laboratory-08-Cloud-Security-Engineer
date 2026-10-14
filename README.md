# Laboratory 08 — The Cloud Security Engineer

## Mission Overview

This laboratory activity focuses on securing a Linux server using the UFW host-based firewall. An Nginx web application was deployed using Docker, and firewall rules were configured to allow required network traffic while blocking incoming traffic by default.

## Objectives

- Understand the Principle of Least Privilege.
- Identify the attack surface of a virtual machine.
- Configure UFW with a default-deny incoming policy.
- Allow SSH and TCP traffic on port 8080.
- Document firewall configurations and security practices.

## Commands Executed

```bash
docker run -d -p 8080:80 --name secure-web-app nginx
curl http://localhost:8080
sudo ufw allow ssh
sudo ufw default deny incoming
sudo ufw default allow outgoing
sudo ufw enable
sudo ufw status verbose
sudo ufw allow 8080/tcp
sudo ufw status numbered
```

## Skills Learned

- Deploying an Nginx container with Docker.
- Testing a web application using curl.
- Configuring UFW firewall rules.
- Applying the default-deny security principle.
- Documenting cloud security configurations using Markdown and GitHub.
