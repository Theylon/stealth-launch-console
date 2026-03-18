# 3D Landing Page Implementation Guide

Use this guide when generating the final single-file page.

## Required stack

- HTML document with embedded CSS and JavaScript
- Tailwind via CDN
- Three.js via CDN

## Required prompt inputs

Treat these as the normal input slots for this skill:

- `Website Context`
- `Aesthetic`

If the user omits one, infer a reasonable default from the request and proceed.

## Recommended page structure

Use a layered structure:

1. Fixed background canvas wrapper
2. Atmospheric overlays for contrast and depth
3. Foreground content sections

Suggested section rhythm:

- Hero
- Proof or feature strip
- Story or benefits section
- Deeper feature section
- CTA footer

The page should be long enough for scroll-linked motion to read clearly.

## Three.js checklist

- Create a `Scene`, `PerspectiveCamera`, and `WebGLRenderer`
- Mount the renderer canvas into a fixed full-screen container
- Use antialiasing and alpha where appropriate
- Set size on load and resize
- Cap pixel ratio, for example with `Math.min(window.devicePixelRatio, 1.75)`
- Use a small set of premium-looking meshes instead of many cheap ones

## Lighting checklist

Always create three distinct lights:

- Key light: dominant direction and strongest intensity
- Fill light: softer counter-balance
- Rim light: back or side separation glow

Optional additions:

- low ambient light
- subtle point light tied to pointer or scroll

## Material checklist

Prefer `MeshPhysicalMaterial` with combinations of:

- `transmission`
- `thickness`
- `roughness`
- `metalness`
- `ior`
- `clearcoat`
- `opacity`

Use these to create frosted-glass, ice-like, pearl, or polished translucent effects.

## Motion checklist

Base motion:

- slow object rotation
- floating via sine-wave offsets
- gentle camera drift or group drift

Scroll-linked motion:

- map scroll progress to object position, rotation, group offset, or camera position
- vary reaction by section instead of using one flat multiplier
- keep the effect cinematic, not chaotic

## Tailwind and layout guidance

- Use Tailwind utility classes directly in the HTML
- Add custom CSS only for atmosphere, canvas layering, typography imports, and non-trivial effects
- Use overlays, blur panels, gradients, and subtle borders to separate text from the scene

## Response format

Return only:

```html
<!DOCTYPE html>
<html>
...
</html>
```

No preamble, no markdown explanation, no file list.
