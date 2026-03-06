# GlossyGlass

<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/6a46de8e-c901-4519-b94e-065b98774319" />
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/9d100614-55d0-4d72-beef-919327bc723f" />

A Discord theme built on [midnight-discord](https://github.com/refact0r/midnight-discord) that replaces the default message layout with WhatsApp-style glass bubbles and a red/pink gradient identity.

## Requirements

- [Vencord](https://vencord.dev) or [BetterDiscord](https://betterdiscord.app) with CSS loading support 
- midnight-discord is imported automatically — no separate install needed

## Installation

1. Copy `GlossyGlass.css` into your client mod's theme folder, or paste it into the custom CSS editor
2. Enable the theme

## Customization

All tuneable values live at the top of the file inside `:root` and `body`. You do not need to touch anything else.

```css
/* Blur levels */
--blur-heavy: 22px;   /* panels, user area, titlebar */
--blur-mid:   15px;   /* bubbles, channel list, chatbar */
--blur-light:  8px;   /* reply preview */

/* Chat area background blur — set to 0px to disable */
--chat-blur: 0px;

/* Wallpaper — replace the URL */
--background-image-url: url('https://i.imgur.com/S3xTtqD.jpeg');
```

To swap the wallpaper, replace the URL in both the `body` block and the `.bg__960e4` rule.

To re-enable chat area blur, set `--chat-blur` to any pixel value, e.g. `12px`.

## Architecture

midnight-discord handles panel island layout, sidebar spacing, window controls, and member list. GlossyGlass handles everything visual: glass finish, bubble system, red/pink gradients, and message layout.

The message area is fully replaced. Discord's default cozy layout is overridden by a block-based bubble system where the avatar floats in a left lane outside the bubble and message content stacks below the username in normal document flow.

## Known limitations

- Avatar decorations are hidden by default due to alignment issues with the bubble layout
- The theme targets midnight-discord's stable class names — if midnight updates its structure, panel islands may need repainting
- `backdrop-filter` is not available in all environments; the theme degrades gracefully to a solid dark tint

Meow I got no idea what I'm doing but feel free to [join](https://discord.gg/tcCGWtW3Pe)

##( Credits

Layout engine: [midnight-discord](https://github.com/refact0r/midnight-discord) by refact0r
