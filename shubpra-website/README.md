# shubpra.com website

A single-page website for Shubpra Group and Ekatra, built to be hosted free on GitHub Pages.

## What's in this folder

| File | Purpose |
| --- | --- |
| `index.html` | The whole website (styles and script included) |
| `404.html` | Page shown for broken links |
| `CNAME` | Tells GitHub Pages to use `shubpra.com` |
| `.nojekyll` | Tells GitHub to publish the files exactly as they are |
| `robots.txt`, `sitemap.xml` | Help Google find and index the site |
| `assets/` | Logos, favicon, app icon and the link-preview image (`og-image.png`) shown when someone shares the link on WhatsApp |

## Put it online (about 15 minutes)

### 1. Create the repository
1. In the **shubpra-group** GitHub organisation, create a new repository named **`shubpra-group.github.io`**.
2. Make it **Public**. GitHub Pages is free only for public repositories on the free plan.
3. Upload **everything in this folder**, including the hidden `.nojekyll` file and the `assets` folder, to the `main` branch.

### 2. Turn on GitHub Pages
1. In the repository, go to **Settings → Pages**.
2. Under **Build and deployment**, choose **Deploy from a branch**, branch **main**, folder **/ (root)**, and save.
3. Under **Custom domain**, enter `shubpra.com` and save. (The `CNAME` file already contains it.)

### 3. Point shubpra.com to GitHub (GoDaddy DNS)
1. **Delete** the existing **A** record for `@` that says **WebsiteBuilder Site**.
2. **Add four A records**, all with Name `@`:
   - `185.199.108.153`
   - `185.199.109.153`
   - `185.199.110.153`
   - `185.199.111.153`
3. **Edit** the `www` **CNAME** record so its value is `shubpra-group.github.io`.
4. **Don't touch** the MX, TXT (SPF, DMARC, DKIM, Google verification) or NS records. Your email keeps working.

### 4. Turn on HTTPS
Wait for the DNS change (often under an hour). Then, in **Settings → Pages**, tick **Enforce HTTPS** once the option becomes available.

### 5. Protect the domain (recommended)
In the **organisation** settings, go to **Pages → Add a verified domain**, add `shubpra.com`, and create the TXT record GitHub shows in GoDaddy. This stops anyone else from using your domain on GitHub Pages.

## Early access form

The form works straight away: when someone submits it, their email app opens with their details filled in, addressed to both of you.

To receive requests directly, without the visitor's email app:
1. Create a free form at **formspree.io** using `prathamesh.kasar@shubpra.com`.
2. Copy its endpoint (it looks like `https://formspree.io/f/abcdwxyz`).
3. In `index.html`, find `formEndpoint: ""` near the bottom and paste it between the quotes.

Requests then arrive in your inbox, and visitors see a "Thanks, you're on the list" message.

## Easy edits

- **Text:** every section is plain HTML in `index.html`. Search for the words you want to change.
- **Contact email:** once you create a `hello@shubpra.com` Google Group, replace the two addresses in the Contact section and in `CONFIG.emails` near the bottom of `index.html`.
- **Team photos:** they load from your GitHub profile pictures. Change your GitHub photo and the site updates. If a photo can't load, your initials show instead.
- **Colours:** all colours are defined at the top of the `<style>` section (`--midnight`, `--ivory`, `--coral`, `--violet` and others).

## Check it works
- Open `https://shubpra.com` on your phone and laptop.
- Share the link in WhatsApp and check the preview image appears.
- Submit the early access form once as a test.
- Send yourself an email, to confirm email still works.
