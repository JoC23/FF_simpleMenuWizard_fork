https://www.reddit.com/r/firefox/comments/7dvtw0/guide_how_to_edit_your_context_menu/

1. Find your **profile folder** (profile names are different for everyone):  
   Address bar > Enter `about:support` > Click `Open Folder` (second one, not the "Update Folder").

2. [Download this project](https://github.com/stonecrusher/simpleMenuWizard/archive/master.zip) and unzip it.

3. 
    * `blank-context.css`	when right-clicking on a blank area or text
    * `frame-context.css` when right-clicking on an iframe
    * `image-context.css` when right-clicking on an image
    * `input-context.css` when right-clicking on an input-field
    * `link-context.css` when right-clicking on a link
    * `main-hamburger.css` when **left**-clicking on the three lines on top right
    * `main-menubar.css` when **left**-clicking on the main menubar (open with ALT key - file, edit, view, ...)
    * `media-context.css` when right-clicking on media like audio or html5 video
    * `newtab-containers.css` when right-clicking on the plus sign to open a new tab or container
    * `select-context.css` when right-clicking on selected text or object
    * `sidebar-context.css` when right-clicking on items in bookmark- or history sidebar
    * `sidebar-header.css` when **left**-clicking the sidebar dropdown menu
    * `source-context.css` when right-clicking a blank area on view-source pages
    * `tab-context.css` when right-clicking on a tab
    * `toolbar-context.css` when right-clicking on toolbar or tabbar
    * `urlbar-context.css` when right-clicking on the addressbar

6. Load `about:config` into addressbar. Search for `toolkit.legacyUserProfileCustomizations.stylesheets` and make sure the value is `true`.

=================================================================

## Hide Pocket / Sync / Screenshots
If you don't use either of those "internal addons" at all, you can just disable them, which will also remove their context menu entries everywhere.

How to do it: Load `about:config` into addressbar and set the respective value.

- Pocket: Search for `extensions.pocket.enabled` and switch to `false`.
- Sync: Search for `identity.fxaccounts.enabled` and switch to `false`.
- Screenshots: Search for `extensions.screenshots.disabled` and switch to `true`.

## Using simpleMenuWizard together with other custom modifications

Easiest thing to do is renaming the `userChrome.css` that came with the zip package of simpleMenuWizard.
Rename it to `simpleMenuWizard.css` and put it into `chrome` directory next to the already existing `userChrome.css`.

Open the old `userChrome.css` which is filled with foreign code and add `@import url("./simpleMenuWizard.css");` to the very top. That's it!
