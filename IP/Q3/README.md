Adding Audio and Video with Control Elements in HTML5

1. Audio with Controls

To add an audio file in HTML5 with built-in play, pause, and volume controls, we use the <audio> tag along with the controls attribute. The controls attribute tells the browser to display its default audio player interface. Multiple <source> elements can be added so that the browser can choose a format it supports. A fallback text can be included for browsers that do not support HTML5 audio.

Example:

<source src="media/song.mp3" type="audio/mpeg">  
<source src="media/song.ogg" type="audio/ogg">  
Your browser does not support the audio element.  
</audio>

Important attributes for audio:
• controls – displays the built-in player UI.
• autoplay – plays the audio automatically (may require muted in modern browsers).
• loop – restarts the audio when it finishes.
• muted – starts audio in muted state.
• preload – tells the browser how much to preload (none, metadata, or auto).

⸻

2. Video with Controls
   To add a video file in HTML5 with built-in play, pause, timeline, and volume controls, we use the <video> tag with the controls attribute. Multiple <source> elements are provided for better browser compatibility. We can also set the size using width and height and add a poster image using the poster attribute.

Example:

<source src="media/clip.mp4" type="video/mp4">  
<source src="media/clip.webm" type="video/webm">  
<track kind="captions" src="media/clip.en.vtt" srclang="en" label="English" default>  
Your browser does not support the video tag.  
</video>

Important attributes for video:
• controls – displays the default video player UI.
• autoplay – starts playing automatically (often requires muted).
• loop – repeats the video after it finishes.
• muted – starts muted.
• poster – displays an image before the video starts.
• playsinline – ensures video plays inline on mobile devices instead of fullscreen.
• preload – same as in audio.
• <track> – adds captions or subtitles (must be in .vtt format).

⸻

3. Accessibility and Best Practices
   • Always include captions with <track> for accessibility.
   • Provide fallback text inside <audio> and <video> tags for unsupported browsers.
   • Use descriptive file names and correct MIME types in the type attribute (e.g., audio/mpeg for MP3, video/mp4 for MP4).
   • Offer multiple file formats for maximum compatibility across browsers.
   • Keep media file sizes optimized to reduce loading times.
