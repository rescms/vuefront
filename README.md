# VueFront Core

> “Simple can be harder than complex: You have to work hard to get your thinking clean to make it simple. But it’s worth it in the end because once you get there, you can move mountains.” ~ Steve Jobs

Vue powered agnostic frontend for your old fashioned Blog and Ecommerce site.

## What does this project do?
Turn your Wordpress, OpenCart, Magenta, Shopify or any other blog/store into an SPA and PWA with Vue.js in 3 simple steps.

## Why is this project useful?
You want to try new technology, outrun your competition and just provide a better user experiance, but not ready to invest thousands of dollars? Then try VueFront. Its easy to setup, test and run. 

- You get a shiny new Web APP.
- You get to keep your current CMS admin panel.
- You can always switch back to your old site. 


> Give it a try, what do you have to loose? 

## How do I get started? (development)

1. Install VueFront [CMS Connect App](http://localhost:8080/cms/) on your site and copy the CMS Connect URL.
2. Install VueFront app. (requires node.js >= 8, git, and yarn)

```bash
# Create VueFront app. replace <project-name> with vuefront
yarn create vuefront-app <project-name>
# OR npx create-vuefront-app <project-name>

yarn dev
```

## Switch to production
1. build your App
```bash
# build the app
yarn build
```

2. Copy the contents of your app from `/dist`  to your root folder of your CMS where it is hosted.

3. Configure your hosting to load `index.html` first. This can be a bit tricky. 

For OpenCart CMS you can use this:

- Apache

```apache
# for VeuFront to work you need to load index.html before any other index file
DirectoryIndex index.html index.php

```

- Nginx
```nginx
# for VeuFront to work you need to load index.html before any other index file
index index.html index.php;

# when visiting any other url, it should forward to the root index.html file
location / {
    try_files $uri $uri/ /index.html;
}
```
