This project aims to provide a better UI for Google's Drive function and allows to quickly index all your files. Cloudflare Workers allow you to write JavaScript which runs on all of Cloudflare's 150+ global data centers.

![GoIndex Drive](https://github.com/CHEF-KOCH/goindex-drive/blob/master/Logo/go-drive-logo.gif?raw=true)

## Table of Contents
* [Table of Contents](#table-of-contents)
  * [Main Features](#main-features)
  * [Requirements](#requirements)
  * [Supported formats](#supported-formats)
  * [To-do](#to-do)
* [Build Instructions](#build-instructions)
  * [Automatic deploy via Website](#automatic-deploy-via-website)
  * [Manually deploy via rclone](#manually-deploy-via-rclone)
  * [How to use Share Drive (previously known as TeamDrive) instead of your normal Drive?](#how-to-use-share-drive-previously-known-as-teamdrive-instead-of-your-normal-drive)
  * [Screenshot](#screenshot)
  * [Tutorial Guides for beginners](#tutorial-guides-for-beginners)
* [Credits](#credits)
* [License](#license)


### Main Features
* Choose from a Light or Dark (_default_) Themes main theme
* Choose from multiple borders colours
* Integrated Search function
* Playable Audio/Video files for e.g. mp4 files without the need to download them to preview it.
* Works with GDrive/ShareDrive (prev. known as TeamDrive)
* Multi-level Search within the team drive
* Basic Encryption support (_does not include rclone based encryption/decryption_)



### Requirements
* [Google Account](http://account.google.com/)
* [CloudFlare Account](https://workers.cloudflare.com/)
* [Google Indesx Source Code](https://github.com/CHEF-KOCH/goindex-drive)


### Supported formats

| Image, Audio, Video or Document   |      Format      |  Supported? |
|:----------:|:-------------:|:------:|
| Video | .asf | ✅ |
| Video | .avi | ✅ |
| Video | .flv | ✅ |
| Video | .mkv | ✅ |
| Video | .mov | ✅ |
| Video | .mp4 | ✅ |
| Video | .mpeg | ✅ |
| Video | .mpg | ✅ |
| Video | .rm | ✅ |
| Video | .rmvb | ✅ |
| Video | .ts | ✅ |
| Video | .webm | ✅ |
| Video | .wmv | ✅ |
| Audio | .flac | ✅ |
| Audio | .m4a | ✅ |
| Audio | .mp3 | ✅ |
| Audio | .ogg | ✅ |
| Audio | .wav | ✅ |
| Audio | AAC 2.0 based | ❌ |
| Document | .css | ✅ |
| Document | .go | ✅ |
| Document | .html | ✅ |
| Document | .java | ✅ |
| Document | .js | ✅ |
| Document | .json | ✅ |
| Document | .md | ✅ |
| Document | .pdf | ✅ |
| Document | .php | ✅ |
| Document | .sh | ✅ |
| Document | .txt | ✅ |
| Image | .bmp | ✅ |
| Image | .gif | ✅ |
| Image | .jpeg | ✅ |
| Image | .jpg | ✅ |
| Image | .png | ✅ |


### To-do
- [ ] A small button to grab all download links in a directory
- [ ] Automatically fetch subtitles
- [ ] Better error fallback page & debug log under files to see problems like rate limit, api limit coming from Google to know what's going on.
- [ ] Checksum support
- [ ] Display VirusTotal results for files below (135 MB _VTs limit for free accounts_)
- [ ] Display srt subtitles from /sub folders or same dir as video file
- [ ] Display uploader or his gmail to identify who uploaded which file
- [ ] Full oAuth support
- [ ] H.265/HEVC playable files
- [ ] Image viewer should not require opening new page
- [ ] Improve search function e.g. real-time search & filter options
- [ ] Sort function via three-dot (or hamburger) menu.
- [ ] URL encode the download link
- [ ] [JDownloader support](https://board.jdownloader.org/showthread.php?t=83613) including [logins](https://board.jdownloader.org/showthread.php?t=84669)
- [ ] epub support
- [x] Add Final / Beta branch
- [x] Add refresh tokens support
- [x] Add support for Support Http Basic Auth
- [x] Add the ability to add multiple share drives
- [x] Correct "How to use instructions"
- [x] Encrypted file storage
- [x] Integrate a working search function
- [x] Integrate multi-level search within the team drive
- [x] Mobile friendly
- [x] PDF support
- [x] Password protected home dir or entire drive
- [x] Remove all Chinese code/comments
- [x] Remove useless icon in the right corner which points to the outdated source
- [x] Support multiple drives (personal & team) without changing server's code
- [x] [Fix Apostrophe (') in file names (throws an error)](https://github.com/kulokenci/goindex-drive/issues/17)


## Build Instructions

### Automatic deploy via Website

Follow the instructions provided over [here](https://g-index.glitch.me) another mirror can be found over [here](https://gencode.ve.workers.dev).


### Manually deploy via rclone
1. Install [rclone](https://github.com/rclone/rclone) software locally.
2. Follow the gien instructions under [https://rclone.org/drive/](https://rclone.org/drive/) to bind a drive.
3. Execute the `commandrclone config file` to find the file `rclone.conf path`.
4. Open `rclone.conf`,find the configuration `root_folder_id` and `refresh_token`.
5. Download `index.js` in [https://github.com/CHEF-KOCH/goindex-drive/blob/master/Final/Search/index.js](https://github.com/CHEF-KOCH/goindex-drive/blob/master/Final/Search/index.js) and fill in root and refresh_token.
6. Deploy the code to [Cloudflare Workers](https://workers.cloudflare.com).



### How to use Share Drive (previously known as TeamDrive) instead of your normal Drive?
* Copy your shared drive ID `DriveURL/drive/folders/<unique-ID>` (example: `1ffgFstW0fotDfDNlU9fyNiEstrWy3b6s` the [random folder ID](https://pirate.london/g-suite-team-drive-sharing-yes-you-can-not-you-cant-yes-you-can-db0a4e3e6220) is your folder) and set it as your root dir.
* **DO NOT** copy the whole URL `DriveURL/drive/folders/` you only need the specific and unique folder ID!


### Screenshot

**Dark Theme**
![Dark Theme](https://raw.githubusercontent.com/kulokenci/goindex-drive/master/screenshot/material-dark.png)


### Tutorial Guides for beginners
* Check the [video demo](https://www.youtube.com/watch?v=8WMddzVX1Dw).
* Check the step-by-step guide over [here](https://telegra.ph/G-Index-DarkMode--MultiAuth--English--TD-Maker--Custom-Domainga-Tutorial-04-29).
* How do I just download files without previewing them? Simple, just remove `?a=view` or use the download button in the right corner.


## Credits
* Based on the [original project](https://github.com/donwa/goindex) (_now offline_)
* Forked from [kulokenci/goindex-drive](https://github.com/kulokenci/goindex-drive)
* Search Base: [w3Schools](https://www.w3schools.com/howto/tryit.asp?filename=tryhow_js_filter_list)
* Search Function: [MakItWeb](https://makitweb.com/jquery-search-text-in-the-element-with-contains-selector/)
* Source: [LeeluPradhan/G-Index](https://github.com/LeeluPradhan/G-Index), the Chinese code can be found over [here](https://github.com/yanzai/goindex)
* Source: [ParveenBhadooOfficial](https://github.com/ParveenBhadooOfficial/Bhadoo-Drive-Index/blob/master/README.md)
* Source: [maple3142](https://github.com/maple3142/GDIndex)
* Video: [INDIA - Create Google Drive Index using CloudFlare Workers](https://www.youtube.com/watch?v=8WMddzVX1Dw)


## License
This project is forked from [kulokenci/goindex-drive](https://github.com/kulokenci/goindex-drive) and re-licensed under the [MIT license](https://github.com/CHEF-KOCH/goindex-drive/blob/master/LICENSE).

