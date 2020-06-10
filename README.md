This project aims to provide a better UI for Google's Drive function and allows to quickly index all your files.

![GoIndex Drive](https://github.com/CHEF-KOCH/goindex-drive/blob/master/Logo/go-drive-logo.gif?raw=true)


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
- [ ] Grab all download links in a directory
- [x] Correct "How to use instructions"


### Original Source
Based on the [original project](https://github.com/donwa/goindex) (_now offline_) & forked from [kulokenci/goindex-drive](https://github.com/kulokenci/goindex-drive).


### How to use
1. Open [https://install.kenci.workers.dev/](https://install.kenci.workers.dev/).
2. Click on the "GET AUTH CODE" button (_big fat blue button in the left corner_). It will open the Google Website where you select your Google Drive Account. Once you're done copy & paste the code you got back into `Paste auth code in here` (it's the first empty line on the install.kenci.workers.dev website).
3. Fill in other all (_optional_) parameters on the `install.kenci.workers.dev`. Once you pressed `BUILD NOW!` it will generate your configure file for Cloudflare Workers.
4. Copy the given code via `COPY ALL` button and build your [Cloudflare Workers](https://workers.cloudflare.com) serverless application.
5. (_optional_) You can change the configuration at any time under you Cloudlare workers application, make sure once you changed something to press `Save and Deploy`.


### How to use Share Drive (previously known as TeamDrive) instead of your normal Drive?
* Copy your shared drive ID `DriveURL/drive/u/0/folders/<unique-ID>` (example: `https://drive.google.com/drive/u/0/folders/1ffgFstW0fotDfDNlU9fyNiEstrWy3b6s` the [random folder ID](https://pirate.london/g-suite-team-drive-sharing-yes-you-can-not-you-cant-yes-you-can-db0a4e3e6220) is your folder) and set it as your root dir.


### Screenshots
**Light Theme**
![Light Theme](https://raw.githubusercontent.com/kulokenci/goindex-drive/master/screenshot/material-light.png)

**Dark Theme**
![Dark Theme](https://raw.githubusercontent.com/kulokenci/goindex-drive/master/screenshot/material-dark.png)


### License
The project is forked from [kulokenci/goindex-drive](https://github.com/kulokenci/goindex-drive) and re-licensed under the [MIT license](https://github.com/CHEF-KOCH/goindex-drive/blob/master/LICENSE).
