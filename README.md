This project aims to provide a better UI for Google's Drive function and allows to quickly index all your files.

![GoIndex Drive](https://github.com/CHEF-KOCH/goindex-drive/blob/master/Logo/go-drive-logo.png?raw=true)


### Main Features
* Choose from a Light or Dark Themes main theme
* Choose from multiple colours for your borders
* Search function (currently only works if you set root `/` dir)
* Media Playback for e.g. mp4 files without downloading them first.
* Works with GDrive/[ShareDrive (TeamDrive)](https://github.com/kulokenci/goindex-drive/issues/19)


### To-do
- [ ] H.265/AV1 playable files
- [ ] Automatically fetch subtitles
- [ ] Sort function via three-dot (or hamburger) menu.
- [ ] URL encode the download link
- [ ] [Fix Apostrophe (') in file names (throws an error)](https://github.com/kulokenci/goindex-drive/issues/17)
- [x] Correct "How to use instructions"
- [ ] Grab all download links in a directory


### Original Source
Based on the [original project](https://github.com/donwa/goindex) (_offline_) & [kulokenci/goindex-drive](https://github.com/kulokenci/goindex-drive).


### How to use
1. Open [https://install.kenci.workers.dev/](https://install.kenci.workers.dev/).
2. Click on the "GET AUTH CODE" button (left corner). It will open the Google Website to select an Google Drive Account, select your account and copy & paste the code into `Paste auth code in here`.
3. Fill in other (_optional_) parameters provided by `install.kenci.workers.dev`.
4. Deploy the code via [Cloudflare Workers](https://workers.cloudflare.com).


### How to use Share Drive (previously known as TeamDrive) instead of your normal Drive?
* Copy the shared drive ID `DriveURL/drive/u/0/folders/` **StringsOfHere** and set it as root dir.


### Screenshots
**Light Theme**
![Light Theme](https://raw.githubusercontent.com/kulokenci/goindex-drive/master/screenshot/material-light.png)

**Dark Theme**
![Dark Theme](https://raw.githubusercontent.com/kulokenci/goindex-drive/master/screenshot/material-dark.png)


### License
The project is forked from [kulokenci/goindex-drive](https://github.com/kulokenci/goindex-drive) and re-licensed under the [MIT license](https://github.com/CHEF-KOCH/goindex-drive/blob/master/LICENSE).
