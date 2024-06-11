# Animations
Miracle supports a number of different built-in animations that can
be configured by the user. If you would like to turn off animations
by default, please see [Enable Animations](./enable_animations.md).

## Key
```
animations
```

## Value
A list of:
```yaml
# The event that you want to animate
event: window_open,
    window_move,
    window_close,
    workspace_switch

# The type of animation that will happen when the event is triggered
type: disabled,
    slide,
    grow,
    shrink,

# The interpolation function applied to the animation.
# https://easings.net/ is a great resource to describe these
function: linear,
    ease_in_sine,
    ease_out_sine,
    ease_in_out_sine,
    ease_in_quad,
    ease_out_quad,
    ease_in_out_quad,
    ease_in_cubic,
    ease_out_cubic,
    ease_in_out_cubic,
    ease_in_quart,
    ease_out_quart,
    ease_in_out_quart,
    ease_in_quint,
    ease_out_quint,
    ease_in_out_quint,
    ease_in_expo,
    ease_out_expo,
    ease_in_out_expo,
    ease_in_circ,
    ease_out_circ,
    ease_in_out_circ,
    ease_in_back,
    ease_out_back,
    ease_in_out_back,
    ease_in_elastic,
    ease_out_elastic,
    ease_in_out_elastic,
    ease_in_bounce,
    ease_out_bounce,
    ease_in_out_bounce

# Time in seconds that the animation will take to complete
duration: float

# Constant values that you can tweak for the various easing
# functions. You can find their meanings on https://easings.net/
c1: float  # default: 1.2
c2: float  # default: 1.83
c3: float  # default: 2.2
c4: float  # default: 2.0943951023931953
c5: float  # default: 1.3962634015954636
n1: float  # default: 7.5625
d1: float  # default: 2.75
```

## Default
```yaml
animations:
    - event: window_open
      type: grow
      function: ease_in_out_back
      duration: 0.25
    - event: window_move
      type: slide
      function: ease_in_out_back
      duration: 0.25
    - event: window_close
      type: shrink
      function: ease_out_back
      duration: 0.25
    - event: workspace_switch
      type: slide
      function: ease_out_sine
      duration: 0.175
```

## Example
```yaml
# ~/.config/miracle-wm.yaml

# Override the workspace switching animations such that it takes
# 1s and linearally interpolates to the target workspace
animations:
  - event: workspace_switch
    type: slide
    duration: 1
    function: linear
```