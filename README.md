# filter-compound-words
A pandoc filter to make hyphens breakable in LaTeX/PDF output

## Rationale
LaTeX does not allow hyphenation in compound words, which can lead to sub-optimal paragraph composition. This filter replaces hyphens in text paragraphs with a hard hyphen.

## Method
We use `\hyp` from the `hyphenat` package. We thus expect `hyphenat` to be part of the LaTeX template in use.
A previous implementation of a similar filter relied on the `babel` shorthand `"-`, but this one is only available in some language presets. An alternative would be to use 
`\babelhyphen{hard}`, but we decided to not rely on `babel` at all.
