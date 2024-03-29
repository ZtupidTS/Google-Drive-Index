<h1 align="center">Google Drive Index 🔥</h1> 

<p align="center">
<a href="https://github.com/sawankumar"><img alt="author" src="https://img.shields.io/badge/author-Sawan%20Kumar-red"/></a>
<a href="https://github.com/ellerbrock/open-source-badges/"><img alt="author" src="https://badges.frapsoft.com/os/v1/open-source.svg?v=103"/></a>
</p>

<hr>

> ## 🔥 A Google Drive Index built with Vue Running on CloudFlare ❤️ Workers.


![preview](https://raw.github.com/sawankumar/Google-Drive-Index/master/Sample.PNG)


> It allows you to deploy a "Google Drive Index" on CloudFlare Workers along with many extra features.
>
> By the way, instead of modify from GOIndex, this is a total rewrite.


## Features :-

-   Frontend is based on Vue.js
-   Image viewer doesn't require opening new page
-   Video player support subtitles(Currently only srt is supported)
-   Online PDF, EPUB reader
-   No directory-level password protection(.password)
-   Support Http Basic Auth
-   Support multiple drives(personal, team) without changing server's code

## Usage

### Simple and automatic way

Go [HERE](https://gdindex-code-builder.glitch.me/), and follow its instructions.

### Manual way

1. Install [rclone](https://rclone.org/)
2. Setup your Google Drive: https://rclone.org/drive/
3. Run `rclone config file` to find your `rclone.conf` location
4. Find `refresh_token` in your `rclone.conf`, and `root_folder_id` too(optionally).
5. Copy the content of [worker/dist/worker.js](worker/dist/worker.js) to CloudFlare Workers.
6. Fill `refresh_token`, `root_folder_id` and other options on the top of the script.
7. Deploy!

## Lite mode

This mode will serve a simple nginx-like directory listing, and it only work with one drive. `upload` will be ignored in this mode.

On the top of the script, change `lite: false` into `lite: true`, than thats all.

## Credits :heart:‍ 

* [maple3142](https://github.com/maple3142/GDIndex)
