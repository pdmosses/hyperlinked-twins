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
the link then jumps to the first declaration.

### Name declarations

In general, there may be any number of references to a name declaration.
Clicking on a declaration displays a modal with links to all the references to the declaration.[^1]

[^1]: When there is only one reference to a declaration,
​    clicking on the declaration jumps directly to the reference.
​    When there are no references to a declaration,
​    clicking on it has no effect.

!!! tip

    To close a modal, either click its × button, or click anywhere outside the modal display.

### Tooltips

Each name reference and declaration has a `title` attribute that browsers may display
when hovering over the name with a pointing device.[^title]

The title indicates whether the name occurrence is a declaration or a reference.
When it is a declaration, it also indicates how many references to it were found.

[^title]: Browsers on mobile devices don't display title attributes.
    Moreover, the Safari desktop browser (version 17) doesn't display them. 

## Formatting

### Page layout

The generated hyperlinked twins display the title of each file at the top of the page.

They also display a link to the GitHub repository file from which each page was generated.[^2]

[^2]: Hyperlinked twins are currently generated from forks of the original repositories.

### Typography

The verbatim display of the specification text uses a fixed-width font,
to ensure that alignment corresponds exactly to that shown on GitHub.

!!! note

    Unfortunately, many files in Spoofax meta-languages contain _tab_ characters.
    It appears that the authors of the files have used various tab-width settings.
    The generated pages currently interpret tab characters as 8 spaces,
    so the alignment may differ from that shown when browsing the files in Spoofax.

### Colour themes

The colours, font-styles, and font-weights should appear the same in the browser
as in Spoofax when using a light theme.

Spoofax automatically inverts the lightness of the colours when Eclipse is using a dark theme.
This feature has been implemented also on the hyperlinked twins,
with a toggle for switching between the light and dark theme.[^3]

[^3]: The dark theme is currently implemented by a transformation in CSS,
    and the resulting colours may differ from those shown in Eclipse.
