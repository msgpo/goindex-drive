
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
