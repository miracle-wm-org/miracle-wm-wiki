# Startup Apps
A list of applications that will be started when the compositor starts.

## Key
```
startup_apps
```

## Value
A list of:

```yaml
- command: string  # A shell command to be executed

# If true, the application will automatically restart
- restart_on_death: bool

# If true, the application will be started with "systemd-run --user --property Restart=on-failure <COMMAND>"
- in_systemd_scope: bool
```

## Example
```yaml
# ~/.config/miracle-wm.yaml

# Start waybar and swaybg on startup
startup_apps:
  - command: waybar
    restart_on_death: true
  - command: swaybg -i /path/to/my/image
    restart_on_death: true
    in_systemd_scoipe: true
```
