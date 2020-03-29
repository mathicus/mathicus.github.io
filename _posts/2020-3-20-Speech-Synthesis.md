---
layout: post
title: Speech Synthesis
---
[breathing](https://htmlpreview.github.io/?https://raw.githubusercontent.com/jonfleming/SpeechSynthesisAPI/master/breathing.htm) |
[blank](https://htmlpreview.github.io/?https://raw.githubusercontent.com/jonfleming/jonfleming.github.io/master/blank.htm) |
[asteroids](https://htmlpreview.github.io/?https://raw.githubusercontent.com/jonfleming/jonfleming.github.io/master/asteroids.html)

## Finding Your Voice
The [Web Speech API](https://developer.mozilla.org/en-US/docs/Web/API/Web_Speech_API) enables you to incorporate voice data into web apps. The Web Speech API has two parts: SpeechSynthesis (Text-to-Speech), and SpeechRecognition (Asynchronous Speech Recognition.)

The SpeechSynthesis interface of the Web Speech API is the controller interface for the speech service; this can be used to retrieve information about the synthesis voices available on the device, start and pause speech, and other commands besides.

Before you convert text to speech you must select a voice. The getVoices() method of the SpeechSynthesis interface returns a list of SpeechSynthesisVoice objects representing all the available voices on the current device. 

I wanted to use a female US English voice. Here is how to filter on a specific voice name
~~~
// get all voices that browser offers
var available_voices = window.speechSynthesis.getVoices();
var english_voice = '';

// find voice by language locale "en-US" with name "Samantha"
for (var i = 0; i < available_voices.length; i++) {
    if (available_voices[i].lang === 'en-US' && available_voices[i].name === 'Samantha') {
        english_voice = available_voices[i];
        break;
    }
}

if (english_voice === '')
    english_voice = available_voices[0];
~~~

## GitHub Projects
- [Pages](https://github.com/jonfleming/jonfleming.github.io/tree/master/_posts)
- [SpeechSynthesisAPI](https://github.com/jonfleming/SpeechSynthesisAPI)


https://www.markdownguide.org/cheat-sheet/
