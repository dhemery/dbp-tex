
## Delegating

When I load a font, call various delegates if they exist:
- `\<typeface>loaded#1{}`
  - Called whenever a font of this typeface is loaded
- `\<scheme>loaded#1{}`
  - Called whenever a font of this scheme is loaded
- `\<family>loaded#1{}`
  - Called whenever a font of this family is loaded
