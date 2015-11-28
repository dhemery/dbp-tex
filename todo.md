## Font Sizes

- Given a typeface and a font size,
    calculate the appropriate optical size ftag.

## Line Breaking

Specify reasonable values for the line-breaking parameters.

## Text Block

The current API is awkward.
Guessing the text block height
from the leading and line count is not obvious.

### Vertical

#### Height
- `\textheight` = dimen
- **`\textlines`**
    - requires
        - `\textsize`
        - `\leading`

#### Margin
- `\topmargin` = dimen
- `\topmarginratio` = thoundandths

#### Head and Foot
- **add to height** (bringhurst recommends this)
- include in height

### Horizontal

#### Width

- `\textwidth` = dimen

#### Margins
- `\spinemargin` (edge implied)
- `\spineoffset` (split remainder)
- `\spineoffset` + `\spinemarginratio`

## Trim Sizes

*Note: I do not need this yet.
YAGNI?*

- 5in-x-8in.tex
