# The Entertainment Co

GitHub Pages deployment is configured for **https://theentertainmentco.in**.

## Publish the website

1. Download [the prepared website ZIP](https://chatgpt.com/) from the ChatGPT conversation (filename: `theentertainmentco-website-source.zip`).
2. Open this repository and click **Add file → Upload files**.
3. Drag the downloaded ZIP into the upload area. Rename it to exactly **`website-source.zip`** before uploading if necessary.
4. Commit directly to `main`.
5. Open **Actions** to follow the build and deployment.

The `.github/workflows/deploy.yml` workflow extracts the ZIP, builds React/Vite, and deploys to GitHub Pages automatically. GitHub Pages publishing source in **Settings → Pages** must be **GitHub Actions**.

In **Settings → Pages → Custom domain**, keep **theentertainmentco.in**. DNS A records for the apex must point to GitHub Pages, and `www` can CNAME to `darpanjaiin.github.io`. Do not remove mail-related MX/TXT records.

The website source ZIP contains the application and binary image assets; uploading it once avoids GitHub's normal file-by-file upload process. The contact forms open the visitor's mail client; they are not backed by a server.

