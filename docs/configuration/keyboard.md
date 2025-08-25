# Keyboard Configuration
Configure the keyboard input device.

## Key
```
keyboard
```

## Value
```yaml
# The keymap.
keymap:
    # The language.
    #
    # You may list the available languages using:
    #   localectl list-x11-keymap-variants
    language: string

    # The variant of the language.
    #
    # You may list the available variants using:
    #   localectl list-x11-keymap-variants
    variant: optional<string>

    # Options on the language variant.
    #
    # These are only applied  if a variant is supplied.
    #
    # You may list the available options using:
    #   localectl list-x11-keymap-options
    options: optional<string>[]
```

## Example
```yaml
# ~/.config/miracle-wm.yaml

# Use the english + dvorak keyboard layout.
keyboard:
    keymap:
        language: en
        variant: dvorak
        options: []
```
