# uninovaletterhead

Letterhead paper for UNINOVA | Institute for the Development of New Technologies

## Preamble

The latest version of this package is available for download at:

https://github.com/joaomlourenco/uninovaletterhead

If you're not sure if you're using the latest version, take a look and [download](https://github.com/joaomlourenco/uninovaletterhead/archive/refs/heads/main.zip) the latest version! By the way, if you find this package useful, [offer a coffee](https://www.paypal.com/donate/?hosted_button_id=8WA8FRVMB78W8) to my alter-ego *NOVAthesis* and in the comments box say it's for the “*uninovaletterhead*” package! ;)


## Load the “*uninovaletterhead*” package

It's actually very simple to use this “*uninovaletterhead*” package... just add the following command to the preamble of the source file, i.e. after the `\docuemntclass{…}` and before the `\begin{document}`:

```latex
\begin{verbatim}
  \usepackage{uninovaletterhead}
\end{verbatim}
```

where only the first page will be letterheaded; or

```latex
\begin{verbatim}
  \usepackage[everypage]{uninovaletterhead}
\end{verbatim}
```

where all pages will be letterheaded.

## Customize the “*uninovaletterhead*” package

Still in the preamble, you will have to customize your document with the following macros:

| Option | Effect |
|----------|----------|
| \unvresearchgroup | This command receives two arguments, the first with the name of the research group in Portuguese and the second with the name of the research group in English.  They will be converted to capital letters and displayed in the top right corner. *If omitted, nothing will be displayed at the top right corner.*
| \unvtitle     	| This command takes as argument the title of the document.\\
| \unvauthor 	| This command takes as an argument the author's name and, optionally, the author's title/position, to be placed in the signature area. *If omitted, nothing will be displayed. If used multiple times, a signature area will be created for each author.*
| \unvauthorsigfont	| Customizing the font used when writing the name of the author(s) in the signature area.\\
| \unvpositionsigfont | Customizing the font used when writing the position of the author(s) in the signature area.\\

## Customize and show the signature area


There is also a command to create a zone to place a signature. This command has three arguments, the first of which (between “`[…]`”) is optional.

```latex
\begin{verbatim}
\unvsignature[line_size]{position}{offset_from_upper_text}
\end{verbatim}
```

where:

| Argument | Value |
|----------------|--------|
| line_size | *Optional* — Indication of the line size (in any unit valid in LaTeX, e.g. *6cm*, *2in*, *30pt*, etc). *If omitted, it draws a line slightly wider than the name/position.* |
| position | *Mandatory* — Indicates the location of the signature area. Possible values are: `l` signature arrea on the left; `l` signature arrea centered; and `r` signature arrea on the right. |
| offset_from_upper_text | *Mandatory* — Vertical offset of the signature area (in any unit valid in LaTeX, e.g. *3cm*, *2.5in*, *10ex*, etc). |

The signature area at the end of this document, located at the bottom right, was created with:

```latex
\begin{verbatim}
  \unvauthor{João M. Lourenço, Professor Associado @ NOVA FCT}
  ...
  \unvsignature{r}{1.5cm}
\end{verbatim}
```
