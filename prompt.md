Help me edit .glb files using nodejs.

I'm working on a website using 11ty 3.0 static site generator. I have a following task:

In the site src/models folder there is a .glb file that contains a 3d model.
During the building of a site I need a building script to do the following:
1. Resize all the textures in .glb file to maximum width of 512px and convert them from png to jpg.
2. Change the Roughness of all materials in 3d model from 0.5 to 0.85
3. Save the edited .glb file in the same folder with a new name and return that name.

Here is package.json for my project:

{
  "name": "test.opaproject.ru",
  "version": "1.0.0",
  "description": "opa test project web site",
  "main": ".eleventy.js",
  "scripts": {
    "clean": "rimraf _site",
    "start": "ELEVENTY_ENV=dev npx @11ty/eleventy --serve",
    "build": "npx @11ty/eleventy",
    "debug": "DEBUG=Eleventy* npx @11ty/eleventy",
    "watch": "ELEVENTY_ENV=dev npx @11ty/eleventy --watch --incremental"
  },
  "keywords": [],
  "author": "",
  "license": "ISC",
  "type": "module",
  "dependencies": {
    "@11ty/eleventy": "^3.0.0",
    "@11ty/eleventy-img": "^5.0.0",
    "@11ty/eleventy-navigation": "^0.3.5",
    "@quasibit/eleventy-plugin-sitemap": "^2.2.0",
    "eleventy-plugin-gen-favicons": "^1.1.3",
    "eleventy-plugin-nesting-toc": "^1.3.0",
    "eleventy-plugin-time-to-read": "^1.3.0",
    "fast-glob": "^3.3.2",
    "html-minifier-terser": "^7.2.0",
    "lightningcss": "^1.27.0",
    "terser": "^5.34.1"
  }
}
