systemd_journald
---

Configure systemd-journald

### Links
- <https://www.freedesktop.org/software/systemd/man/systemd-journald.service.html>
- <https://www.freedesktop.org/software/systemd/man/journald.conf.html>

### Variables
- **systemd_journald_configs** *(type=[], mandatory)* - Objects list with format `{filename: "...", content: "..."}`.

### Example
```yaml
systemd_journald_configs:
- filename: storage.conf
  content: |
    [Journal]
    Storage=persistent
    Compress=yes
    SystemMaxUse=10G
    RuntimeMaxUse=1G
```
