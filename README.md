
![GoIndex Drive](https://raw.githubusercontent.com/kulokenci/goindex-drive/master/go-drive-logo.png)


### Features
* Choose a Light or Dark Themes
* Select multiple colours you can pick from
* Search Function (currently only works in the root `/` dir)
* Media Playback
* Works with GDrive/[ShareDrive (TeamDrive)](https://github.com/kulokenci/goindex-drive/issues/19)


### To-do
* H.265/AV1 playable files
* Fetch subtitles
* Sort function
* URL encode the download link
* [Fix Apostrophe (') in file names (throws an error)](https://github.com/kulokenci/goindex-drive/issues/17)
* Correct "How to use instructions"
* Get all download links in a directory


### Source
Based on the [original project](https://github.com/donwa/goindex) (_down_) & [kulokenci/goindex-drive](https://github.com/kulokenci/goindex-drive).


### How to use
1. Open [https://install.kenci.workers.dev/](https://install.kenci.workers.dev/).
2. Click on the "GET AUTH CODE" button (left corner). It will open the Google Website to select an Google Drive Account, select your account and copy & paste the code into `Paste auth code in here`.
3. Fill in other (_optional_) parameters provided by `install.kenci.workers.dev`.
4. Deploy the code via [Cloudflare Workers](https://workers.cloudflare.com).


### How to use Share Drive (previously known as TeamDrive) instead of your normal Drive?
* Copy the shared drive ID `DriveURL/drive/u/0/folders/` **StringsOfHere** and set it as root dir.


### Screenshots
Light Theme
![Light Theme](https://raw.githubusercontent.com/kulokenci/goindex-drive/master/screenshot/material-light.png)

Dark Theme![Dark Theme](https://raw.githubusercontent.com/kulokenci/goindex-drive/master/screenshot/material-dark.png)


### License
The project is forked from [kulokenci/goindex-drive](https://github.com/kulokenci/goindex-drive) and re-licensed under the [MIT license](https://github.com/CHEF-KOCH/goindex-drive/blob/master/LICENSE).
