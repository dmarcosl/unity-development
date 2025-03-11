# Audio Mixer

The Audio Mixer allows you to mix various Audio Sources, apply effects to them, and perform mastering.

The window displays the Audio Mixer which is basically a tree of Audio Mixer Groups. Each one of them is essentially a mix of audio, a signal chain which allows you to apply volume attenuation and pitch correction. It allows to insert effects that process the audio signal and change the parameters of the effects. There is also a send and return mechanism to pass the results from one bus to another.

Attenuation is the volume control for an Audio Group.

![](image52.png)

* **S button**, soloing the group
* **M button**, muting the group
* **B button**, bypassing all the effects in the group

When you select Add you can select from a list of effects that can be applied to the group

![](image63.png)

* **Lowpass**, allows frequency behind the value
* **Highpass**, allows frequency above the value
* **ParamEQ**, alter the frequency response using linear filters
* **Pitch Shifter**, shift a signal up or down in pitch
* **Echo**, repeats a sound after a given delay, attenuating the repetitions based on the decay ratio
* **Chorus**, takes an Audio Mixer Group output and processes it creating a chorus effect
* **Normalize**, applies a constant amount of gain to an audio to bring the average or peak amplitude to a target level
* **Send**, sends the sound from a Audio Mixer Group to another with receive effect
* **Receive**, receives the sound from a Audio Mixer Group with a send effect and mixes it with the sound of the current group

You can take different Snapshots of the values of the Audio Mixer Groups.

You can set up Views of groups, having only a several of them visible in each one.

An Audio Mixer is an asset. You can create several and have more than one active at any time. An Audio Mixer always contains a master group. Other groups can then be added to define the structure of the mixer.

You route the output of an Audio Source to a group within an Audio Mixer. The effects will then be applied to the signal.

The Audio Mixer Group values can be edited during the gameplay and the changes persist.

Audio Pipeline: Audio Sources > Audio Mixers > Audio Listener