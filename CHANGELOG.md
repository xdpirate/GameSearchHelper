## Changelog
### v1.3.1
- The script now runs on English Wikipedia. The script does a decent job of figuring out what's a game and what's not a game using the category designations. If you see it trigger on a non-game or game franchise article, or don't trigger on a game article, let me know!
- Fixed an oversight that would give built-in search engine icons and custom search engine icons different spacing in some contexts

### v1.3.0
- The script now runs on Epic Games Store's game and add-ons pages
- Adjusted the offset of the main GSH options toggle as it would obscure other page elements on Hookshot Media and Epic Games Store
- Added selection filters to both search engine boxes in options (select all, select none, invert selection)

### v1.2.2
- Toggling search engines is now disabled on the Github custom search engine page, as it has no effect there anyway
- Added styles to most elements so the UI stays more consistent across the sites it runs on
- Added tooltips to most elements within GSH to explain or clarify what things do
- Minor text adjustments

### v1.2.1
- Added a link to the new [custom search engine page on Github](https://github.com/xdpirate/GameSearchHelper/blob/main/CustomSearchEngines.md) inside the options box
- The custom search engine Github page now previews the icons for each custom search engine
- Adjusted max size of custom search engine box
- Adjusted some text

### v1.2.0
- Added support for one-click installation of a number of custom search engines at the [CustomSearchEngines.md](https://github.com/xdpirate/GameSearchHelper/blob/main/CustomSearchEngines.md) page on Github! Just visit the page with GSH installed and enabled, then click an installation link to add the respective search engine to GSH.
- Renamed "Load OpenCritic results with one click" to "Open Startpage proxy results with one click".
  - Added a help link from this option to the readme on Github to explain what this means.

### v1.1.2
- The script now supports most game pages on Metacritic. Currently supported pages:
  - Games home (/game)
  - System home (/game/$system)
  - Game browse pages (/browse/games/*)
  - Game detail pages (/game/$system/$gameName)
  - Legacy page (/game/legacy)

### v1.1.1
- The script now supports each game item on Steam bundle pages
- Added an option to strip non-ASCII characters from the search term

### v1.1.0
- The script now supports multi-game pages on Hookshot Media ("Featured Games")

### v1.0.0
- Initial release
