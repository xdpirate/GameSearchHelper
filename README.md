# Game Search Helper
## About
Game Search Helper (GSH) is a script that runs on various gaming-related websites, and adds elements that let you search for games on external websites. As an example, when viewing a game on Steam, you can have buttons for searching Metacritic for that game, searching eBay for a physical copy, or a custom search engine to search your favorite review site.

## How to use
### Configuration
After installation, navigate to a supported site. A small box with a magnifying glass will appear in the top-left corner of the page; Click it to expand the GSH options. The box will show the current context (site or groups of sites) you're in, and which search engines and options are enabled. Your enabled search engines are saved on a per-context basis, meaning you can have different enabled engines for different websites. Make your preferred changes, then press the "Save and reload" button to save your changes.

### Custom search engines
You can add any custom search engine you like to the script. To add a new custom search engine, press [new] in the upper-right corner of the custom search engine box within the options page. A new box will pop up beneath it. Fill in a display name, a search URL and an icon in the new text boxes, then click "Save and reload" to save your changes. Here's an explanation of the options:

#### **Display name**
The name of the custom search engine. This will show in the custom search engine list and when you hover over the resulting icon on the page

#### **Search URL**
The URL to use to search with this custom search engine. Substitute the search term (game name) with `%search%`. If you find that this doesn't work as expected, the website might expect spaces in searches to be replaces with plus-signs (+). In that case, substitute `%searchPlus%` instead.

#### **Icon**
A 16x16 image used to represent the custom search engine. This can be anything that's accepted in a html `<img>` tag's `src` attribute, like a direct URL to an image or an icon, or a [data URI](https://en.wikipedia.org/wiki/Data_URI_scheme) with the image contents itself. I recommend converting an image to a data URI, as that will make it load instantly, instead of having to make a new HTTP request for each icon to be loaded. You can use [Base64 Image Encoder](https://www.base64-image.de/) to easily convert an image into a data URI to paste into this field.

## Supported sites
The script currently runs on the following pages. Feel free to request your favorite website to be added to this list.
- Steam Store (Game pages)
- Hookshot Media (Game pages, news, reviews, features, guides)
  - Nintendo Life 
  - Push Square
  - Pure Xbox
- More to come

## Built-in search engines
- Startpage
- Google
- Metacritic
- OpenCritic
- eBay.com
- eBay UK

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