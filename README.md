
# Noodels Bowl (HTML + CSS + SVG)

Minimal animated noodle bowl (steam + chopsticks) using pure HTML/CSS/SVG.

## Structure
```text
noodels/
├─ index.html
└─ style.css
```

## Quick Start
1. Put the HTML in `index.html` and the CSS in `style.css`.
2. Add to `<head>`:
```html
<link rel="stylesheet" href="style.css">
```
3. Open `index.html` in your browser.

## Customize
- Bowl color: `.bowl { background: #5c4033; }`
- Noodle color: change SVG `stroke` (e.g., `#e0aa3e`)
- Steam speed: `.steam { animation: rise 3s infinite; }`
- Noodle sway: `.noodels { animation: wave 2s infinite; }`

## Note
`.lift-group` uses `animation: liftUp ...` but `@keyframes liftUp` is missing. Add:
```css
@keyframes liftUp { 0% { transform: translateY(0); } 100% { transform: translateY(-40px); } }
```

## Troubleshooting
- No styles → verify `style.css` path.
- Not centered → `body { display:flex; height:100vh; margin:0; }`
- Motion too strong → adjust durations/easing.
