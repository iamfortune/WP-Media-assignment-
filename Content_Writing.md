# How to preload key requests on WordPress?
*Preload key requests are a popular warning in WordPress websites, they are a good way to optimize WordPress websites for speed.*

Preload is a process that hints on files and resources needed to load a webpage to browsers. Preload key requests means adding preload hints to a browser for those required resources.

Its important to note that linking resources is not substitute to the original files, you’d still need to keep the original linking of resources to enable them load on your website. 

Also preloaded files are downloadable at the same time by browsers while doing other tasks, so downloading them reduces load time on websites and has no impact on website speed.

## How to Preload key requests on WordPress

There are many ways of preloading resources, some of which include fonts, CSS and JavaScript files. In the section below, we will outline how to preload some specific resources and how to preload key requests using the [WP Rocket](https://wp-rocket.me/) and [Autoptimize.](https://autoptimize.com/)


## CSS

CSS resources can be preloaded by adding a `preload` attribute to the `rel` element, next we will define the resource type we want to preload.


    <link rel="preload" href="style.css" as="style">

In the code block above, we tried preloading our CSS resources, first we added the file we want to preload in our `href` and using the `as` attribute, we define our file type.

A similar syntax can be used to preload JavaScript resources, this can be using the code snippet below


    <link rel="preload" href="main.js" as="script">


## Fonts

Fonts are one of the most popular file types that come up in PageSpeed insight warnings, this is mostly caused by use of custom fonts with `@font-face`. `@font-face` fonts are usually not added to the html document in websites and so browsers are delayed while waiting for them to be parsed and downloaded. This delay can affect the speed of your website. To solve this, you can use the syntax below 


    <link rel="preload" href="font.woff" as="font" type="font/woff" crossorigin>

In the code snippet above, we used the `type` to indicate the resource type while `crossorigin` is used for preloading files from external websites. `@font-face` is used to load fonts on your websites. 


## Preloading Key requests using WordPress Plugins

You can preload key requests in WordPress by using some WordPress plugins like [WP Rocket](https://wp-rocket.me/). Plugins like this make it easier to load the necessary files for your website and fix the preload warnings. Most plugins do more than preload key requests, most include caching and optimization functionalities. 

## WP Rocket 

WP Rocket is a well known WordPress plugin for caching and optimization. With WP Rocket, you can solve preload key requests warning without installing a new plugin. To preload key requests in WordPress with WP Rocket, from your dashboard, go to **Settings > WP Rocket > Preload.** At the end of the page, you will see a preload fonts section. 
Inside the **Fonts to preload** text box, add all the links to the fonts you got from the preload key requests warning, once you’ve done this, click save. 

It’s important to note that WP Rocket only allows you to preload fonts on your site and not external sites. You can learn more about [WP Rocket here](https://webspeedtools.com/visit/wp-rocket/).

## Autoptimize

Autoptimize is a popular WordPress optimization plugin, it comes with a GUI and preload key requests option for WordPress websites. To preload key requests using Autoptimize, navigate to **Settings > Autoptimize > Extra** from your dashboard. In your box, input the links you get from your PageSpeed insights.

It’s important to note that you should separate multiple links with a comma. 

With the steps above, you can preload key requests on your WordPress site.
