# Introduction

This website is about _hyperlinked twin websites_ of GitHub project repositories.

!!! note ""

    The icons :material-lightbulb: and :material-lightbulb-outline: toggle between light and dark mode.
    The present website also supports auto-toggling, indicated by :material-lightbulb-auto:.

Hyperlinked twins support _precise name-based code navigation online in ordinary web browsers!_
The hyperlinks and highlighting make it much easier to browse, explore, and understand code
in unfamiliar repositories or languages.

!!! tip

    Jump between references and declarations just by clicking on names.

A paper about generation of hyperlinked twins was 
[presented at SLE](https://2023.splashcon.org/home/sle-2023#program) in October 2023:

> [Online Name-Based Navigation for Software Meta-languages](https://doi.org/10.1145/3623476.3623528 "DOI")

The sources of the webpages were generated using Spoofax from the analysed language project.
The hyperlinks added to names were generated from the name binding analysis used by Spoofax,
and the syntax highlighting corresponds closely to that displayed when browsing files in Spoofax.

The aim is for a future release of Spoofax to support generation of hyperlinked twin websites
with code in all [Spoofax meta-languages].

The [published websites](examples.md) are built from the generated files
using [Material for MkDocs].[^plugin]

[^plugin]: The [mkdocs-awesome-pages-plugin] overrides the built-in title transformation
    [currently made by MkDocs](https://github.com/mkdocs/mkdocs/issues/2086>).

[Spoofax]: https://spoofax.dev
[Spoofax meta-languages]: https://spoofax.dev/references/#spoofax-meta-languages
[SDF repo]: https://github.com/metaborg/sdf
[Material for MkDocs]: https://squidfunk.github.io/mkdocs-material
[mkdocs-awesome-pages-plugin]: https://github.com/lukasgeiter/mkdocs-awesome-pages-plugin
