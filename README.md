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
The URL to use to search with this custom search engine. Substitute the search term (game name) with one of the following tokens:
- `%search%` - Normal search term substitution. Will keep all characters and just run `encodeURIComponent` on it
- `%searchPlus%` - Same as above, but replaces spaces/`%20` with a plus-sign `+`. Some sites require this, for instance Metacritic tends to crash if you give it a search term with more than three words using spaces and not plus-signs
- `%searchPlusAlpha%` - Replaces spaces with plus-signs like the one above, but also strips out any and all non-alphanumeric character apart from space. GameFAQs, for instance, tend to sometimes give a failed search if it detects URL-encoded special characters

Examples:
- Search GameSpot with a normal search term:<br />`https://www.gamespot.com/search/?q=%search%`
- Search Metacritic, substitute spaces with plus-signs:<br />`https://www.metacritic.com/search/game/%searchPlus%/results`
- Search GameFAQs, substitute spaces with plus-signs, and strip all non-alphanumeric characters:<br />`https://gamefaqs.gamespot.com/search?game=%searchPlusAlpha%`

#### **Icon**
A 16x16 image used to represent the custom search engine. This can be anything that's accepted in a html `<img>` tag's `src` attribute, like a direct URL to an image or an icon, or a [data URI](https://en.wikipedia.org/wiki/Data_URI_scheme) with the image contents itself. I recommend converting an image to a data URI, as that will make it load instantly, instead of having to make a new HTTP request for each icon to be loaded. You can use [Base64 Image Encoder](https://www.base64-image.de/) to easily convert an image into a data URI to paste into this field.

### Options
- **Reorder search engines**<br />
You can reorder both built-in and custom search engines by grabbing the handle next to the search engine you wish to move, then dragging it up and down the list. Your custom order is saved on a per-context basis. Built-in search engines will always appear first in the list once they are placed on the page. If you hate this, you can disable all built-in engines and use the custom list only.

- **Open Startpage proxy results with one click**<br />
Amongst others, sites like OpenCritic have no proper search system to send a request to, only a JavaScript-based search on the site itself. GSH therefore uses Startpage to search OpenCritic, which requires you to click the top result to open the OpenCritic page. This option sends along a custom URL parameter to Startpage when performing that search, detects that parameter, and automatically clicks the top result for you. You can also manually add this parameter (`ocgsh=1`) to any other Startpage URL to achieve the same effect, in order to add other sites with no functioning GET-based search system.

- **Strip non-ASCII characters from search term**<br />
This option strips any non-ASCII character from the game name, such as &trade;, &copy;, &reg;, etc, in order to perform a clean search for the game name only. This *will* break searches for games with names containing non-latin script, such as Japanese. If you need search to work for games in languages with non-latin scripts, disable this option.

## Supported sites
The script currently runs on the following websites. Feel free to request your favorite gaming website to be added to this list!

| Context | Websites | Supported pages |
| --- | --- | --- |
| Epic Games Store | Epic Games Store | Game pages<br />Add-Ons pages |
| GOG.com | GOG.com | Game pages |
| HookshotMedia | Nintendo Life<br />Push Square<br />Pure Xbox<br />Time Extension | Game pages<br />News<br />Reviews<br />Features<br />Guides |
| Metacritic | Metacritic | Game pages<br />Games home<br />System home<br />Game lists/browse pages<br />Legacy page |
| OpenCritic | OpenCritic | Game pages |
| Steam | Steam | Game pages<br />Bundle pages |
| Wikipedia | English Wikipedia | Articles about games<br />Articles about game franchises |

<br />

## Built-in search engines
- Startpage
- Google
- Metacritic
- OpenCritic
- eBay.com
- eBay UK

## Changelog
You can read the changelog [here](https://github.com/xdpirate/GameSearchHelper/blob/main/CHANGELOG.md).

## Support, bug reports, or contributing
If you've found a bug, need help, would like to contribute code, or have any other concerns, please leave me some [feedback](https://greasyfork.org/en/scripts/441809-game-search-helper/feedback) on Greasy Fork, or create an [issue](https://github.com/xdpirate/GameSearchHelper/issues) in the Github repository.

## Disable GSH on specific sites
If you don't want GSH to run on one of its supported sites, you can add user excludes through your userscript manager. 

In Tampermonkey:
1. Click the Tampermonkey toolbar icon
1. Click Dashboard
1. Find Game Search Helper and click on its name
1. Click the Settings tab
1. Scroll down to the "Includes/Exclude" section
1. Find the site you would like to exclude in either the "Original includes" or "Original matches" boxes
1. Click the site URL, then click "Add as User excludes" underneath the box
1. GSH will no longer run on that site

Other userscript managers should have equivalent functionality available.

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

## Credits
Game Search Helper uses [Sortable](https://github.com/SortableJS/Sortable), which is licensed under the MIT license:

> Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:
>
> The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.
>
> THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
