# Emoji CSS Builder

A simple tool for helping you display emoji in web browsers.

## What you get

* Tiled image of the emoji icons for efficient retrieval.
* Generated CSS classes for each icon.
* Sample HTML5 demo.

## What you need

* Any Ruby
* ImageMagick (or more specifically, the montage command)
* &#xe00d;

## What you do

Just require `emoji_css_builder`:

    # Build the default iphone emoji set
    EmojiCSSBuilder.build(:iphone, "/path/to/assets")

    # Build a subset of the iphone emoji:
    EmojiCSSBuilder.build(:iphone, "/path/to/assets", 
      %w(e001 e002 e00d))

Or use `rake`:

    rake emoji DEST=/path/to/assets
    rake emoji DEST=/path/to/assets SET=iphone
    rake emoji DEST=/path/to/assets SET=iphone ICONS=e001,e002,e00d

## What I need

* Images and icon sets for more

## Whom you should thank

* Kyle Barrow (http://pukupi.com/post/1964/)