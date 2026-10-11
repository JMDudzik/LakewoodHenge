# Lakewoodhenge

The website for [lakewoodhenge.com](https://lakewoodhenge.com): the evenings when the setting sun lines up with the streets of Lakewood, Ohio.

It is a plain static site, hosted free on GitHub Pages. There is no build step.

| File | What it is |
| --- | --- |
| `index.html` | The page |
| `styles.css` | The styling |

To preview, double-click `index.html` to open it in a browser.

## Publishing

### 1. Push the files to GitHub

Commit the changes and push to the `main` branch of `JMDudzik/LakewoodHenge` (in GitHub Desktop: write a summary, **Commit to main**, then **Push origin**).

### 2. Turn on GitHub Pages (one time)

1. On GitHub, open the repository, then **Settings → Pages**.
2. Under **Build and deployment**, set **Source** to **Deploy from a branch**.
3. Set **Branch** to `main` and the folder to `/ (root)`, then **Save**.

After a minute or two the site is live at <https://jmdudzik.github.io/LakewoodHenge/>. The repository must be public for Pages to work on a free account.

From here on, every push to `main` republishes the site automatically.

### 3. Point lakewoodhenge.com at it (one time)

At the domain registrar, in the DNS settings for lakewoodhenge.com, add:

| Type | Name / Host | Value |
| --- | --- | --- |
| A | `@` | `185.199.108.153` |
| A | `@` | `185.199.109.153` |
| A | `@` | `185.199.110.153` |
| A | `@` | `185.199.111.153` |
| CNAME | `www` | `jmdudzik.github.io` |

Remove any existing A records or parking/forwarding entries for `@` and `www` that the registrar added by default.

Then on GitHub, in **Settings → Pages**:

1. Enter `lakewoodhenge.com` under **Custom domain** and **Save**. GitHub adds a `CNAME` file to the repository, so pull (GitHub Desktop: **Fetch origin**, then **Pull**) before making the next local change.
2. Wait for the DNS check to pass. This can take anywhere from a few minutes to a day.
3. Tick **Enforce HTTPS** once it becomes available.
