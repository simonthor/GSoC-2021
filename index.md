# GSoC Final Report 2021
## Fonts
I also identified which font is being used by the old plotting backend and identified how to configure matplotlib to use the same font. Specifically, for regular text, the `URW Palladio L` font is used, while for mathematical expressions, the `PazoMath` font is used. 

These fonts are specified via an .mplstyle file, which also specifies additional matplotlib rcParams that determines how plots in Rivet should be formatted.

Currently, manual configurations of the fonts and the .mplstyle file are needed to add the Rivet style to matplotlib. This is something that needs to be improved in the future, by automating this configuration using automake, which will be executed when Rivet is installed. Some resources that are relevant to solving this issue are:
- [Where to put the mplstyle file so that matplotlib can find it](https://matplotlib.org/stable/tutorials/introductory/customizing.html#defining-your-own-style)
- [How to make matplotlib find fonts installed in a custom location](https://stackoverflow.com/a/43647344/11841986)

Additional issues and merge requests I have contributed to during GSoC:
- https://gitlab.com/hepcedar/rivet/-/issues/233
- https://gitlab.com/hepcedar/rivet/-/merge_requests/322
- https://gitlab.com/hepcedar/rivet/-/merge_requests/307
- https://gitlab.com/hepcedar/rivet/-/merge_requests/318
