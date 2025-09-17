# Environment Variables
A list of environment variables that are set when the compositor starts.

## Key
```
environment_variables
```

## Value
A list of:

```yaml
- key: string
- value: any
```

## Example

```yaml
# ~/.config/miracle-wm/config.yaml

environment_variables:
  - key: mesa_glthread  # Setting mesa_glthread to false fixes some AMD issues
    value: false
```
