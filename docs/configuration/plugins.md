# Plugins
Specify the plugins that should be registered in the system. A plugin may
be referenced later by its unique name (See [Animations](./animations.md))
for an example.

## Example

```yaml
# Use a plugin animation for window open
plugins:
  - path: /path/to/plugin_playground.wasm
    name: playground
  - path: /another/file.wasm
    name: another

animations:
  - event: window_open
    duration: 0.25
    type: plugin
    plugin_name: playground
```

## Schema
A list of plugins with a path and unique name for reference.

```yaml
plugins:
  - path: <string path>
    name: <string unique>
```

## Properties

### path
:   <small>required</small> **type:** String

    The path to the WebAssembly module that should be loaded as a plugin.

### name
:   <small>required</small> **type:** String

    A unique, referenceable name for the plugin. If a name is specified more than once, only the first encountered plugin will be used.

