---
date: 2021-01-02T00:19:23Z
hero_image: "/content/images/sarah-dorweiler-9Z1KRIfpBTM-unsplash.jpg"
title: Brief Intro To Webpack
author: Robert Thoreau

---
### What is it?

Webpack is a module bundler. It combines all of the modules in an application into one or more bundle(s) that an `index.html` file can reference.

### What problem does it solve?

Traditionally in a JavaScript application, JavaScript code would be separated into individual files that an `index.html` file would reference one by one. 

    <body>
      ...
      <script src="src/b.js"></script>
      <script src='src/c.js'></script>
      <script src='src/d.js'></script>
      <script src='src/e.js'></script>
      <script src='src/f.js'></script>
      <script src='src/a.js'></script>
    </body>

Not only is maintaining a list of script files in this way tedious and prone to errors, the order of script tags matters, If script `b.js` has a dependency on script `a.js` but is loaded first, things would stop working. Webpack solves this issue by intelligently creating a bundle that handles the ordering.