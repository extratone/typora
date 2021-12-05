<img src="https://i.snap.as/rjd6QGVp.png" alt="Typora Logo Version 2" style="zoom:33%;" />

![GitBook Slate](capture/GitBookSlate.png)

# My Darling, Typora (David Blue's Typora Configuration)

### This repo is my personal collection of themes/tricks/snippets/configuration files for Typora on Windows 10/11. It is *not* associated with Typora's ongoing development in any way.

I have found my perfect word processing solution. I have much to say about it, eventually, but for now, I want to share instructions you can follow that should result in you having *precisely* the same experience:

1. Download and install the latest [64-bit version](https://typora.io/#windows) for Windows.
2. Run Typora, open Preferences `Ctrl + ,` → Appearance and find "Open Themes Folder" near the bottom.
3. Download the .zip file of the GitBook theme's [latest release](https://github.com/h16nning/typora-gitbook-theme/releases/latest) and extract it to the themes folder. (As in, you should be adding one directory `/GitBook` to the themes folder along with 3 .css files.)
4. Return to Typora's Preferences menu and find "Open Advanced Settings." This should open `JustYou\AppData\Roaming\Typora\conf`, where you should see `conf.user.json` and
   `conf.default.json`. You should have basically zero reservations about fucking with these considering the software has a restore button right next to the one that got us here. That said - if you'd like to replicate my custom keybinds precisely, either open `conf.user.json` and copy and paste the snippet below where appropriate or just [**download the whole file**](https://github.com/extratone/typora/blob/main/config/conf.user.json) and replace. (I can't promise anything else will be kept as up-to-date.)

```json
"keyBinding": {
    "Highlight": "Ctrl+Shift+H"
    "Quote": "Alt+Q"
    "PrintDialog:": "Alt+P"
    "Always on Top": "Ctrl+Shift+P"
    "Task List": "Ctrl+Shift+T"
    "Strike": "Alt+S"
},
```

### My Custom Keybinds

| Action                                                  |      Input       |
| ------------------------------------------------------- | :--------------: |
| Highlight selected text `====`                          | Ctrl + Shift + H |
| Transform selected text into Markdown pullquote `>`     |     Alt + Q      |
| Show/hide legacy menu items                             |     Alt + P      |
| ~~Always on Top~~                                       | Ctrl + Shift + P |
| Transform selected text into Markdown task list `- [ ]` | Ctrl + Shift + T |
| Transform selected text into Strikethrough text `~~~~`  |     Alt + S      |



<img src="https://user-images.githubusercontent.com/43663476/126875727-a314692c-76da-4803-852e-84e319098ce4.png" width="45%"></img> <img src="https://user-images.githubusercontent.com/43663476/126875730-465e8581-6ebd-4b45-ab11-b24bb1f6819d.png" width="45%"></img> <img src="https://user-images.githubusercontent.com/43663476/126875731-86461bcd-cfa0-4a59-b580-bd6e2aa2c897.png" width="45%"></img> <img src="https://user-images.githubusercontent.com/43663476/126875735-753f4924-abf2-4a4b-9d9d-9b208f302192.png" width="45%"></img> <img src="https://user-images.githubusercontent.com/43663476/126875739-5742bc27-4a52-41a2-9ff7-838f74bf0c8a.png" width="45%"></img> <img src="https://user-images.githubusercontent.com/43663476/126875740-72de1b56-93d5-48dd-a819-73d001e280ba.png" width="45%"></img> <img src="https://user-images.githubusercontent.com/43663476/126875741-8ab0b94f-00ed-445a-9304-0bc066cd60f1.png" width="45%"></img> <img src="https://user-images.githubusercontent.com/43663476/126875742-058e9307-2620-49a8-91d7-9369ad3b957a.png" width="45%"></img> 

* [**My conf.user.json file**](https://gist.github.com/extratone/bda30d19e18cd70de2fafcbde5e3322d) in GitHub Gist form. (Embedded below.)
* [**GitHub Issue**](https://github.com/extratone/bilge/issues/11) for my upcoming (and ridiculously long-awaited) "review" of Typora around 1.0's release
* GitBook theme's [Theme Library page](https://theme.typora.io/theme/Gitbook/).

<script src="https://gist.github.com/extratone/bda30d19e18cd70de2fafcbde5e3322d.js"></script>


~~`![Typora Tile](https://i.snap.as/3vbelEU.png)`~~

`https://github.com/h16nning/typora-gitbook-theme/discussions/29`

## ~~~General Resources~~

~~* [Typora Theme Gallery](https://theme.typora.io/) (Web)~~

***

### [GitBook Slate CSS](https://github.com/h16nning/typora-gitbook-theme/blob/main/src/gitbook-slate.css)

(The below is just a truncated sample.)

```css
@import "gitbook/fonts.css";
@import "gitbook/slate-colors.css";

/*by 16soundsofsilence, yes this code is an absolute mess*/

html,
.form-control,
.modal {
    font-size: 16px;
}

body {
    background: var(--bg-color);
    font-family: var(--font-family);
    font-weight: 400;
    color: white;
    line-height: 1.6rem;
    height: 100%;
}

#write {
    font-size: 0.95rem;
    max-width: 850px;
    margin: 0 auto;
    margin-top: 1rem;
    padding: 30px;
    padding-bottom: 100px;
    position: static;
    width: 100%;
}

#write > ul:first-child,
#write > ol:first-child {
    margin-top: 30px;
}

a {
    color: var(--primary-color);
    text-decoration: none !important;
    transition-duration: 0.2s;
    transition-property: color;
}

a:hover {
    color: var(--primary-color-darker);
}

mark a,
mark .md-content.md-url {
    color: var(--primary-color-darker2);
}

mark a:hover {
    color: var(--primary-color-darkest);
}

.ty-preferences a {
    color: var(--primary-color);
}

h1,
h2,
h3,
h4,
h5,
h6 {
    position: relative;
    color: var(--heading-text-color);
    cursor: text;
}

h1:hover a.anchor,
h2:hover a.anchor,
h3:hover a.anchor,
h4:hover a.anchor,
h5:hover a.anchor,
h6:hover a.anchor {
    text-decoration: none;
}

h1 tt,
h1 code {
    font-size: inherit;
}

h2 tt,
h2 code {
    font-size: inherit;
}

h3 tt,
h3 code {
    font-size: inherit;
}

h4 tt,
h4 code {
    font-size: inherit;
}

h5 tt,
h5 code {
    font-size: inherit;
}

h6 tt,
h6 code {
    font-size: inherit;
}

h1 {
    font-size: 2.2rem;
    font-weight: 700;
    line-height: 1.5;
    margin-top: 3rem;
    margin-bottom: 0.5rem;
    padding-bottom: 0.2rem;
    border-bottom: solid 1px var(--borders);
}

h2 {
    font-size: 1.7rem;
    font-weight: 700;
    line-height: 1.5;
    margin-top: 2rem;
    margin-bottom: 0.5rem;
}

h3 {
    font-size: 1.375rem;
    font-weight: 700;
    line-height: 1.5;
    margin-top: 1.5rem;
    margin-bottom: 0.5rem;
}

h4 {
    font-size: 1.15rem;
    font-weight: 700;
    line-height: 1.5;
    margin-top: 1.5rem;
    margin-bottom: 0.5rem;
}

h5 {
    font-size: 0.95rem;
    font-weight: 700;
    line-height: 1.5;
    margin-top: 1.5rem;
    margin-bottom: 0.5rem;
}

h6 {
    font-size: 0.95rem;
    font-weight: 400;
    line-height: 1.5;
    margin-top: 1.5rem;
    margin-bottom: 0.5rem;
}

#write > h1.md-focus:before,
#write > h2.md-focus:before,
#write > h3.md-focus:before,
#write > h4.md-focus:before,
#write > h5.md-focus:before,
#write > h6.md-focus:before {
    color: var(--light-text-color);
    border: none;
    position: absolute;
    font-size: 0.9rem;
    font-weight: 500;
    padding: 0px;
    line-height: 1;
}

#write > h1.md-focus:before {
    content: "h1";
    top: 1.15rem;
    left: -1.75rem;
}

#write > h2.md-focus:before {
    content: "h2";
    top: 0.75rem;
    left: -1.75rem;
}

#write > h3.md-focus:before {
    content: "h3";
    top: 0.575rem;
    left: -1.75rem;
}

#write > h4.md-focus:before {
    content: "h4";
    top: 0.4rem;
    left: -1.75rem;
}

#write > h5.md-focus:before {
    content: "h5";
    top: 0.25rem;
    left: -1.75rem;
}

#write > h6.md-focus:before {
    content: "h6";
    top: 0.25rem;
    left: -1.75rem;
}

h1:first-child,
h2:first-child,
h3:first-child,
h4:first-child,
h5:first-child,
h6:first-child,
blockquote h1,
blockquote h2,
blockquote h3,
blockquote h4,
blockquote h5,
blockquote h6 {
    margin-top: 0rem;
}
..
/* This is a truncated sample!!
```

