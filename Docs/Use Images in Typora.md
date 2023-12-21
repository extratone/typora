## Images in Markdown

In markdown, image is written like `![alt](src)`. The `src` here can either be a URL like `https://octodex.github.com/images/yaktocat.png`, or an absolute/relative file path, like `../images/test.png`. 

* Outline
{:toc}



## How to insert images in Typora

### Write the Markdown

You could simply write down the markdown syntax to insert the image. Or click "image" from the menu bar, or press the shortcut key. When you do this, and meanwhile, if there is an image URL in clipboard, then the URL will be inserted into the `src` part directly.

### Drag & Drop

Of course, there's a easier way — drag & drop, like the screencast below. 

![drag-img](https://support.typora.io/media/about-image/drag-img.gif)

You could also drag & drop multiple image files at one time.

### Select from local files

You could click menu item `Format` → `Image` → `Insert Local Images…` from menu bar to open a dialog to select and insert local image(s). 

If you use this menu item frequently, we would suggest you to re-assign the shortcut key for this "insert image" command following [Custom Key Binding](https://support.typora.io/Shortcut-Keys/#change-shortcut-keys).

### Paste images from clipboard

Since Markdown file is only plain text file, users could not insert image data into Markdown file directly, but can insert image reference to file/URL. 

Typora support paste image data from clipboard, **after telling typora where to put those images**. Typora would put image data into given folder or server, then insert images referring to that stored file or URL. Please refer to section **[When insert local image…](#when-insert-local-image…)** for more detail.

> **Tips**: on macOS, users could copy image file from finder and then paste into typora. It has same behavior with drag and drop.
>
> **Tips**: on macOS, you could also copy images from iPhone and then paste into Typora after setup the location to put image files.

## When insert images...

Typora support copying image files into given folder or web server (require [iPic][]) when insert local images using drag & drop, or from menu bar. Following are instructions on the set-up.

### Default behaviors

By default, when you insert or drag & drop a image file into Typora, we will use the path of image file for attribute `src`. 

### Use Relative Path

If you enable `Editor` → `Image Insert` →  `Use relative path if possible` in preferences panel, and your writing has been saved into a file, then when you drag & drop a local image, the `src` attribute will be set as its relative path to current file (folder).

### Copy image files to target folder when insert local image

> To use this feature, you need to opt-in the option `Allow copy images to given folder` in preferences panel.

One common scenario is to edit `*.md` posts in static sites (like Jekyll) using Typora. For example, if the `.*md` file is put under `_posts` folder while the image files goes into `_media` folder, you may want to copy images files into folder `_media` when you drag/drop or paste images into Markdown file automatically. Here's how:

1. Save your file into some path.

2. Enable `Editor` → `Image Insert` → `Allow copy images to given folder` in preferences panel.

   <img src="https://support.typora.io/media/about-image/Snip20161117_2.png" style="zoom:50%" />

3. Select `Format` → `Image` → `When Insert Local Images` → `Copy Image File to Folder` from the menu bar, pick the target folder.

   ![Snip20161117_6](https://support.typora.io/media/about-image/Snip20161117_6.png)

In step 3, a new item `typora-copy-images-to: {relative path}` will be inserted into the [YAML Front Matter][] block of current document. So you could also manually add **typora-copy-images-to** property in YAML Front Matter to enable this behavior.

After that, if you drag & drop **local** images or paste images into Typora, the image file will be copied into the target file and update related `src`.

### Upload image file to web server.

Please refer [Upload Automatically When Insert Images](https://support.typora.io/Upload-Image/#upload-automatically-when-insert-images).

### Use global setting for image insert operations.

You could tell Typora where to copy images or upload images when insert images for all documents (global setting). You could find the images under "image" section in preferences panel.

![20190802](https://support.typora.io/media/about-image/20190802.png)

## Display images in relative path

### Relative path to current file/folder (default behavior)

By default, users could refer to local image by relative path to current `*.md` file. For example, if the `*.md` file is at `/User/typora/desktop/test.md`, then the `![img](image.png)` will display image from `/User/typora/desktop/image.png` just like the `<img>` tag in HTML. Also, for `../download/image.png`, image from `/User/typora/download/image.png` will be fetched.

### Relative path to certain folder

If you’re using markdown for building websites, you may specify a URL prefix for image preview in local computer with property `typora-root-url` in YAML Front Matters. 

For example, input `typora-root-url:/User/Abner/Website/typora.io/` in YAML Front Matters, and then `![alt](/blog/img/test.png)` will be treated as `![alt](file:///User/Abner/Website/typora.io/blog/img/test.png)` in typora.

In new version, instead of manually input `typora-root-url` property, you could just click item from the menu bar `Format` → `Image` → `Use Image Root Path` to tell Typora to generate `typora-root-url` property automatically.

## Upload images to cloud server

Typora supports to upload image to a cloud image server.

<img src="https://support.typora.io/media/image-upload/upload.gif" style="zoom:50%;" />

Please refer [Upload Image](https://support.typora.io/Upload-Image).

### Upload all local images to cloud server

Please refer [Upload All Local Images](https://support.typora.io/Upload-Image/#upload-all-local-images)

### Upload when inserting images

How-tos for this part can be found in section [When insert local image…](#when-insert-local-image…) → Upload image file to web server. 

## Align images

Currently Typora does not support image alignment. But you could use HTML code like `<center>![img](src)</center>` to align images on exported HTML or PDF.

Also, by default, if one paragraph only contains one image, it will be center aligned. It is controlled by CSS, and can be reverted by [add custom CSS](https://support.typora.io/Add-Custom-CSS/):

```css
p .md-image:only-child{
    width: auto;
    text-align: inherit;
}
```

## Resize images

Please check [this link](https://support.typora.io/Resize-Image/).

[YAML Front Matter]: http://yaml.org/
[iPic]: https://itunes.apple.com/app/id1101244278?ls=1&amp;mt=12---