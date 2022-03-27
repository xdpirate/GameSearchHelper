# Game Search Helper
## About
Game Search Helper (GSH) is a userscript that runs on various gaming-related websites, and adds elements that let you search for games on external websites. As an example, when viewing a game on Steam, you can have buttons for searching Metacritic for that game, searching eBay for a physical copy, or a custom search engine to search your favorite review site.

## How to use
### Installation
1. Install a userscript manager addon such as Tampermonkey or Violentmonkey in your browser
1. Install the script from [Greasy Fork](https://greasyfork.org/en/scripts/441809-game-search-helper/) (click install button) or [Github](https://github.com/xdpirate/GameSearchHelper/raw/main/GameSearchHelper.user.js) (direct link)

### Configuration
After installation, navigate to a supported site (see below for an updated list). A small box with a magnifying glass will appear in the top-left corner of the page; Click it to expand the GSH options. The box will show the current context (site or groups of sites) you're in, and which search engines and options are enabled. Your enabled search engines are saved on a per-context basis, meaning you can have different enabled engines for different websites. Make your preferred changes, then press the "Save and reload" button to save your changes.

### Custom search engines
-  Starting with version 1.2, there are a number of custom search engines available for [one-click installation over at the CustomSearchEngines.md page!](https://github.com/xdpirate/GameSearchHelper/blob/main/CustomSearchEngines.md)

You can add any custom search engine you like to the script. To add a new custom search engine, press [new] in the upper-right corner of the custom search engine box within the options page. A new box will pop up beneath it. Fill in a display name, a search URL and an icon in the new text boxes, then click "Save and reload" to save your changes. Here's an explanation of the options:

#### **Display name**
The name of the custom search engine. This will show in the custom search engine list and when you hover over the resulting icon on the page

#### **Search URL**
The URL to use to search with this custom search engine. Substitute the search term (game name) with `%search%`. If you find that this doesn't work as expected, the website might expect spaces in searches to be replaced with plus-signs (+). In that case, substitute `%searchPlus%` instead.

#### **Icon**
A 16x16 image used to represent the custom search engine. This can be anything that's accepted in a html `<img>` tag's `src` attribute, like a direct URL to an image or an icon, or a [data URI](https://en.wikipedia.org/wiki/Data_URI_scheme) with the image contents itself. I recommend converting an image to a data URI, as that will make it load instantly, instead of having to make a new HTTP request for each icon to be loaded. You can use [Base64 Image Encoder](https://www.base64-image.de/) to easily convert an image into a data URI to paste into this field.

### Options
- **Open Startpage proxy results with one click**<br />
Amongst others, sites like OpenCritic have no proper search system to send a request to, only a JavaScript-based search on the site itself. GSH therefore uses Startpage to search OpenCritic, which requires you to click the top result to open the OpenCritic page. This option sends along a custom URL parameter to Startpage when performing that search, detects that parameter, and automatically clicks the top result for you. You can also manually add this parameter (`ocgsh=1`) to any other Startpage URL to achieve the same effect, in order to add other sites with no functioning GET-based search system.

- **Strip non-ASCII characters from search term**<br />
This option strips any non-ASCII character from the game name, such as &trade;, &copy;, &reg;, etc, in order to perform a clean search for the game name only. This *will* break searches for games with names containing non-latin script, such as Japanese. If you need search to work for games in languages with non-latin scripts, disable this option.

## Supported sites
The script currently runs on the following websites. Feel free to request your favorite gaming website to be added to this list!

| Context | Websites | Supported pages |
| --- | --- | --- |
| HookshotMedia | Nintendo Life<br />Push Square<br />Pure Xbox | Game pages<br />News<br />Reviews<br />Features<br />Guides |
| Metacritic | Metacritic | Game pages<br />Games home<br />System home<br />Game lists/browse pages<br />Legacy page |
| Steam | Steam | Game pages<br />Bundle pages |

<br />

## Built-in search engines
- Startpage
- Google
- Metacritic
- OpenCritic
- eBay.com
- eBay UK

## Support, bug reports, or contributing
If you've found a bug, need help, would like to contribute code, or have any other concerns, please leave me some [feedback](https://greasyfork.org/en/scripts/441809-game-search-helper/feedback) on Greasy Fork, or create an [issue](https://github.com/xdpirate/GameSearchHelper/issues) in the Github repository.

## Backup
> There are two kinds of people: Those who do backups, and those who *will*.

As with any data you care about, I recommend you do regular backups of the script settings if you care about your custom search engines. I've tried to write the script in such a way that it should be resilient to future changes and additions, but unforeseen circumstances do occur. I am not a professional programmer, and only do it as a hobby, so no guarantee can be given as to code quality or actual resilience.

## Licensing
Game Search Helper © 2022 xdpirate

This program is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU General Public License for more details.

You should have received a copy of the GNU General Public License along with this program.  If not, see <https://www.gnu.org/licenses/>.

## History
GSH replaces three previous scripts of mine: 
- Steam Game Search Helper
- Hookshot Media Game Search Helper
- GSH OpenCritic Helper

If you installed any of these scripts previously, you can remove all of them, and replace them with this script, as it has all the features of the scripts it replaces.

## Changelog
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
