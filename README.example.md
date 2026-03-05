# Email Server — Quick Reference

---


## Manage Accounts

All commands must be executed from: 
```bash
cd ~/your_path/mailserver
```

### Create account
```bash
./setup.sh email add nombre@your_domain
```

### Delete account
```bash
./setup.sh email del nombre@your_domain
```

### Change password
```bash
./setup.sh email update nombre@your_domain
```

### List all accounts
```bash
./setup.sh email list
```

---

## Configure email account on Thunderbird / Outlook

| Campo         | Valor |
|---------------|-------|
| Server IMAP   | `mail.your_domain` |
| Port IMAP     | `993` |
| Security IMAP | `SSL/TLS` |
| Server SMTP   | `mail.your_domain` |
| Port SMTP     | `587` |
| Security SMTP | `STARTTLS` |
| user          | `tu@your_domain` |
| Password      | The one you defined when creating the account. |

---

## Webmail
`https://webmail.your_domain`

---

## Useful Docker commands.

```bash
# See status
docker ps | grep mailserver

# see logs in realtime
docker logs mailserver -f

# Restart
docker restart mailserver

# down and up the container
cd ~/your_path/mailserver
docker compose down
docker compose up -d
```
