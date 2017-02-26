# Pixar

- render a YouTube video (https://www.youtube.com/watch?v=7CVtTOpgSyY) in video.js player (http://docs.videojs.com/) integrated with vue.js 1.* (build a custom directive or component, flexiblity here. http://v1.vuejs.org/guide/).
  - when the YouTube finishes, automatically render an hls video (https://d2zihajmogu5jn.cloudfront.net/bipbop-advanced/bipbop_16x9_variant.m3u8) in the video.js player. 
- build a custom vuejs video controls component (don't worry about styling) that supports functionality including play/pause toggle, a full-width scrub bar with playhead to scrub forwards and scrub backwards, a display of current time and full video duration, and a way to toggle mute. Use any additional libraries desired to generate, but ensure implemented as vue.js component.
- modify the implementation of the scrub bar so that it supports displaying the entire video length (YouTube + HLS). You can store the durations in a data object fed into the component. Ensure that the current time and full video duration is a combination of the YouTube and HLS.
  - when the user clicks/drags across the scrub bar line (between the two videos), ensure the video source switches and the playback is initiated at the appropriate offset timestamp.
- add events to print/log the following events in a div below player:
  - video is ready
  - video play/pause state has changed
  - user has seeked forward/backward in the video
  - video source has changed
  - video has completed
  - video current time has changed (with current time)
  - video duration, when available


## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report
```

For detailed explanation on how things work, checkout the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).
