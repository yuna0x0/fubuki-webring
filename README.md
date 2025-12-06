# Fubuki Webring

A webring for cozy blogs and personal websites. Powered by [ringfairy](https://github.com/k3rs3d/ringfairy).

## How to join the webring

1. Choose a unique `slug` for your site (e.g., `yuna0x0`).
2. Clone or fork this repository, then edit the `websites.json` file to add your site in the following format:

```json
{
  "name": "your name",
  "slug": "your chosen slug",
  "about": "a short description of you or your website.",
  "url": "https://example.com",
  "owner": "your.email@example.com",
  "rss": "https://example.com/rss.xml", // optional
  "misc": {
    "button": "https://example.com/88x31.webp", // 88x31 button image URL (optional, but recommended)
    "twtxt": "https://example.com/twtxt.txt" // twtxt feed URL (optional)
  }
}
```

3. Commit your changes and create a pull request on [GitHub](https://github.com/yuna0x0/fubuki-webring) or [Codeberg](https://codeberg.org/yuna0x0/fubuki-webring). (Repositories are mirrored between the two platforms.)
4. After your PR is merged, add the follow HTML snippet (or customize it as you like) to your website, replacing `{your-slug}` with your chosen slug:

```html
<a href="https://webring.fbk.moe/{your-slug}/previous">&larr;</a>
<a href="https://webring.fbk.moe">Fubuki Webring</a>
<a href="https://webring.fbk.moe/{your-slug}/next">&rarr;</a>
```

## Build

1. Install [ringfairy](https://github.com/k3rs3d/ringfairy) using Cargo:

```bash
cargo install --git https://github.com/k3rs3d/ringfairy.git
```

2. Clone this repository:

```bash
# GitHub
git clone https://github.com/yuna0x0/fubuki-webring.git
# or Codeberg
git clone https://codeberg.org/yuna0x0/fubuki-webring.git

cd fubuki-webring
```

2. Build the webring site:

```bash
ringfairy
```

This will generate the static site in the `webring` directory.

## License

This webring uses [ringfairy](https://github.com/k3rs3d/ringfairy) and is licensed under the [GNU General Public License v3.0](LICENSE).
