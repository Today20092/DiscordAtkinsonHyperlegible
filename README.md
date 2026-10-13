# Atkinson Hyperlegible Next for Discord

A Vencord font theme using [Atkinson Hyperlegible Next](https://fonts.google.com/specimen/Atkinson+Hyperlegible+Next), designed for readability by the [Braille Institute](https://www.brailleinstitute.org/freefont/).

The theme sets Discord's `--font-primary` and `--font-display` variables. Code keeps Discord's monospace font. Regular and italic styles load from Google Fonts with weights 200 through 800; no system font installation or Vencord plugin is required.

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

## Font loading and troubleshooting

- The theme requests the stylesheet from `fonts.googleapis.com` and font files from `fonts.gstatic.com`. If those hosts are blocked or unavailable, the fallback fonts are used.
- Remove the old `* { font-family: ... !important; }` override if you previously pasted it into QuickCSS. It overrides fonts intended for code and other specialized text.
- If another theme changes fonts, disable its font override or test this theme by itself.
- To remove this theme, delete its online URL, disable its local theme card, or remove its QuickCSS, depending on how you installed it.

Installation behavior is documented in Vencord's [online theme settings](https://github.com/Vendicated/Vencord/blob/main/src/components/settings/tabs/themes/OnlineThemesTab.tsx) and [local theme settings](https://github.com/Vendicated/Vencord/blob/main/src/components/settings/tabs/themes/LocalThemesTab.tsx). See also [Vencord support](https://vencord.dev/support/).

## Credits

- Font: [Braille Institute and contributors](https://github.com/googlefonts/atkinson-hyperlegible-next), licensed under the SIL Open Font License.
- Theme: [@Today20092](https://github.com/Today20092) and [@TheCommieAxolotl](https://github.com/TheCommieAxolotl).
