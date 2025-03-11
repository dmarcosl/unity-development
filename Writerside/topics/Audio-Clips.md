# Audio Clips

## Normal Audio

Digital record of a sound wave stripped of the parts not audible by the human ear.

Some normal audio formats are:

* .aif
* .wav
* .mp3
* .ogg

## Tracker Modules

The tracker modules store instrument and note data in patterns, in a form similar to a spreadsheet. Those patterns contains note number, instrument number and controller messages.

Some tracker modules formats are:

* .xm
* .mod
* .it
* .s3m

## Compression Formats

| Format     | Compression | CPU Usage | Rule of Thumb                    |
|:-----------|:------------|:----------|:---------------------------------|
| PCM        | None        | Low       | Short clips used often           |
| ADPCM      | X 3.5       | Med       | Noisy clips because of artifacts |
| Vorbis/MP3 | X 10        | High      | Medium length SFX and music      |

## Options

To import an audio clip in Unity just draw and drop it to the Project view.

At select an audio clip in the Project View, the properties are displayed in the Inspector View. At the bottom is displayed a sample of the sound wave, and above it there are three buttons, from right to left:  

![](image74.png)

* **Play**, play the audio clip
* **Loop on**, replay at finish
* **Auto play**, auto play the audio clip at select it in the Project view

In the Inspector view, above the sample, we can found the compression settings, which allow us to select different compressions for each platform.

![](image42.png)

The options are:

* **Load type**
    * **Decompress On Load**: decompress at load the scene (consumes a lot of memory, but does not impact the CPU usage)
    * **Compressed in Memory**: decompress when is used (impacts the CPU usage but does not consume much memory)
    * **Streaming**: read from disk and decompress when is used (no memory consuming, but highly impacts the CPU usage)
* **Compression Format**, the compression that will be used
* **Quality**, only available with Vorbis, to high value, less compress
* **Sample Rate Setting**
    * **Preserve**, do not change the sample rate of the audio file
    * **Optimize**, deduce the optimal sample rate
    * **Override**, override the sample rate of the audio file with a custom value

Above the compression settings, there are some other options:

![](image8.png)

* **Force to mono**, merge the two channel audio to one channel audio, a side effect is that the volume level is reduced and quite quiet
    * **Normalize**, normalize the peak amplitude of the sound wave of the audio clip
* **Load in background**, the clip will run on a separate thread without blocking the main one
* **Ambisonic**, ambisonic audio sources store audio in a format which represents a soundfield that can be rotated based on the listener's orientation.
* **Preload audio data**, start load the clip at level start (Obsolete)

To save the settings push the Apply button, to discard them, push the Revert button.