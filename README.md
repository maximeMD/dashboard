﻿# Dashboard

![screenshot](screenshot.png "screenshot")


Dashboard is just that - a dashboard. It's inspired by [SUI](https://github.com/jeroenpardon/sui) and has all the same features as SUI.

## Features

So what makes this thing better than SUI?

- "Display URL" functionality, in case the URL you want to show is different than the URL you want to be redirected to
- Theming through JSON
- Search providers customizable through JSON (SUI has them both in a JSON and hardcoded)

## Installation
Getting Dashboard to run is fairly simple:

    git clone https://github.com/phntxx/dashboard.git
    cd dashboard
    yarn
    yarn start

Alternatively, if you want to get static files, simply run:

    git clone https://github.com/phntxx/dashboard.git
    cd dashboard
    yarn
    yarn build
and then put the files in the build-folder onto your web server.
## Customization
Dashboard is designed to be customizable. Everything is handled using four .json-files, which can be found at /src/components/data

### Applications
To add an application, append the following to applications.json or simply edit one of the examples given.

```
{
	"name": "[Name of the Application]",
	"displayURL": "[URL you want to show]",
	"URL": "[URL to redirect to]",
	"icon": "[Icon code]"
}
...
```

   To find icons, simply go to the [Material Design Icon Library](https://material.io/icons/) and copy one of the codes for an icon there.

### Bookmarks

To add an bookmark, append the following to bookmarks.json or simply edit one of the examples given.

```
{
	"name": "[Category name]",
	"items": [
		{
		"name": "[Bookmark name]",
		"url": "[URL to redirect to]"
		},
		{
		"name": "[Bookmark name]",
		"url": "[URL to redirect to]"
		},
		{
		"name": "[Bookmark name]",
		"url": "[URL to redirect to]"
		}
		...
	]
},
...
```

### Theming:
Dashboard also supports themes with the help of a simple JSON-file: themes.json. To add a theme, append the following to themes.json:

```
{
	"label": "[Theme Name]",
	"value": [Number of the theme],
	"mainColor": "[Main Color as 6-character hex code]",
	"accentColor": "[Accent Color as 6-character hex code]",
	"backgroundColor": "[Background Color as 6-character hex code]"
}
```

### Search Providers:
The searchbar on the top supports shortcuts like "/so", just as SUI does. To add one of your own, simply append the following to search.json

```
{
	"name":"[Name of the website]",
	"url":"[Link that processes searches on that website]",
	"prefix":"[a custom prefix]"
},
```
