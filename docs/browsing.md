# Browsing

It should be easy enough to browse the hyperlinked twins *without* reading this section.
The following explanations may however clarify the rationale for some features.

## Name-based navigation

A specification in a Spoofax meta-language may consist of a collection of modules,
each in a separate file.
Name binding is multi-file: a name declared in one module may be referenced in other modules.[^imports]

[^imports]: In some meta-languages, module imports are implicit.

Each name reference in a hyperlinked twin webpage is a clickable link to a declaration.
However, a name declaration may be split across different pages;
a reference to the name then links to its first declaration
(either in the same file as the reference,
otherwise in the file with the file with the first relative URL, ordered lexicographically).

In general, there may be any number of references to a name declaration.
Each declaration in the generated webpage links to the first such reference.
(When browsing or editing files in the Spoofax language workbench,
declarations don't provide any links to references.)

Each name reference and declaration has a `title` attribute that browsers may display
when hovering over the name with a pointing device.[^title]
The title shows the line number of the target of the link,
together with the relative URL of its module for hyperlinks to other files.
It also lists the line numbers and URLs of any further occurrences of the name.[^missing]

[^title]: Browsers on mobile devices don't display title attributes.
    Moreover, it appears that the Safari desktop browser doesn't when full-screen. 

[^missing]: It appears that the Spoofax name analysis does not always include inter-module references
    in the absence of direct imports.
    Then the title on a declaration may indicate that there are no references to it,
    which may be misleading.

When the title of a name reference or declaration contains more than one line number,
it should be possible to display it as a pop-up or modal
containing clickable links to all the listed lines and files.
However, this is not currently a feature of Spoofax itself,
and the appearance of pop-ups might be too distracting when browsing a hyperlinked twin.
Perhaps clicking on a name should display a modal whenever the name is linked to lines on more than one page,
instead of linking directly to an occurrence on the first page.

## Formatting

The generated hyperlinked twins display the title of each file at the top of the page,
followed by a link to the GitHub repo file from which the page was generated.

The verbatim display of the specification text uses a fixed-width font,
to ensure that alignment corresponds exactly to that shown on GitHub.

!!! note

    Unfortunately, many files in Spoofax meta-languages contain tab characters.
    It appears that the authors of the files have used various tab-width settings.
    The generated pages currently interpret tab characters as 8 spaces,
    which may give different alignment from that shown in Spoofax.

The colours, font-styles, and font-weights should appear the same in the browser
as in Spoofax when using a light theme.
Spoofax automatically inverts the lightness of the colours when Eclipse is using a dark theme;
however, this feature has not yet been implemented on the hyperlinked twins,
so the toggle for switching to dark mode is currently omitted.
