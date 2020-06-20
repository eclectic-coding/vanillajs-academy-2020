# Aria Live

The `aria-live` attribute allows screens readers to know the content is dynamic. It can be set to:
- `off` (same as not at all)
- `assertive` (interrupts user to announce changes)
- `polite` (announces updates only)

Exampe:
```javascript
<div id="app" aria-live="polite">The content of this element is going to change.</div>
````

## Project
Modify the previous project to include accessibility.
