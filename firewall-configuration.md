# Firewall Configuration

## 1. Allow SSH Access

```bash
sudo ufw allow ssh
```

This command allows SSH traffic so administrators can remotely manage the server.

## 2. Configure the Default Policies

```bash
sudo ufw default deny incoming
sudo ufw default allow outgoing
```

The first command blocks incoming traffic by default unless a firewall rule permits it. The second command allows outgoing traffic by default.

## 3. Enable the Firewall

```bash
sudo ufw enable
sudo ufw status verbose
```

These commands activate the firewall and display its current status and default policies.

## 4. Allow the Web Application Port

```bash
sudo ufw allow 8080/tcp
sudo ufw status numbered
```

The first command adds a rule allowing incoming TCP traffic on port 8080. The second command displays the firewall rules with their numbers.

## 5. Why SSH Must Be Allowed First

If `sudo ufw enable` is run before `sudo ufw allow ssh`, a remote administrator could lose SSH access to the server because incoming SSH connections may be blocked by the firewall's default policy.
