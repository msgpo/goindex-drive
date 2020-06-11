This project aims to provide a better UI for Google's Drive function and allows to quickly index all your files. Cloudflare Workers allow you to write JavaScript which runs on all of Cloudflare's 150+ global data centers.

![GoIndex Drive](https://github.com/CHEF-KOCH/goindex-drive/blob/master/Logo/go-drive-logo.gif?raw=true)


### Main Features
* Choose from a Light or Dark Themes main theme
* Choose from multiple colours for your borders
* Search function
* Media Playback for e.g. mp4 files without downloading them first.
* Works with GDrive/ShareDrive (prev. known as TeamDrive)


### To-do
- [ ] H.265/AV1 playable files
- [ ] Automatically fetch subtitles
- [x] Display srt subtitles
- [ ] Sort function via three-dot (or hamburger) menu.
- [ ] URL encode the download link
- [x] [Fix Apostrophe (') in file names (throws an error)](https://github.com/kulokenci/goindex-drive/issues/17)
- [ ] Grab all download links in a directory
- [x] Correct "How to use instructions"
- [ ] Online PDF, EPUB reader
- [ ] No directory-level password protection (because it's useless for public shared folder)
- [x] Add support for Support Http Basic Auth
- [ ] Image viewer should not require opening new page
- [x] Support multiple drives (personal & team) without changing server's code
- [x] Remove useless icon in the right corner which points to the outdated source
- [x] Integrate a working search function
- [ ] Improve search function, real-time search and filter options


### OLD method

<details>
  <summary>Spoiler warning</summary>

  1. Open [https://gencode.ve.workers.dev/](https://gencode.ve.workers.dev/).
  2. If you want to deploy main drive leave the option ROOT as it is. But if you want to deploy your Team Drive/Shared Drive/Folder then copy the ID and replace it with ROOT.
  3. Click on the "GET AUTH CODE" button (_big fat blue button in the left corner_). It will open the Google Website where you select your Google Drive Account. Once you're done copy & paste the code you got back into `Paste auth code in here` (it's the first empty line on the install.kenci.workers.dev website).
  4. Fill in other all (_optional_) parameters on the `install.kenci.workers.dev`. Once you pressed `BUILD NOW!` it will generate your configure file for Cloudflare Workers.
  5. Copy the given code via `COPY ALL` button and build your [Cloudflare Workers](https://workers.cloudflare.com) serverless application.
  6. Find Workers and Open it, then create your sub-domain or continue if already done. Select the `Free Plan`, then click on `Create a Worker`. (_Optional_) You can rename the workers at top of the page. Now paste the code you copied earlier. Click on `Save and Deploy`.
  7. (_optional_) You can change the configuration at any time under you Cloudlare workers application, make sure once you changed something to press `Save and Deploy`.

</details>

### How to deploy via rclone
1. Install [rclone](https://github.com/rclone/rclone) software locally.
2. Follow [https://rclone.org/drive/](https://rclone.org/drive/) and bind it to your drive.
3. Execute the `commandrclone config file` to find the file `rclone.conf path`.
4. Open `rclone.conf`,find the configuration `root_folder_id` and `refresh_token`.
5. Download `index.js` in [https://github.com/CHEF-KOCH/goindex-drive/blob/master/src/worker/index.js](https://github.com/CHEF-KOCH/goindex-drive/blob/master/src/worker/index.js) and fill in root and refresh_token.
6. Deploy the code to [Cloudflare Workers](https://workers.cloudflare.com).
7. (_optional_) Check the [video demo](https://www.youtube.com/watch?v=8WMddzVX1Dw).


### How to use Share Drive (previously known as TeamDrive) instead of your normal Drive?
* Copy your shared drive ID `DriveURL/drive/folders/<unique-ID>` (example: `1ffgFstW0fotDfDNlU9fyNiEstrWy3b6s` the [random folder ID](https://pirate.london/g-suite-team-drive-sharing-yes-you-can-not-you-cant-yes-you-can-db0a4e3e6220) is your folder) and set it as your root dir.
* **DO NOT** copy the whole URL `DriveURL/drive/folders/` you only need the specific and unique folder ID!


### Screenshots

**Dark Theme**
![Dark Theme](https://raw.githubusercontent.com/kulokenci/goindex-drive/master/screenshot/material-dark.png)


### Credits
* Based on the [original project](https://github.com/donwa/goindex) (_now offline_)
* Forked from [kulokenci/goindex-drive](https://github.com/kulokenci/goindex-drive)
* Source: [maple3142](https://github.com/maple3142/GDIndex)
* Source: [yanzai](https://github.com/yanzai/goindex)
* Search Function: [MakItWeb](https://makitweb.com/jquery-search-text-in-the-element-with-contains-selector/)
* Search Base: [w3Schools](https://www.w3schools.com/howto/tryit.asp?filename=tryhow_js_filter_list)
* Source: [ParveenBhadooOfficial](https://github.com/ParveenBhadooOfficial/Bhadoo-Drive-Index/blob/master/README.md)
* Video: [INDIA - Create Google Drive Index using CloudFlare Workers](https://www.youtube.com/watch?v=8WMddzVX1Dw)


### License
The project is forked from [kulokenci/goindex-drive](https://github.com/kulokenci/goindex-drive) and re-licensed under the [MIT license](https://github.com/CHEF-KOCH/goindex-drive/blob/master/LICENSE).

