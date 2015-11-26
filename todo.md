1.  Last line min length = 2 x `\\parindent`.
2.  Find good values for the line-breaking parameters.
3.  Problem:
    Text block height calculation
    does not account for headline and footline.
    -   It might leave the
        too close to the top of the page.
    -   Redo the calculation
        to account for the headline and footline?
    -   Warn if any margin is too small?
