1.  Find good values for the line-breaking parameters.
1.  Problem: API for text block dimensions.
    Guessing the text block height from the leading and line count is awkward.

    Possibilities:
    1.  Fit height to desired line count.
    1.  Calculate line count from height,
        then adjust height to fit line count exactly.
    1.  Specify height and width, and split margins.
    1.  Specify four margins.
1.  trim sizes
    - each sets the text block
    - fivebyeight
