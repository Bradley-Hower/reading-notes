# *Course 201, Entry 11: Audio, Video, Images*

The web wouldn't be much without basic media content. Implementation is key though. Considerations should also be taken into account for accessibility. Maximizing accessibility maximizes an audience.

## Changes to Distribution 

In the earlier days of the internet, everyone was viewing web pages on their home computers or laptops. 

This made considerations for screen sizes of little consequence. Since then, mobile devices have become ubiquitous, and in some ways have taken over content consumption due to convenience. With this being the case, consideration of different screen sizes is now very relevant.

Also, video, once possible around the turn of the century, was implemented via third-party plugins, like Flash. Flash is no good though. It has been replaced with higher quality and more secure native HTML solutions. And with HTML5, we have even more capabilities at hand. 

## Video Attributes

There are a number of HTML attributes. Some are arguably absolutely necessary, others, dependent on the circumstance.

src - This provides the path for the video so it can be loaded. As with other attributes with links, `src` is set equal to a link within quotes.

controls - Allows for playback buttons in a video. Without a built-out solution, it's necessary to include this property. Not only is important for those with audio, visual, or neurological impairments, but how annoying would it be to watch a video, miss the first five seconds, and have to watch it all over again, multiple times, just to try to figure out what that first five seconds was. Annoying!

fallback link - Anchor link within the video tags, this serves as another option for folks who don't have an updated browser to view a video. It improves accessibility. Most people don't like to include this option as it encourages content theft and besides, people should update their browsers.

width and height - Similar to images, is a good placeholder in case the web page does not load entirely. Addtionally, text within paragraph tags, nested within the video tags, can give us some information, likeunto an alt attribute.

**autoplay** - Plays video automatically upon page load.

**loop** - Automatically replays a video.

**muted** - Turns off sound for video.

**poster** - Sets an image thumbnail before playing. Great for giving viewers a sense of the content.

**preload** - Buffers files, with the following options:

1. None. No buffering. Does not buffer the file.
2. Auto. Buffering on. Buffers the media file.
3. Metadata. Only buffers metadata.

### Subtitles

Subtitles have so many use cases. Assisting the hearing impaired, assisting people who can't hear the audio clearly due to various environments and speaker setups, and lastly, people speak different languages. There are clear motivations for putting in subtitles.

With WebVTT, subtitles are easier. Coming as a .vtt file, the content of the file follows the following format:

```
WEBVTT

322
00:28:28.230 --> 00:28:32.606
We could be that mistake!

323
00:28:35.739 --> 00:28:37.074
Okay! Just relax, man. 

```

To implement, include the `track` tag within the video tags. The track tag holds the following attributes:

**kind** - set equal to `subtitles`, within quotes.

**src** - link to the .vtt file.

**srclang** - set equal to the language abbreviation within quotes. For English, it would be "en", in Spanish, "es".

**label** - This provides a viewer with a clear indication of what subtitle track language is available for selection.

### Audio and Video Short Story

Audio and video can be a great couple. But they have to match and they have to make sense for each other. Things over time have changed. Audio and video have changed also - for the better. Now more beautiful and with higher fidelity than ever before.

## Grid 

Unlike flex, grid allows for a lot more flexibility. Most importantly, it offers the ability to easily manipulate vertical positioning.

Grid has some important components that make it work:

**Grid container** - The grid container is the outline of the grid box. This is where the grid lines and items will be held.

**Grid line** -  Within the grid container are the lines. These vertical and horizontal crisscrossing lines which create a geographically manageable area.

**Grid item** - Grid items are the objects we want to move and dictate their location for.

## Responsive Images

Responsive images take the viewer into consideration. While we could just make a one-size web page, this would be very frustrating for people, especially those with vision impairments, to be able to view and enjoy content. Ultimately, responsive imaging keeps a website relevant in the modern era, as all users benefit from a much more usable website. Moreover, don't waste people's data.

srcset - provides multiple source images with corresponding listed sizes, each set being delineated with a comma.

sizes - specifies which images to use in which conditions. This is accomplished by listing a max-width size, and then go-to image size for up to that upper limit.

Example:
```
srcset="fluffydog-500.png 500w, fluffydog_1000.png 1000w"
sizes="(max-width: 500px) 500px,
        1000px"
src="fluffydog_1000.png"

```

To properly implement accessible content that is not a bandwidth strain on mobile users, it is important to only load content that is useful to that user. For this reason, using `srcset` is a better option than CSS. With just CSS or perhaps a JavaScript solution, all content is loaded upfront and the proper size is served to the user - a waste. However, depending on the content and the audience, some might prefer larger content anyway. Perhaps give the viewer the option to choose.

## Things I want to know more about

What are the most common screen size. How many image sizes are sufficient?