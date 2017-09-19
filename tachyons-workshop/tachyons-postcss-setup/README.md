# Tachyons PostCSS Setup

If you're a design control freak and you just want to change the shade of that blue or make that spacing a little smaller then this is the kit for you!

## How it works

This kit uses `PostCSS` to allow you to change the variables in Tachyons and outputs a new stylesheet.

To make the stylesheet run:

```sh
> npm install && npm run css-watch
```

This installs the dependencies and makes a `style.min.css` file you can include in your html (`watch` watches for any changes you make to the variables or other files in the `css` folder).

+ The `variables` are all in the `./css/_variables.css` file and you can change any of these to adjust the styles in tachyons
+ Add any extra styles you like in `./css/_custom.css`
+ `./css/index.css` imports everything (all the tachyons styles, variables and the custom css) and is the entry point for `postCSS` (think of it like `index.js` for a node server)

## What is PostCSS?

http://postcss.org/

PostCSS is a build tool that lets you write CSS with unusual syntax and can transform the output into normal css the browser can read (if you've used [SASS](http://sass-lang.com/) before it's similar).

Where PostCSS differs from SASS is that it's pluggable. You can add functionality to it with modules (one's you'd install with npm) to make it do whatever you like.

This setup uses a bunch of modules that let's us do cool things!

+ `postcss-import` allows you to import other css files
+ `autoprefixer` adds vendor prefixes like -webkit or -moz to your css for better browser support
+ `postcss-custom-media` can set media queries as variables
+ `postcss-custom-properties` allows you to use css variables e.g. var(--my-variable)
+ `postcss-clean` minifies the output css (i.e. removes all the spaces and comments)
