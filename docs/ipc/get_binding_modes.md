# GET_VERSION
Retrieves a list of valid binding modes. The "default" binding mode is always in the list.

## Payload
Empty

## Reply
```json
[
    string
]
```

For example:
```json
[
    "default",
    "resize",
    "selecting",
    "dragging",
    "moving"
]
```