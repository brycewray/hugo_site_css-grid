# Hugo starter set

This is a starter set for the [Hugo](https://gohugo.io) [static site generator (SSG)](https://staticgen.com), based on my website at [brycewray.com](https://brycewray.com).

See the [online demo](https://hugo-site-css-grid.netlify.app/).

[![Netlify Status](https://api.netlify.com/api/v1/badges/dbf86fd7-5d17-4476-879d-8847b6213b50/deploy-status)](https://app.netlify.com/sites/hugo-site-css-grid/deploys)

## How to use

1. Clone this to a local repo.
2. Make appropriate changes to `config.toml` to conform to your site’s parameters.
3. Run `npm install` to load all the dependencies in `package.json`.
4. Once you have [installed Hugo](https://gohugo.io/getting-started/installing/), run `npm run start` from your terminal app. You can then view the site in [http://localhost:1313](http://localhost:1313) on your computer.
5. Read the sample posts and their Markdown files to see how everything works.
6. Edit the content to make it your own!
7. When ready, [deploy the site](https://gohugo.io/hosting-and-deployment/) to your chosen host. The `build` command is `npm run build`. (For local testing, you can use `npm run testbuild` to set the environment to `production`; see “What’s under the hood,” below.)


## What’s under the hood

For Hugo users unused to dealing with JavaScript from [npm](https://npmjs.org) plugins and dependencies, this repo may not be your cup of tea, and that’s perfectly understandable.* However, if you’re willing to take a trip to the npm Dark Side, it does offer some interesting add-on possibilities. (That said, Hugo’s single-binary, nearly-everything-out-of-the-box approach has served it well and is impressive.) In `package.json`, you’ll find dependencies that make possible the use of [PostCSS](https://postcss.org) and [Tailwind CSS](https://tailwindcss.com). (**Note**: Tailwind’s [built-in use](https://tailwindcss.com/docs/controlling-file-size) of [PurgeCSS](https://purgecss.com/) works **only** in a **production** environment—so, if you want to check that during local testing, use the `npm run testbuild` script in `package.json`.)

In addition, there’s:

- Lazy-loading of in-body images through use of [lazyload](https://github.com/verlok/vanilla-lazyload).
- Responsive images through Hugo’s [built-in image processing capabilities](https://gohugo.io/content-management/image-processing/), using code borrowed shamelessly (and, where necessary, adapted for later versions of Hugo) from Stereobooster’s “[Responsive images for Hugo](https://dev.to/stereobooster/responsive-images-for-hugo-dn9)” and Strict Panda’s “[Using Image Processing to Load Images in Hugo](https://blog.strict-panda.com/post/image-processing-media-queries/).” (The **real** site’s repo uses [Cloudinary](https://cloudinary.com) rather than having the images in the repo and processing them as such.)


\* If you don’t care for dealing with [npm](https://npmjs.org) plugins and dependencies, you may be interested in another Hugo repo, [hugo_solo](https://github.com/brycewray/hugo_solo), which offers the same lazy-loading and image processing **but** uses [SCSS](https://sass-lang.com/) [through Hugo Pipes](https://gohugo.io/hugo-pipes/scss-sass/) instead of Tailwind CSS and PostCSS.