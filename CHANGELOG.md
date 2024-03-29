## Changelog
### v1.3.8
- The script now supports the new Hookshot Media site Time Extension.

### v1.3.7
- New search term option added: `%searchPlusAlpha%`. This replaces spaces with plus signs, and strips any non-alphanumeric character from the search term. Additionally, the GameFAQs custom search engine on the [custom search engine page](https://github.com/xdpirate/GameSearchHelper/blob/main/CustomSearchEngines.md) has been updated accordingly, as it would sometimes crash if there were non-alphanumeric characters in the search term, URL encoding notwithstanding.

### v1.3.6
- The script now runs on GOG.com (Game pages)

### v1.3.5
- Fixed a bug where new installations wouldn't let any custom search engines appear

### v1.3.4
- Adding or removing customs search engines should no longer mess with your sort order

### v1.3.3
- You can now sort the order in which your search engines appear:
  - Open the options page, then grab the handle to the left of each search engine to reorder it
  - Your sort will apply both to the lists in the options page, and to the order the search engine icons appear on the page
  - Custom sort order is saved on a per-context basis, just like the state of enabled search engines
  - Adding/removing custom search engines may mess with your saved order
  - This feature uses the excellent [Sortable](https://github.com/SortableJS/Sortable)

### v1.3.2
- The script now runs on OpenCritic.
- Selection filters are now hidden on the Github custom search engine page

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
