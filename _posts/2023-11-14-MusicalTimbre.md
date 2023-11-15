--- 
title: Visualizing musical timbre
date: 2023-11-15 15:37:00 +0800
categories: [Blog, Music, Science,]
tags: [blog]     # TAG names should always be lowercase
math: true
---

## What is Timbre?


Basically *timbre* is the quality of a musical note or sound that distinguishes different types of musical instruments, or voices. It's related to the harmonic content of a sound. It is often used in music to describe the difference between two sounds, for example, a guitar and a piano playing the same note at the same volume. But they still sound different because of the timbre of the sound.

### Pitch

A ***Pitch*** is just a vibration at a certain frequency, for example the note A is 440 Hz. The pitch is the same for all instruments playing the same note. So we need to physically or digitally generate a sound wave at a certain frequency to produce a pitch. The difference stays in the manner of generation of the sound wave. That's when the timbre comes in.

### Pitch intresting fact

So if i take a drum and play it very fast, let's say 440 times per second, i will get the same pitch as the note A. Of course this will destroy the sticks and the drum will fire up.

Now if i play a very simple 3:4:5 polyrythm, what will happen is that the drum will play the note A, the note C and the note E at the same time. So i will get a chord: A minor. Now it's time to get rid of your drum because it will explode.

## Visualizing Timbre

In order to visualize the difference in timber we can use a special kind of tool, called a *spectrogram*. A spectrogram is a visual representation of the spectrum of frequencies of a signal as it varies with time. 

Let's now see some spectrograms for different instruments playing the same note.


![Spectrogram](/assets/img/sample/spectrogram.png)
_This is from an assignment i've done for my ISPR course, if you want to deepen into the maths behind it, you can check it out [here](https://github.com/U-n-Own/UniversityNotes/blob/master/Assignments/IntelligentSystemsforPatternRecognition/First%20Midterm/FirstMidterm_Spectrograms-Analisys-Instruments.ipynb) my code and explanation._

The main note on the spectrogram is the fundamental frequency, and the other notes are the harmonics. The harmonics are the multiples of the fundamental frequency. For example, if the fundamental frequency is 128Hz as in this case, the harmonics are 256Hz, 384Hz, 512Hz, etc...

Of course there is some noise, but that's because the instruments are not perfect, and the sound is taken by a microphone, which is not perfect either. But we can see that the harmonics are the same for all instruments, but the intensity of each harmonic is different. **That's what makes the difference in timbre.**

More differences can be found in the tremolo effect embedded in some instruments like the violin or generally string instruments. Different instruments plays notes in different ways, for example a Trumpet how does work? Well it's instresting here a video that explains it very well at minute 9:08:

{% include embed/youtube.html id='rGNUHigqUBM' %} 

## Conclusion

So now we know that the timbre of a sound is the difference in the intensity of the harmonics of the sound. And we can visualize it using a spectrogram. Why we are intrested in this niche thing of music? For example if we becomes rich and want to buy a custom shop guitar that is worth 35.000€, and a PRS that is 900€, we can see the difference in timbre between the two guitars. And we can see if the difference in price is worth it or not. Or just buy a PRS and a good plugin from [Neural DPS](https://neuraldsp.com/) (Not endorsed unfortunately) and save 34.000€. 