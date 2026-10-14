# Laboratory 08 - Cloud Security Engineer

## Mission Overview

This laboratory focuses on securing a Linux cloud server using UFW (Uncomplicated Firewall). The activity demonstrates how firewall rules can control network traffic, reduce security risks, and protect a web application running inside a Docker container.

## Objectives

- Understand important cloud security concepts.
- Explain the Principle of Least Privilege, Attack Surface, and Default Deny Policy.
- Deploy an Nginx web application using Docker.
- Configure UFW firewall rules.
- Allow SSH access for remote administration.
- Block incoming traffic by default.
- Allow legitimate web traffic through TCP port 8080.
- Verify firewall rules and document the results.

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

- Understanding cloud security best practices
- Applying the Principle of Least Privilege
- Identifying server attack surfaces
- Configuring Linux firewall rules
- Managing incoming and outgoing network traffic
- Securing SSH access
- Managing TCP ports
- Testing web application connectivity
- Documenting security configurations
