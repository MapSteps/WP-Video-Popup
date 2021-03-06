<p align="center">
<a href="https://wp-video-popup.com/" target="_blank" rel="noopener noreferrer">

![alt text](https://ps.w.org/responsive-youtube-vimeo-popup/assets/banner-772x250.jpg "WP Video Popup")

</a>
</p>

## Summary

- [Description](#description)
- [Installation](#installation)
- [Usage](#usage)
- [Examples](#examples)
- [Shortcode Attributes](#shortcode-attributes)
- [Advanced](#advanced)
- [WP Video Popup Pro](#wp-video-popup-pro)

## Description

[**WP Video Popup**](https://wp-video-popup.com/?utm_source=repository&utm_medium=link&utm_campaign=wp_video_popup) lets you add a responsive YouTube or Vimeo video lightbox popup to any page or post of your website.

- This plugin is 100% GDPR compliant. No connection to YouTube or Vimeo is established before the trigger element has been clicked.
- Embedding videos can slow down your website. With **WP Video Popup**, the lightbox & video are only being loaded by the click on the trigger element.

## Installation

#### Through The WordPress Administrative Area

- From WordPress administrative area, go to _Plugins_ -> _Add New_
- Search for "_WP Video Popup_" (By David Vongries)
- Install and then activate it

#### Download Manually

- Download [the zip file here](https://wordpress.org/plugins/responsive-youtube-vimeo-popup/) to your computer.
- Unzip the file.
- Upload the extracted folder to your `/wp-content/plugins/` directory.
- Activate the plugin through the Plugins menu in WordPress.

## Usage

Use the shortcode:

`[wp-video-popup video="link-to-your-youtube-video"]`

or

`[wp-video-popup vimeo="1" video="link-to-your-vimeo-video"]`

in your post, page or template file to embed your YouTube or Vimeo lightbox popup.

To open the popup, add the CSS-class `wp-video-popup` to the element you wish to trigger the lightbox.

## Examples

Example Shortcode to display a **YouTube** video:

```
[wp-video-popup video="https://www.youtube.com/watch?v=YlUKcNNmywk"]
```

Example Shortcode to display a **Vimeo** video:

```
[wp-video-popup vimeo="1" video="https://vimeo.com/136696258"]
```

After that, CSS class needs to be added to the element you want to open the lightbox: `wp-video-popup`. So your trigger element can be like this:

```
<a href="#" class="wp-video-popup">Play Video</a>
```

## Shortcode Attributes

- `mute="1"` : Mute video by default
- `start="24"` : Start video at a specific time (value in seconds)
- `portrait="1"` : Vimeo for instance allows you to upload videos in portrait mode

Example: `[wp-video-popup mute="1" start="24" video="https://www.youtube.com/watch?v=YlUKcNNmywk"]`

## Advanced

In addition to the Shortcode Attributes, there is a filter available to add more parameters to the embed-URL. By default, we only add the autoplay attribute to the embed-URL.

In the example below, we use the filter to remove the YouTube branding from the video by adding the modestbranding parameter:

```
function prefix_your_custom_embed_url_attributes( $video_url ) {
    $video_url .= '&modestbranding=1';
    return $video_url;
}

add_filter( 'wp_video_popup', 'prefix_your_custom_embed_url_attributes' );
```

## WP Video Popup Pro

For multiple popups on a single page, autoplay on page load functionality, self-hosted videos & more check out [WP Video Popup PRO](https://wp-video-popup.com/pricing/?utm_source=repository&utm_medium=link&utm_campaign=wp_video_popup)!

#### Features:

- Multiple Popups on a single Page/Post
- Self-Hosted Videos (New!)
- Autoplay on Page-Load
- Adjustable Popup Size
- Overlay Background-Color Setting

Get [WP Video Popup PRO](https://wp-video-popup.com/pricing/?utm_source=repository&utm_medium=link&utm_campaign=wp_video_popup) today!
