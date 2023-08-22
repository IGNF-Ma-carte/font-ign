# Font-IGN
A set of icon font and SVG for use with GIS and spatial analysis tools

## Getting started

[Online examples]()

### Install

```javascript
npm install git+https://gitlab.com/ignf/macarte/font-ign.git 
```

Then you can access the fonts as node module inside the font-gis/public folder.
```javascript
import 'font-ign/public/font-ign.css'
```

### using Font-IGN

You can use Font-IGN as a font or as SVG symbols or images.

To use it in a web page, just add the css in your project.
```html
<link href="https://path/to/font-ign/public/font-ign.css" rel="stylesheet" />
```
Then use an inline element with a class prefixed with `fg-` to add a new icon.    
```html
<!-- prefix: fi - icon name: locate -->
<i class="fi-locate"></i>
<!-- using a <span> is more semantically correct but a little bit verbose. -->
<span class="fi-polygon"></span>
```
Or use it as an svg sprite (svg sprites are inlocated in the `./dist/font-ign.svg` file):    
```html
<svg class="font-ign fi-3x"><use xlink:href="path/to/font-ign/public/font-ign.svg#fg-polygon" /></svg>
```

## Contributing

Please use the [GitHub issue tracker](https://github.com/IGNF-Ma-carte/font-ign/issues) to ask for new features 
or create a pull request.    
Font is created from the files placed in the `./svg` folder, you only have to create a new file in this folder / subfolder.    
Icons must be 100x100px with a single path to fit the font correctly, only path fill color is used, other will be ignored (stroke size, etc.).    
Use the `./templates/template.svg` template to create a new icon.  
The new glyph will be referenced in the [font-ign.json]() file. You can add a theme and search tags 
(other fields will be filled automatically).

If you wan't to build the font and create the dist, use the build script (run `npm install` to install the dev dependencies before):
```console
npm run build
```
Use a local server (http://localhost:8181/) to see result on the page:
```console
npm start
```

## Licenses

Copyright (c) 2021 IGN-France
Font-IGN is free, open source, and GPL friendly. You can use it for commercial projects, open source projects, or really almost whatever you want. Read full Font-GIS license

* Font-GIS font is licensed under the SIL OFL 1.1 License
* Icons and SVG files are licensed under the CC BY 4.0 License
* Codes and all non font or icon files are licensed under the MIT License

Attribution is required by MIT, SIL OFL, and CC BY licenses. Font-GIS files already contain embedded comments with sufficient attribution, so you shouldn't need to do anything additional when using these files normally.
