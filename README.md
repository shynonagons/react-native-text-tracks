# react-native-text-tracks

Implementation-agnostic text track support for React Native video playback.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)

## Installation

```
$ yarn add react-native-text-tracks
```

## Usage

```js
import Captions from 'react-native-text-tracks';

<Captions
  currentTime={currentTimeInMilliseconds}
  currentTextTrack={{
    source:
      'https://bitdash-a.akamaihd.net/content/sintel/subtitles/subtitles_en.vtt',
  }}
/>;
```

### Props

- [currentTime](#currentTime)
- [hasSeeked](#hasSeeked)
- [currentTextTrack](#currentTextTrack)
- [containerStyle](#containerStyle)
- [textStyle](#textStyle)

#### currentTime

Integer with the current time. It should change every second, yes. A common use case would be having a video an setting a state with the current time as it changes.

#### hasSeeked

When the time is changed the Captions component should re evaluate the text track file and get the current text for the given time. You can pass a simple boolean and invert it every time the video seeked a new timestamp.

#### currentTextTrack

An object with the `source` property containing the url. You can add more properties to this object, like name or lang, to use on the frontend for changing between each one.

#### containerStyle

The style for the container

#### textStyle

The style for the text
