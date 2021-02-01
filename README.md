# MMM-Mopidy-MPD

This module uses MPD (Music Player Deamon) to connect to your favorite music player, for example mopidy, 
and shows the current state of your music player on your magic mirror.
This is a fork from Tim Jongsma's MMM-MPD module. But after no respond from him due to pull request i decided to move this to a new module.

[![Platform](https://img.shields.io/badge/platform-MagicMirror-informational)](https://MagicMirror.builders)

## Example

![screenshot of MMM-Mopidy-MPD](https://user-images.githubusercontent.com/55058372/96780350-f34c3700-13ec-11eb-8c2d-536098016fef.jpg)

## Installation

In your terminal, go to your MagicMirror's Module folder:

````sh
cd ~/MagicMirror/modules
````

Clone this repository:

````sh
git clone https://github.com/coderpussy/MMM-Mopidy-MPD.git
````

Run npm install in the module folder:

````sh
npm install
````

Configure the module in your `config/config.js` file.

## Updating

If you want to update your MMM-MPD module to the latest version, use your terminal to go to your MMM-MPD module folder and type the following command:

````sh
git pull && npm install
````

If you haven't changed the modules, this should work without any problems.
Type `git status` to see your changes, if there are any, you can reset them with `git reset --hard`. After that, git pull should be possible.

## Using the module

To use this module, add it to the modules array in the `config/config.js` file:
````js
modules: [
	{
		module: "MMM-Mopidy-MPD",
		position: "top_right",	// This can be any of the regions.
		config: {
			// See 'Configuration options' for more information.
			hostname: "localhost",
			port: 6600
			
		}
	}
]
````

## Configuration options

The following properties can be configured:

| Option | Description
| ------ | -----------
| `hostname` | The hostname of the machine running the MPD server. <br><br> **Example:** `'192.168.0.10'` <br> **Default value:** `'localhost'`
| `port` | The port of the MPD server. <br><br> **Example:** `'6600` <br> **Default value:** `'6600'`
| `showPlaylist` | Show playlist or not <br><br> **Example:** `'true` <br> **Default value:** `'true'`
| `maxRows` | The number of songs comming up in your playlist which will be displayed. <br><br> **Example:** `'10` <br> **Default value:** `'10'`
| `fade` | Enable fading effect. <br><br> **Example:** `'true` <br> **Default value:** `'true'`
| `fadePoint` | The point where the playlist starts to fade. <br><br> **Example:** `'0.3` <br> **Default value:** `'0.3'`

### Displaying the MMM-MPD module

Stop and start your Magic Mirror (your exact method may vary)

````sh
pm2 restart mm
````