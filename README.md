![Icon](http://i.imgur.com/uSO3wmE.png)

# equalizer-issue-tracker

<a href="https://play.google.com/store/apps/details?id=eu.pinpong.equalizer">
	<img alt="Get it on Google Play" src="https://play.google.com/intl/en_us/badges/images/generic/en-play-badge.png" height="60" />
</a>

The [issue][issues] tracker for **Equalizer**.

### [View issues][issues]
### [Open new issue][new-issue] (only English and German language allowed, no duplicates)

## Known issues:

* A short pause when enabling the Equalizer is needed to find out the current audio app.
  You can avoid that behavior by letting us start monitoring the current audio track directly after your phone booted.
  Use the switch in the app settings to opt-in.

## Players:

We maintain a list of music players that we know to support/not support Equalizer:

* [Google Play Music](https://play.google.com/store/apps/details?id=com.google.android.music): 
  Supported :heavy_check_mark:
* [Spotify Music](https://play.google.com/store/apps/details?id=com.spotify.music): 
  Supported :heavy_check_mark:
* [Jair Music Player](https://play.google.com/store/apps/details?id=aj.jair.music): 
  Supported :heavy_check_mark:
* [Phonograph Music Player](https://play.google.com/store/apps/details?id=com.kabouzeid.gramophone):
  Supported :heavy_check_mark:
* [Shuttle Music Player](https://play.google.com/store/apps/details?id=another.music.player):
  Supported :heavy_check_mark:
* [Music Player - MP3 Player, Audio Player](https://play.google.com/store/apps/details?id=musicplayer.musicapps.music.mp3player):
  Supported :heavy_check_mark:
* [Deezer](https://play.google.com/store/apps/details?id=deezer.android.app):
Supported, enable Equalizer on Deezer audio settings :heavy_check_mark:
* [Tidal](https://play.google.com/store/apps/details?id=com.aspiro.tidal):
  They're working on supporting the standard Android API :wrench:
* [SoundCloud](https://play.google.com/store/apps/details?id=com.soundcloud.android):
  They're [working on supporting the standard Android API](https://help.soundcloud.com/requests/483626/) :wrench:
* [VLC](https://play.google.com/store/apps/details?id=org.videolan.vlc):
  They're [working on supporting the standard Android API](https://trac.videolan.org/vlc/ticket/18254) :wrench:
* [Amazon Music](https://play.google.com/store/apps/details?id=com.amazon.mp3):
  Not implementing standard Android API ([more details][not-supporting]) :x:
* [Pulsar Music Player](https://play.google.com/store/apps/details?id=com.rhmsoft.pulsar):
  Not implementing standard Android API ([more details][not-supporting]) :x:
* [Poweramp](https://play.google.com/store/apps/details?id=com.maxmpz.audioplayer):
  Not correctly implementing standard Android API ([more details][not-supporting]) :x:
* [Pocket Cast](https://play.google.com/store/apps/details?id=au.com.shiftyjelly.pocketcasts):
  Not implementing standard Android API ([more details][not-supporting]) :x:
* [Stream YouTube Player](https://play.google.com/store/apps/details?id=com.djit.apps.stream):
  Not implementing standard Android API ([more details][not-supporting]) :x:
* [YouTube](https://play.google.com/store/apps/details?id=com.google.android.youtube):
  Not implementing standard Android API ([more details][not-supporting]) :x:

#### Players not supporting the standard Android API:

Equalizer doesn't work with some music players that don't provide track information, so that we can't apply audio effects.  
You can help by contacting us or the app developers directly to suggest supporting the standard Android API.
We've created a simple guide on how to support the API: [Guide for music player developers](EQUALIZER_BROADCAST.md).

## Changelog:

* **2.1.1:**
  * Fixed Android O related bugs
* **2.1.0:**
  * Stability improvements
  * Improved UI/UX
  * Improved compatibility with music players
* **2.0.3:**
  * Fixed Bluetooth device detection
  * Fixed  Equalizer stability
  * Fixed Theme selection
  * Fixed Bug when migrating from 1.3.6
  * Fixed UI issues
* **2.0.2:**
  * Fixed Bluetooth device detection
* **2.0.1:**
  * Fixed compatibility with Spotify
* **2.0.0:**
  * New Features
  * New supported languages
  * New Icon
  * Improved UI/UX
  * Improved compatibility with music players
  * Bugfixes
  * Update translations
* **1.3.6:**
  * Bug fixes
  * Update translation
* **1.3.5:**
  * Bug fixes
  * Update dependencies
  * Update translation
* **1.3.4:**
  * Bug fixes
  * Update translation
* **1.3.3:**
  * **New feature:** New language: Russian
  * **New feature:** New language: Japanese
  * **New feature:** New language: Thai
  * **New feature:** New language: Indonesia
  * **New feature:** New language: Portuguese
* **1.3.2:**
  * Bug fixes
  * Stability improvements
* **1.3.1:**
  * Bug fixes
  * Stability improvements
  * UI improvements
* **1.3:**
  * **New feature:** New free theme: Material
  * **New feature:** New theme: Pink
  * Bug fixes
  * Stability improvements
* **1.2.9:**
  * UI improvements
* **1.2.8:**
  * Bug fixes
  * Stability improvements
* **1.2.7:**
  * Stability improvements
* **1.2.6:**
  * Bug fixes
  * Stability improvements
* **1.2.5:**
  * Bug fixes
* **1.2.4:**
  * **New feature:** Disable notification
  * Bug fixes
* **1.2.3:**
  * Bug fixes
* **1.2.2:**
  * Bug fixes
  * **New language:** Hebrew
  * **New language:** Danish
* **1.2:**
  * Improvements
* **1.1:**
  * **New language:** French
  * **New language:** Bengali
  * **New language:** Hindi
  * **New language:** Chinese
  * **New language:** Dutch
  * **New language:** Italian
  * **New language:** Spanish
  * **New language:** Greek
* **1.0:**
  * *Initial release*

[issues]: https://github.com/pinpong/equalizer-issue-tracker/issues
[new-issue]: https://github.com/pinpong/equalizer-issue-tracker/issues/new
[not-supporting]: #players-not-supporting-the-standard-android-api
