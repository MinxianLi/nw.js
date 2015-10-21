## node-webkit is renamed NW.js

[![Gitter](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/nwjs/nw.js?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)  
Official site: http://nwjs.io  
[Announcement](https://groups.google.com/d/msg/nwjs-general/V1FhvfaFIzQ/720xKVd0jNkJ)  
## Introduction

NW.js is an app runtime based on `Chromium` and `node.js`. You can 
write native apps in HTML and JavaScript with NW.js. It also lets you
call Node.js modules directly from the DOM and enables a new way of writing
native applications with all Web technologies.

It was created in the Intel Open Source Technology Center.

[Introduction to node-webkit (slides)](https://speakerdeck.com/u/zcbenz/p/node-webkit-app-runtime-based-on-chromium-and-node-dot-js)   
[Creating Desktop Applications With node-webkit](http://strongloop.com/strongblog/creating-desktop-applications-with-node-webkit/)     
[WebApp to DesktopApp with node-webkit (slides)](http://oldgeeksguide.github.io/presentations/html5devconf2013/wtod.html)  
[Essay on the history and internals of the project](http://yedingding.com/2014/08/01/node-webkit-intro-en.html)

## Features

* Apps written in modern HTML5, CSS3, JS and WebGL.
* Complete support for [Node.js APIs](http://nodejs.org/api/) and all its [third party modules](https://npmjs.org).
* Good performance: Node and WebKit run in the same thread: Function calls are made straightforward; objects are in the same heap and can just reference each other;
* Easy to package and distribute apps.
* Available on Linux, Mac OS X and Windows

## Downloads
* **v0.12.3:** (Jul 31, 2015, based off of IO.js v1.2.0, Chromium 41.0.2272.76): [release notes](https://groups.google.com/d/msg/nwjs-general/hhXCS4aXGV0/TUQmcu5XDwAJ)  
 * Linux: [32bit](http://dl.nwjs.io/v0.12.3/nwjs-v0.12.3-linux-ia32.tar.gz) / [64bit](http://dl.nwjs.io/v0.12.3/nwjs-v0.12.3-linux-x64.tar.gz)
 * Windows: [32bit](http://dl.nwjs.io/v0.12.3/nwjs-v0.12.3-win-ia32.zip) / [64bit](http://dl.nwjs.io/v0.12.3/nwjs-v0.12.3-win-x64.zip)
 * Mac 10.7+: [32bit](http://dl.nwjs.io/v0.12.3/nwjs-v0.12.3-osx-ia32.zip) / [64bit](http://dl.nwjs.io/v0.12.3/nwjs-v0.12.3-osx-x64.zip)

* **v0.13.0-alpha2:** (Jun 23, 2015, based off of IO.js v1.5.1, Chromium 43.0.2357.45): [release notes](https://groups.google.com/d/msg/nwjs-general/zeC6SedUSFY/BlumrYJeVHYJ)  
 **NOTE** You might want the **SDK build**. Please read the release notes  
 * Linux: [32bit](http://dl.nwjs.io/v0.13.0/alpha2/nwjs-v0.13.0-alpha2-linux-ia32.tar.gz) / [64bit](http://dl.nwjs.io/v0.13.0/alpha2/nwjs-v0.13.0-alpha2-linux-x64.tar.gz)
 * Windows: [32bit](http://dl.nwjs.io/v0.13.0/alpha2/nwjs-v0.13.0-alpha2-win-ia32.zip) / [64bit](http://dl.nwjs.io/v0.13.0/alpha2/nwjs-v0.13.0-alpha2-win-x64.zip)
 * Mac 10.7+: [32bit](http://dl.nwjs.io/v0.13.0/alpha2/nwjs-v0.13.0-alpha2-osx-ia32.zip) / [64bit](http://dl.nwjs.io/v0.13.0/alpha2/nwjs-v0.13.0-alpha2-osx-x64.zip)

* **0.8.6:** (Apr 18, 2014, based off of Node v0.10.22, Chrome 30.0.1599.66) **If your native Node module works only with Node v0.10, then you should use node-webkit v0.8.x, which is also a maintained branch. [More info](https://groups.google.com/d/msg/nwjs-general/2OJ1cEMPLlA/09BvpTagSA0J)**  
[release notes](https://groups.google.com/d/msg/nwjs-general/CLPkgfV-i7s/hwkkQuJ1kngJ)

 * Linux: [32bit](http://dl.node-webkit.org/v0.8.6/node-webkit-v0.8.6-linux-ia32.tar.gz) / [64bit](http://dl.node-webkit.org/v0.8.6/node-webkit-v0.8.6-linux-x64.tar.gz)
 * Windows: [win32](http://dl.node-webkit.org/v0.8.6/node-webkit-v0.8.6-win-ia32.zip)
 * Mac: [32bit, 10.7+](http://dl.node-webkit.org/v0.8.6/node-webkit-v0.8.6-osx-ia32.zip)

* **latest live build**: git tip version; build triggered from every git commit: http://dl.nwjs.io/live-build/

* [Previous versions](https://github.com/rogerwang/node-webkit/wiki/Downloads-of-old-versions)

###Demos and real apps
You may also be interested in [our demos repository](https://github.com/zcbenz/nw-sample-apps) and the [List of apps and companies using nw.js](https://github.com/nwjs/nw.js/wiki/List-of-apps-and-companies-using-nw.js).

## Quick Start

Create `index.html`:

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Hello World!</title>
  </head>
  <body>
    <h1>Hello World!</h1>
    We are using node.js <script>document.write(process.version)</script>.
  </body>
</html>
```

Create `package.json`:

```json
{
  "name": "nw-demo",
  "version": "0.0.1",
  "main": "index.html"
}
```

Run:  
```bash
$ /path/to/nw .  (suppose the current directory contains 'package.json')
```

Note: on Windows, you can drag the folder containing `package.json` to `nw.exe` to open it.

Note: on OSX, the executable binary is in a hidden directory within the .app file. To run node-webkit on OSX, type:  
`/path/to/nwjs.app/Contents/MacOS/nwjs .` *(suppose the current directory contains 'package.json')*   

## Documents

For more information on how to write/package/run apps, see:

* [How to run apps](https://github.com/rogerwang/node-webkit/wiki/How-to-run-apps)
* [How to package and distribute your apps](https://github.com/rogerwang/node-webkit/wiki/How-to-package-and-distribute-your-apps)
* [How to use Node.js modules in node-webkit](https://github.com/rogerwang/node-webkit/wiki/Using-Node-modules)

And our [Wiki](https://github.com/rogerwang/node-webkit/wiki) for much more.

## Community

We use the [google group](https://groups.google.com/d/forum/nwjs-general) as
our mailing list (use English only). Subscribe via [nwjs-general+subscribe@googlegroups.com](mailto:nwjs-general+subscribe@googlegroups.com).

*NOTE*: Links to the old google group (e.g. `https://groups.google.com/forum/#!msg/node-webkit/doRWZ07LgWQ/4fheV8FF8zsJ`) that are no more working can be fixed by replacing `node-webkit` with `nwjs-general` (e.g `https://groups.google.com/forum/#!msg/nwjs-general/doRWZ07LgWQ/4fheV8FF8zsJ`).

Issues are being tracked here on GitHub.

## License

`node-webkit`'s code in this repo uses the MIT license, see our `LICENSE` file. To redistribute the binary, see [How to package and distribute your apps](https://github.com/rogerwang/node-webkit/wiki/How-to-package-and-distribute-your-apps)

## Sponsors

The work is being sponsored by:  
* [Intel](http://www.intel.com)
* [Gnor Tech](http://gnor.net)




-------------------------------------Minxian----------------------------------------------------------------------------
Refer: http://tutorialzine.com/2015/01/your-first-node-webkit-app/

Creating Your First Desktop App With HTML, JS and Node-WebKit

 Danny Markov January 7th, 2015

Download   
These days you can do pretty much anything with JavaScript and HTML. Thanks to Node-WebKit, we can even create desktop applications that feel native, and have full access to every part of the operating system. In this short tutorial, we will show you how to create a simple desktop application using Node-WebKit, which combines jQuery and a few Node.js modules.

Node-WebKit is a combination of Node.js and an embedded WebKit browser. The JavaScript code that you write is executed in a special environment and has access to both standard browser APIs and Node.js. Sounds interesting? Keep reading!

Update (15th Jan 2015) – Just after a week of publishing this tutorial, node-webkit was renamed to NW.js. For now, this tutorial is perfectly compatible with it. In the future we might update it if there are any changes.
100 Must Know jQuery Tips and Tricks
jQuery Trickshot is our free book, filled with kick-ass tips and tricks for jQuery that every developer should know.

DOWNLOAD IT
Installing Node-WebKit

For developing applications, you will need to download the node-webkit executable, and call it from your terminal when you want to run your code. (Later you can package everything in a single program so your users can only click an icon to start it).

Head over to the project page and download the executable that is built for your operating system. Extract the archive somewhere on your computer. To start it, you need to do this in your terminal:

# If you are on linux/osx

/path/to/node-webkit/nw /your/project/folder

# If you are on windows

C:\path\to\node-webkit\nw.exe C:\your\project\folder

# (the paths are only for illustrative purposes, any folder will do)
This will open a new node-webkit window and print a bunch of debug messages in your terminal.

You can optionally add the extracted node-webkit folder to your PATH, so that it is available as the nw command from your terminal.

Your First Application

There is a Download button near the top of this article. Click it and get a zip with a sample app that we prepared for you. It fetches the most recent articles on Tutorialzine from our RSS feed and turns them into a cool looking 3D carousel using jQuery Flipster.

Directory Structure
Directory Structure

Once you extract it, you will see the files above. From here this looks like a standard static website. However, it won’t work if you simply double click index.html – it requires Node.js modules, which is invalid in a web browser. To run it, CD into this folder, and try running the app with this command:

/path/to/node-webkit/nw .
This will show our glorious desktop app.

Our node-webkit app
Our node-webkit app

How it was made

It all starts with the package.json file, which node-webkit looks up when starting. It describes what node-webkit should load and various parameters of the window.

package.json

{
  "name": "nw-app",
  "version": "1.0.0",
  "description": "",
  "main": "index.html",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "author": "",
  "window": {
    "toolbar": false,
    "width": 800,
    "height": 500
  },
  "license": "ISC",
  "dependencies": {
    "pretty-bytes": "^1.0.2"
  }
}
The window property in this file tells node-webkit to open a new window 800 by 500px and hide the toolbar. The file pointed to by the main property will be loaded. In our case this is index.html:

index.html

<!DOCTYPE html>
<html>
<head>

	<meta charset="utf-8">
	<meta name="viewport" content="width=device-width, initial-scale=1">

	<title>Tutorialzine Node-Webkit Experiment</title>

	<link rel="stylesheet" href="./css/jquery.flipster.min.css">
	<link rel="stylesheet" href="./css/styles.css">

</head>
<body>

	<div class="flipster">
		<ul>
			<!-- Tutorialzine's latest articles will show here -->
		</ul>
	</div>

	<p class="stats"></p>

	<script src="./js/jquery.min.js"></script>
	<script src="./js/jquery.flipster.min.js"></script>
	<script src="./js/script.js"></script>
</body>
</html>
And finally, here is our JavaScript file. This is where it gets interesting!

js/script.js

// Mixing jQuery and Node.js code in the same file? Yes please!

$(function(){


	// Display some statistic about this computer, using node's os module.

	var os = require('os');
	var prettyBytes = require('pretty-bytes');

	$('.stats').append('Number of cpu cores: <span>' + os.cpus().length + '</span>');
	$('.stats').append('Free memory: <span>' + prettyBytes(os.freemem())+ '</span>');

	// Node webkit's native UI library. We will need it for later
	var gui = require('nw.gui');


	// Fetch the recent posts on Tutorialzine

	var ul = $('.flipster ul');

	// The same-origin security policy doesn't apply to node-webkit, so we can
	// send ajax request to other sites. Let's fetch Tutorialzine's rss feed:

	$.get('http://feeds.feedburner.com/Tutorialzine', function(response){

		var rss = $(response);

		// Find all articles in the RSS feed:

		rss.find('item').each(function(){
			var item = $(this);
			
			var content = item.find('encoded').html().split('</a></div>')[0]+'</a></div>';
			var urlRegex = /(http|ftp|https):\/\/[\w\-_]+(\.[\w\-_]+)+([\w\-\.,@?^=%&amp;:/~\+#]*[\w\-\@?^=%&amp;/~\+#])?/g;

			// Fetch the first image of the article
			var imageSource = content.match(urlRegex)[1];


			// Create a li item for every article, and append it to the unordered list

			var li = $('<li><img /><a target="_blank"></a></li>');

			li.find('a')
				.attr('href', item.find('link').text())
				.text(item.find("title").text());

			li.find('img').attr('src', imageSource);

			li.appendTo(ul);

		});

		// Initialize the flipster plugin

		$('.flipster').flipster({
			style: 'carousel'
		});

		// When an article is clicked, open the page in the system default browser.
		// Otherwise it would open it in the node-webkit window which is not what we want.

		$('.flipster').on('click', 'a', function (e) {

			e.preventDefault();
			
			// Open URL with default browser.
			gui.Shell.openExternal(e.target.href);

		});

	});

});
Notice that we are accessing Tutorialzine’s RSS feed directly with jQuery, even though it is on a different domain. This is not possible in a browser, but Node-WebKit removes this limitation to make development of desktop applications easier.

Here are the node modules we’ve used:

Shell – A node webkit module that provides a collection of APIs that do desktop related jobs.
OS – The built-in Node.js OS module, which has a method that returns the amount of free system memory in bytes.
Pretty Bytes – Convert bytes to a human readable string: 1337 → 1.34 kB.
Our project also includes jQuery and the jQuery-flipster plugin, and that’s pretty much it!

Packaging and Distribution

You most certainly don’t want your users to go through the same steps in order to run you application. You wan’t to package it in a standalone program, and open it by simply double clicking it.

Packaging node-webkit apps for multiple operating systems takes a lot of work to do manually. But there are libraries that do this for you. We tried this npm module – https://github.com/mllrsohn/node-webkit-builder, and it worked pretty well.

The only disadvantage is that the executable files have a large size (they can easily hit 40-50mb) , because they pack a stripped down webkit browser and node.js together with your code and assets. This makes it rather impractical for small desktop apps (such as ours), but for larger apps it is worth a look.

Conclusion

Node-webkit is a powerful tool that opens a lot of doors to web developers. With it, you can easily create companion apps for your web services and build desktop clients which have full access to the users’s computer.

You can read more about node-webkit on their wiki.
