# Atkinson Hyperlegible Next for Discord

A Vencord font theme using [Atkinson Hyperlegible Next](https://fonts.google.com/specimen/Atkinson+Hyperlegible+Next), designed for readability by the [Braille Institute](https://www.brailleinstitute.org/freefont/).

The theme sets Discord's `--font-primary` and `--font-display` variables to Atkinson Hyperlegible Next, and `--font-code` to [Atkinson Hyperlegible Mono](https://fonts.google.com/specimen/Atkinson+Hyperlegible+Mono) for inline code and code blocks. Both families load regular and italic styles from Google Fonts with weights 200 through 800; no system font installation or Vencord plugin is required.

## Install in Vencord

Choose one installation method to avoid loading duplicate copies.

### Online theme

1. Open Discord's **User Settings > Vencord > Themes > Online Themes**.
2. Paste this URL on its own line:

   ```text
   https://raw.githubusercontent.com/Today20092/DiscordAtkinsonHyperlegible/main/HyperLegibleFont.theme.css
   ```

3. Click outside the text box to save and apply it.

The filename stays the same so existing installations keep their URL. The online URL serves the version published on `main`; use the local method to test unpublished changes.

### Local theme

1. Download [HyperLegibleFont.theme.css](./HyperLegibleFont.theme.css), or use the file from your clone. Save the CSS itself, not the GitHub HTML page.
2. Open **User Settings > Vencord > Themes > Local Themes > Open Themes Folder**.
3. Copy the file into that folder, keeping the `.theme.css` extension.
4. Click **Load missing Themes**, then enable **Atkinson Hyperlegible Next**.

In Vencord's browser extension, use **Upload Theme** in Local Themes instead of opening a folder.

### QuickCSS alternative

Open **Edit QuickCSS**, paste the contents of the theme file, and enable **Enable Custom CSS** in Vencord settings. Keep the `@import` before all ordinary CSS rules, including any rules already in your QuickCSS file.

## Font sources and privacy

Google Fonts is the default for convenient installation. You can use Bunny Fonts or installed fonts instead. Choose one provider; adding several imports makes requests to several services rather than providing a reliable fallback.

### Bunny Fonts

[Bunny Fonts](https://fonts.bunny.net/about/) offers both Next and Mono and states that its font service has a no-logging policy. It is still an external service that your client connects to.

Use a local copy of the theme or QuickCSS, disable the online version of this theme, and replace the Google Fonts `@import` with this line at the top of your CSS:

```css
@import url('https://fonts.bunny.net/css?family=atkinson-hyperlegible-mono:200,200i,300,300i,400,400i,500,500i,600,600i,700,700i,800,800i|atkinson-hyperlegible-next:200,200i,300,300i,400,400i,500,500i,600,600i,700,700i,800,800i&display=swap');
```

Keep the three font variables unchanged. This requests normal and italic styles at each weight from 200 to 800. Bunny uses a different API format from Google's CSS2 endpoint; do not simply replace the hostname in the existing import.

### Installed fonts without external font requests

1. Download **Atkinson Hyperlegible Next** and **Atkinson Hyperlegible Mono** from the [Braille Institute](https://www.brailleinstitute.org/freefont/). Choose both families, including their normal and italic styles.
2. Install the desktop fonts through your operating system, then fully quit and reopen Discord or your browser.
3. Use a local copy of this theme or QuickCSS and remove its `@import` line. Keep the three font variables unchanged.
4. Disable any online copy of this theme and remove duplicate font imports from QuickCSS. Otherwise those copies will still request fonts externally.

The CSS family names match the installed fonts. If your client cannot access them, it uses the fallback fonts; browser privacy settings can restrict access to installed fonts. This removes this theme's external font requests, not Discord's other network traffic.

### Other download sources

Fontsource also provides desktop and webfont downloads for [Next](https://fontsource.org/fonts/atkinson-hyperlegible-next/use) and [Mono](https://fontsource.org/fonts/atkinson-hyperlegible-mono/use). Use desktop TTF/OTF files for system installation; WOFF/WOFF2 files are for web hosting. If you redistribute or self-host the fonts, retain their included SIL Open Font License.

## Font loading and troubleshooting

- The theme requests the stylesheet from `fonts.googleapis.com` and font files from `fonts.gstatic.com`. If those hosts are blocked or unavailable, the fallback fonts are used.
- Remove the old `* { font-family: ... !important; }` override if you previously pasted it into QuickCSS. It overrides fonts intended for code and other specialized text.
- If another theme changes fonts, disable its font override or test this theme by itself.
- To remove this theme, delete its online URL, disable its local theme card, or remove its QuickCSS, depending on how you installed it.

Installation behavior is documented in Vencord's [online theme settings](https://github.com/Vendicated/Vencord/blob/main/src/components/settings/tabs/themes/OnlineThemesTab.tsx) and [local theme settings](https://github.com/Vendicated/Vencord/blob/main/src/components/settings/tabs/themes/LocalThemesTab.tsx). See also [Vencord support](https://vencord.dev/support/).

## Credits

- Font: [Braille Institute and contributors](https://github.com/googlefonts/atkinson-hyperlegible-next), licensed under the SIL Open Font License.
- Theme: [@Today20092](https://github.com/Today20092) and [@TheCommieAxolotl](https://github.com/TheCommieAxolotl).
