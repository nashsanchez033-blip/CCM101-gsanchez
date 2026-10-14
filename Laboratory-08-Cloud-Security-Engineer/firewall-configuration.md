# Firewall Configuration

## Allow SSH Access

Command:

```bash
sudo ufw allow ssh
```

This command allows SSH traffic through port 22 so administrators can remotely access and manage the server.

## Configure Default Firewall Policies

Commands:

```bash
sudo ufw default deny incoming
sudo ufw default allow outgoing
```

These commands block incoming connections by default while allowing outgoing connections from the server.

## Enable the Firewall

Command:

```bash
sudo ufw enable
```

This command activates the configured UFW firewall rules.

## Verify Firewall Status

Command:

```bash
sudo ufw status verbose
```

This command displays the firewall status and its default policies.

## Allow TCP Port 8080

Command:

```bash
sudo ufw allow 8080/tcp
```

This command allows incoming TCP traffic on port 8080 for the web application.

## Verify Numbered Firewall Rules

Command:

```bash
sudo ufw status numbered
```

This command displays the firewall rules with their corresponding numbers.

## Why SSH Must Be Allowed Before Enabling UFW

Enabling UFW before allowing SSH could block remote administrative access and lock the administrator out of the server.

## Important Note

Docker-published container ports may bypass some UFW filtering rules, so UFW configuration alone does not guarantee that a Docker container is protected. Additional Docker-aware firewall configuration may be required in a production environment.
