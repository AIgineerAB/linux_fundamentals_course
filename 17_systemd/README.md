# systemd to manage services in Linux

## TODO update this file


<a href="" target="_blank">
  <img src="https://github.com/kokchun/assets/blob/main/linux/.png?raw=true" alt="" width="600">
</a>

## Steps to autostart a user script 

1. Create a bash script 
2. symlink it to "home/<username>/.local/bin", e.g.
```bash
ln -s <path_to_script> ~/.local/bin/<scriptname>
```
3. Create a unit file `~/.config/systemd/user/<service-name>.service`

4. Reload systemd, activate and start service

```bash
sudo systemctl daemon-reload
sudo systemctl enable <service-name>.service
sudo systemctl start <service-name>
```

5. Check status 

```bash
systemctl status <service-name>
```


## Example of a unit 

```ini
[Unit]
Description="Backup pictures"
# symlink to boot mode config file for your system
# i.e. start this service after boot process is finished
After=default.target

[Service]
# runs once
Type=oneshot
# %h -> home directory
ExecStart=%h/.local/bin/backup-secrets

[Install]
# service starts when boots normally
WantedBy=default.target
```

<br>
<br>