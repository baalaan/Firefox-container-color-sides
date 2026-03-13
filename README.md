# userchrome.css
Firefox allows users to change its interface using CSS. Let's do that!

### Customizations
The goal of this project is to basically fix small things I didn't really like about the Firefox UI:
* The selected tab does not stand out enough from the others
* The URL bar is a bit cluttered with all buttons displayed

This theme works with both dark and light Firefox themes.

With that in mind, here are the customizations:
* The "container color bar" below the tab is moved to the sides of the tab
  * The currently selected tab has wider borders, which makes it more visible
  * Hovering an inactive tab slightly thickens its borders as a preview
  * There is an animated border transition when selecting a new tab
* Tabs that are not selected have a slightly less visible font and dimmed favicons
* Inactive tabs get a subtle background highlight on hover
* Tab separator lines are hidden for a cleaner look

![tab switch gif](.github/screenshots/tabswitch.gif)

* The small search bar only displays the arrow button when the mouse is hovering over it (also with a small delay)
* The URL bar buttons are only displayed when hovering over it or when focused via keyboard, with a small delay

![URL bar gif](.github/screenshots/urlbar.gif)

* Close buttons are hidden on inactive tabs, but appear on hover

### How to use
1. Open Firefox
2. Go to `about:config` and set `toolkit.legacyUserProfileCustomizations.stylesheets` to `true`
3. Visit the `about:profiles` page
4. Open a command prompt / terminal and `cd` to the folder displayed as root directory of the currently selected profile
5. Run this command to download this repo into the `chrome` folder
```sh
git clone https://github.com/baalaan/Firefox-container-color-sides.git chrome
```
6. Restart Firefox. The theme should now be applied.

**Alternative**: Instead of doing step 4 and 5 you can also just directly download the [`userChrome.css`](userChrome.css) file, create a `chrome` directory in the profile directory (shown on the `about:profiles` page) and place the downloaded file there.

> **Note**: On some Linux distributions (e.g. Linux Mint), the Firefox profile directory may be located at `~/.config/mozilla/firefox/` instead of `~/.mozilla/firefox/`.

### Companion theme (optional)

The `theme/` folder contains **Container Clarity**, a companion Firefox theme that pairs with the CSS tweaks. It provides a muted, minimal color palette with subtle depth so container colors and the selected tab card stand out clearly. It includes both dark and light variants.

To install it:
1. Open Firefox and go to `about:debugging#/runtime/this-firefox`
2. Click "Load Temporary Add-on..."
3. Navigate to the `theme/` folder and select `manifest.json`

> **Note**: Temporary add-ons are removed when Firefox restarts. For a permanent install, you can package and sign the theme via [addons.mozilla.org](https://addons.mozilla.org).

### How to develop
There's a [tutorial on Reddit](https://www.reddit.com/r/FirefoxCSS/comments/73dvty/tutorial_how_to_create_and_livedebug_userchromecss/) on how to edit the Firefox UI like a website using the built-in developer tools.

### License
This is free as in "It's just a stylesheet; just use it, I don't care" software. Do whatever you like with it.
