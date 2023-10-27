systemd_journald
---

Configure systemd-journald.


### Links
- <https://www.freedesktop.org/software/systemd/man/systemd-journald.service.html>
- <https://www.freedesktop.org/software/systemd/man/journald.conf.html>


### Variables
- **`systemd_journald_configs`** *(type=[], mandatory)* - List of objects with struct `{filename: "", content: ""}`, where `filename` - filename in `/etc/systemd/journald.conf.d/` and `content` - multiline string with config file content.


### Examples
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
