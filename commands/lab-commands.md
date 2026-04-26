# Home SOC Wazuh Lab Commands

## Verify SSH is Open

```bash
nmap -p 22 <target-ip>
```

Checks whether SSH is open on the target endpoint.

---

## Create a Small Test Password List

```bash
echo -e "123456\npassword\nadmin\nroot\nkali" > test.txt
```

Creates a short password list for lab testing.

---

## Run Hydra Brute-Force Simulation

```bash
hydra -t 4 -l root -P test.txt ssh://<target-ip>
```

Simulates repeated SSH login attempts.

---

## Search in Wazuh Discover

```text
sshd
```

```text
authentication_failed
```

Filters Wazuh logs for SSH and authentication failure events.

---

## Install UFW

```bash
sudo apt install ufw -y
```

Installs the UFW firewall.

---

## Configure UFW

```bash
sudo ufw default deny incoming
sudo ufw allow ssh
sudo ufw limit ssh
sudo ufw enable
sudo ufw status verbose
```

Blocks inbound traffic by default, allows SSH, rate-limits SSH, and verifies firewall status.
