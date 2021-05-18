# videojs-next-episode
Next episode system in serials shows for rFlix....



# Table of Contents

# Installation
npm install --save videojs-next-episode
# Usage
To include videojs-next-episode on your website or web application, use any of the following methods.

# <script> Tag
This is the simplest case. Get the script in whatever way you prefer and include the plugin after you include video.js, so that the videojs global is available.

<script src="//path/to/video.min.js"></script>
<script src="//path/to/videojs-next-episode.min.js"></script>
<script>
  var player = videojs("my-video");
 
  player.nextEpisode();
</script> 
  
# Browserify/CommonJS
When using with Browserify, install videojs-next-episode via npm and require the plugin as you would any other module.

var videojs = require("video.js");
 
// The actual plugin function is exported by this module, but it is also
// attached to the `Player.prototype`; so, there is no need to assign it
// to a variable.
require("videojs-next-episode");
 
var player = videojs("my-video");
 
player.nextEpisode({
  showDialogTime: lastStart,
  url: `https://site.com/movie/1234`,
  nextEpisodeData: {},
  nextEpisodeText: "Next Episode",
  titlePrefixText: " ",
  seasonText: "Season ",
  episodeText: " Episode ",
  timeout: 8,
  placementIndex: 9
});

# RequireJS/AMD
When using with RequireJS (or another AMD library), get the script in whatever way you prefer and require the plugin as you normally would:

require(["video.js", "videojs-next-episode"], function (videojs) {
  var player = videojs("my-video");
 
  player.nextEpisode({
    showDialogTime: lastStart,
    url: `https://site.com/movie/1234`,
    nextEpisodeData: {},
    nextEpisodeText: "Next Episode",
    titlePrefixText: " ",
    seasonText: "Season ",
    episodeText: " Episode ",
    timeout: 8,
    placementIndex: 9
  });
});
