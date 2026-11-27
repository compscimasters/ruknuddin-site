# Publishing www.ruknuddin.com for free (GitHub Pages)

No web hosting and no payment card needed. GitHub Pages hosts the site for free and lets it use your own domain, with free HTTPS.

## 1. Put the files on GitHub
1. Sign in at github.com (a free account is enough).
2. Create a new **public** repository, for example `ruknuddin-site`.
3. Click **Add file → Upload files** and upload `index.html` and `CNAME` (from this folder). Commit.

## 2. Turn on GitHub Pages
1. In the repository go to **Settings → Pages**.
2. Under *Build and deployment*: Source = **Deploy from a branch**, Branch = **main**, folder = **/ (root)**. Save.
3. Under *Custom domain* you should see `www.ruknuddin.com` (it comes from the CNAME file). If not, type it and save.

## 3. Point the domain to GitHub (at your domain registrar)
Log in where ruknuddin.com was bought (the place that currently forwards it to Google Sites).

1. **Remove the current forwarding / redirect** to sites.google.com.
2. Add these DNS records:

| Type  | Name / Host | Value                     |
|-------|-------------|---------------------------|
| A     | @           | 185.199.108.153           |
| A     | @           | 185.199.109.153           |
| A     | @           | 185.199.110.153           |
| A     | @           | 185.199.111.153           |
| CNAME | www         | YOUR-GITHUB-USERNAME.github.io |

3. Wait for DNS to update (usually under an hour, sometimes up to 24 hours).
4. Back in **Settings → Pages**, tick **Enforce HTTPS** once it becomes available.

Both `ruknuddin.com` and `www.ruknuddin.com` will then open the new site.

## Updating the site later
Edit `index.html` on GitHub (pencil icon) and commit. Changes go live in a minute or two.

## Note
The Google Site (sites.google.com/view/compscimaster) stays as it is. The new site links to its pages for notes, papers, recordings and class portals, so those keep working with no extra effort.
