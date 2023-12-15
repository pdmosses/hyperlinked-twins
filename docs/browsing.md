# Browsing

It should be easy enough to browse the hyperlinked twins *without* reading this section.
The following explanations may however clarify the rationale for some features.

## Name-based navigation

Name-based navigation uses hyperlinks between references and declarations
to browse a repository.

Clicking on a hyperlinked name can be much easier than trying to locate
the declaration of a name manually – especially in a large and unfamiliar repository,
or in a language with unfamiliar name binding constructs.

Clicking on names is also much less effort than drilling up and down in nested directories,
scrolling around in individual pages,
or using search interfaces.

### Name references

Each name reference in a hyperlinked twin webpage is a clickable link to a declaration.

However, a name may refer to a non-unique declaration;
the reference then links to its first declaration
(either in the same page as the reference,
otherwise in the page with the first relative URL, ordered lexicographically).

### Name declarations

In general, there may be any number of references to a name declaration.
Each declaration in the generated webpage links directly to the first reference to it
when all the references are in a single page;
otherwise clicking on the name displays a modal with a link to a reference in each page.

### Tooltips

Each name reference and declaration has a `title` attribute that browsers may display
when hovering over the name with a pointing device.[^title]

The title shows the line number of the target of the link,
together with the relative URL for hyperlinks to other pages.
It also lists the line numbers and URLs of any further occurrences of the name.

[^title]: Browsers on mobile devices don't display title attributes.
    Moreover, the Safari desktop browser (version 17) doesn't display them. 

### Popups

Clicking on a name declaration displays a modal whenever there are references to it
on more than one page.
The modal has a link to a reference on each page.

!!! tip

    To close a modal, either click its × button, or click anywhere outside the modal.

## Formatting

### Page layout

The generated hyperlinked twins display the title of each file at the top of the page.

They also display a link to the GitHub repository file from which each page was generated.

### Typography

The verbatim display of the specification text uses a fixed-width font,
to ensure that alignment corresponds exactly to that shown on GitHub.

!!! note

    Unfortunately, many files in Spoofax meta-languages contain _tab_ characters.
    It appears that the authors of the files have used various tab-width settings.
    The generated pages currently interpret tab characters as 8 spaces,
    which may give different alignment from that shown when browsing in Spoofax.

### Colour themes

The colours, font-styles, and font-weights should appear the same in the browser
as in Spoofax when using a light theme.

Spoofax automatically inverts the lightness of the colours when Eclipse is using a dark theme.
This feature has now been implemented on the hyperlinked twins,
with a toggle for switching between light and dark mode.
