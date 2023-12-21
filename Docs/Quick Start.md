# Welcome

Thank you for choosing **Typora**. This document will help you to start Typora.

[TOC]

## Live Preview

**Typora** use the feature: *Live Preview*, meaning that you could see these inline styles after you finish typing, and see block styles when you type or after you press `Enter` key or focus to another paragraph. Just try to type some markdown in typora, and you would see how it works.

**Note**: Markdown tags for inline styles, such as `**` will be hidden or displayed smartly. Markdown tags for block level styles, such as `###` or `- [x]` will be hidden once the block is rendered.

## Markdown For Typora

**Typora** is using [GitHub Flavored Markdown](https://help.github.com/articles/github-flavored-markdown/), For more detail, please open [Markdown Reference](Markdown%20Reference.md).

To see full markdown Syntax references and extra usage, please check `Help`->`Markdown Reference` in menu bar.

## Useful Shortcuts

#### Writing Assist Key

`Esc` key will trigger assistant behavior, like open inline preview for inline math, auto-complete for emoji, etc. More behavior will be supported in future.

#### Actions

- Select word: cmd+D
- Delete word: shift+cmd+D
- Select line/sentence: cmd+L
- Select row in table: cmd+L
- Add row in table: cmd+Enter
- Select Styled Scope (or cell in a table) cmd+E
- Jump to selection: cmd+J
- Jump to Top: cmd+↑
- Jump To Bottom: cmd+↓
- Increase/decrease heading level from `<p>` to `<h1>`: cmd+-/+
- New line: shift+Return
- Move table row/column: ⌘ + ⌃ + arrow key.

For more shortcut keys and custom key bindings, you can refer [here](https://support.typora.io/Shortcut-Keys/).

#### Styles

Please check the `Paragraph` and `Format` menu in menu bar.

#### Custom Shortcut Keys

Most shortcut keys are configurable, see [this document](https://support.typora.io/Shortcut-Keys/#change-shortcut-keys) for detail.

## Outline

Mouse over the windows toolbar and click the outline icon on the right top of the window can open outline panel. This Panel can be pinned to left side.

## Word Count

Mouse over the windows toolbar will make word count visible. "Always show word count" can be set from preference panel. Click it will popup detailed word count tooltip. If a range of text is selected word count for selection will also be displayed on word count tooltip.

## Quick Open

Currently Typora only provides a simple "Quick Open" function. Recent opened files, files from same folder or context folder (like a git repository) will be include in quick open file list. This features replies on OS X Spotlight to work correctly.

## Copy

We create typora and want to make it your default markdown editor, thus copy and paste means copy from another app or paste to another app, instead of *copy/paste from/to another markdown editor*. Therefore, by default, `Copy` means `Copy As HTML` ( and `Paste` means `Paste from HTML`). 

However, after click "**Copy Markdown source by default**", typora will copy selected text in HTML/markdown format (When pasting, rich editors will accept the HTML format, while plain text / code editor will accept the markdown source code format).

To **copy Markdown source code** explicitly, please use shortcut key `shift+cmd+c` or `Copy as Markdown` from menu. To **Copy as HTML Code**, please select `Copy as HTML Code` from menu.

## Smart Paste

**Typora** is able to analyze styles of the text content in your clipboard when pasting. For example, after pasting a `<h1>HEADING</h1>` from some website, typora will keep the 'first level heading’ format instead of paste ‘heading’ as plain text. 

To **paste as markdown source** or plain text, you should use `paste as plain text` or press the shortcut key: `shift+cmd+v`.

## Themes

Please refer to `Help` → `Custom Themes` from menu bar.

## Publish

Currently Typora only support to export as **PDF** or **HTML**. More data format support as import/export will be integrated in future.

## Command Line Tool

To launch typora from Terminal, you could add

```bash
alias typora="open -a typora"
```

in your `.bash\_profile` or other configuration file, then you would be able to do `typora file.md` for opening files by typora from shell/terminal.

## More Useful Tips & Documents

<https://support.typora.io/>

## And More ?

For more questions or feedbacks, please contact us by:

- Home Page: http://typora.io
- Email: <hi@typora.io>
- Twitter [@typora](https://twitter.com/typora)

We opened a Github issue page in case you want to start a discussion or as an alternative way to report bugs/suggestions: https://github.com/typora/typora-issues/issues