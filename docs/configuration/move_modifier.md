# Move Modifier
While the specified modifier is held and the user clicks the primary mouse
button, they will be able to translate the container 
under the pointer to the resulting position of the cursor. If this
container belongs to a group of containers (e.g. a floating mini tree), then
the entire tree will be translated. This command does **not**

## Key
```
move_modifier
```

## Value
```yaml
String[]
```

For a list of valid modifiers, see [Action Key](action_key.md).

## Default
```yaml
move_modifier:
  - primary
```

## Example
```yaml
# ~/.config/miracle-wm.yaml

move_modifier:
  - primary
  - shift
```
