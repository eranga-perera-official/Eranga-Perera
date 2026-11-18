# Eranga Perera portfolio: site, dashboard and GitHub backend

```
index.html        the public site (reads content.json)
content.json      all text, projects and settings
admin/index.html  the dashboard (open yourdomain/admin/)
assets/           your images, CV and videos
```

## How it works
The dashboard is a page that talks to the GitHub API. When you click **Publish**, it commits `content.json` and any images you uploaded to your repository. GitHub Pages then redeploys the site, usually within a minute. There is no separate server to run or pay for.

## Setup
1. Create a **public** repository named `YOUR-USERNAME.github.io`.
2. Upload `index.html`, `content.json`, the `admin` folder and the `assets` folder.
3. Settings > Pages > Build and deployment > Source: **Deploy from a branch**, branch **main**, folder **/ (root)**.
4. Create a token: GitHub > Settings > Developer settings > Personal access tokens > **Fine-grained tokens** > Generate.
   - Repository access: **Only select repositories**, choose this one.
   - Permissions > Repository permissions > **Contents: Read and write**.
   - Set an expiry date.
5. Open `https://YOUR-USERNAME.github.io/admin/`, enter your username, repository, branch and token, then **Connect**.

## Security
- The token never leaves your browser except to api.github.com. Do not share it or paste it into chat.
- Anyone can open the `/admin/` page, but without your token they can change nothing.
- Use a token limited to this one repository. If it leaks, delete it in GitHub settings.
- Everything in the repository is public, including content.json. Do not put confidential Abans material, prices or client details in it.

## Notes
- Images are resized to 1600 px and saved as JPEG when uploaded from the dashboard.
- For videos, upload the file to `assets/` on GitHub and set the path in content.json.
- To change the CV, upload the PDF to `assets/` on GitHub and set its path under Site and contact.
- Use **Download backup** before big edits.
