# TTS-with-emotion-conversion
Text-to-speech using emotion conversion for more immersion into theatre piece. This repo will be implemented soon in [GOSAI](https://github.com/GOSAI-DVIC). The goal is too use the audio created by this program in an application to train for theatre when a comadian is not there. For more realisme we want to put emotion characteristic. 

[Image](theatre.png)

## Overview
This project leverages advanced voice conversion technologies to bring life to theatrical scripts. Using the [Coqui.ai library](https://github.com/coqui-ai/TTS) for voice synthesis and the [FAIRSEQ emotion conversion tool](https://github.com/facebookresearch/fairseq/tree/main/examples/emotion_conversion), this system transforms written scripts into expressive, character-specific audio files.

## How it works
With a CSV file of the script created by with this [repo](https://github.com/hugodmn/Theatre_Script_Processing/tree/main) made by me and my classmate, the program creates first a Neutral version of the audio using the TTS fastspeech model, using the emotion conversion tool made using fairseq, it generates audio from Neutral to the target emotion that the program specified.

## Audio Example
You can listen to some examples of audio generated

[Audio Example](https://drive.google.com/drive/folders/1HnyVwVjERHKs_aIR7H0eZaWzWf-23UlO?usp=sharing)

## Future Works
- Push code
- Implement it as a GOSAI module
- Use it in a GOSAI application
