# Contribute

To set up a development environment,
we recommend using:
- [Pixi](https://pixi.prefix.dev/), to automatically install dependencies,
- [VSCode](https://code.visualstudio.com).

Clone the repository and open the directory with VSCode.
If the [LaTeX Workshop](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop) extension is not installed,
it will suggest doing so.
If that extension and `pixi` are installed,
you're ready to go.

## Compile a chapter

1. Open a chapter under `book/chapters/<number>.tex`,
2. compile it with the green ▶ in the top-right corner,
3. and preview the output PDF file using the button next to it.
4. On the dropdown, select `Subfiles package root file`.

We are using the `subfiles` package to compile separately each chapter.

The compiled PDF and associated files are saved to the `.pixi/_build/` directory.

## Compile the book

Run `pixi run compile-main` on the terminal.

## Rules and style

### Labels

Use the same number that appeared in the book,
as it is easier to replace elsewhere when it appears.
For instance,
when copying the equation 8.1,
use `eq:8.1` as label:

```tex
\begin{equation}
  % the equation itself
  \label{eq:8.1}
\end{equation}
```

### Semantic linefeed

**TL;DR:** put each sentence in a new line.

In LaTeX,
new lines in the source do not generate a new line in the compiled document.

> By starting a new line at the end of each sentence,
> and splitting sentences themselves at natural breaks between clauses,
> a text file becomes far easier to edit and version control.
> 
> —[Semantic Linefeeds](https://rhodesmill.org/brandon/2012/one-sentence-per-line/) by Brandon Rhodes

The same can be applied to long equations:
put long terms after a `+` or `=` sign in a new line.
