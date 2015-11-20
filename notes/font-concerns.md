
## Terminology

- **typeface** << family
  - Typeface name
- **scheme** << intent
  - Size
  - Intent (caption, text, subhead, display)
- **family** << style
    - Remove the need for a suffix on these
    - `\bodystyle` --> `\body`
    - `\chaptertitle`
    - `\booktitle`
- **style** = font settings + paragraph settings + …

## Delegating

When I load a font, call various delegates if they exist:
- `\<typeface>loaded#1{}`
  - Called whenever a font of this typeface is loaded
- `\<scheme>loaded#1{}`
  - Called whenever a font of this scheme is loaded
- `\<family>loaded#1{}`
  - Called whenever a font of this family is loaded

## Colliding with other names

- Name families without a suffix: \\body
-
