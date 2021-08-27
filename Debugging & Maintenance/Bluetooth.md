## No utility from gnome

**Check Driver**

**Check Module is loaded**

**Check service**

```bash
systemctl status bluetooth.service
```

result: Service installed, loaded, but not enabled, not start and blocked by rfkill

**Resolution**

```bash
systemctl enable bluetooth.service
systemctl start bluetooth.service
sudo rfkill unblock bluetooth
systemctl restart bluetooth.service
```

