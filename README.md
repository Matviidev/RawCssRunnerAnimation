# Web Animations Runner

An infinite runner demo that demonstrates the power and flexibility of the native [Web Animations API](https://developer.mozilla.org/en-US/docs/Web/API/Web_Animations_API).

## Controls

| Key          | Action                |
| ------------ | --------------------- |
| `Space`      | Play/Pause the game   |
| `ArrowUp`    | Jump                  |
| `ArrowRight` | Increase speed by 10% |
| `ArrowLeft`  | Decrease speed by 10% |

## Features

### Core Animations

- **Character Running Animation**: Sprite sheet animation using CSS background positioning, cycled via `steps(8, jump-none)` easing to snap between frames
- **Street Scrolling**: Seamless infinite scroll using `translateX` animation on a 200vw element
- **Dynamic Shadow**: Shadow scales during jumps to create depth illusion, synchronized with the jump animation using shared timing properties
- **Parallax Layers**: Background and foreground layers create depth perception
- **Procedural Cars**: Randomly spawned cars with independently rotating wheels using pseudo-element animations
- **Auto Speed Adjustment**: Speed gradually decreases over time to increase difficulty

### Technical Highlights

- **No animation libraries** - Pure vanilla JavaScript and CSS
- **Programmatic control** - Animations created and controlled via `Element.animate()`
- **Playback manipulation** - `pause()`, `play()`, `playbackRate` for dynamic speed control
- **Async/await** - `animation.finished` promise for sequencing
- **Shared timing** - Shadow animation inherits duration, easing, and direction from jump animation
- **Pseudo-element animations** - Wheels animated using `pseudoElement` option
