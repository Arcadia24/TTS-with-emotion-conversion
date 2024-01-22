# TTS-with-emotion-conversion
Text-to-speech using emotion conversion for more immersion into theatre piece. This repo will be implemented soon in [GOSAI](https://github.com/GOSAI-DVIC). The goal is too use the audio created by this program in an application to train for theatre when a comadian is not there. For more realisme we want to put emotion characteristic. 

![Explanation of the application](https://github.com/Arcadia24/TTS-with-emotion-conversion/blob/main/Theatre.png)

## Overview
This project leverages advanced voice conversion technologies to bring life to theatrical scripts. Using the [Coqui.ai library](https://github.com/coqui-ai/TTS) for voice synthesis and the [FAIRSEQ emotion conversion tool](https://github.com/facebookresearch/fairseq/tree/main/examples/emotion_conversion), this system transforms written scripts into expressive, character-specific audio files.

# How it works
With a CSV file of the script created with this [repo](https://github.com/hugodmn/Theatre_Script_Processing/tree/main) made by me and my classmate, the program creates first a Neutral version of the audio using the TTS fastspeech model. Then, using the emotion conversion tool made using fairseq, it generates audio from Neutral to the target emotion that the program specified.

# How to use it

## Installation

Create a environment

```
conda create -n emotion python=3.8 -y
conda activate emotion
```
Then:
```
git clone https://github.com/facebookresearch/fairseq.git
cd fairseq/examples/emotion_conversion
git clone https://github.com/Arcadia24/speech-resynthesis.git
cp -r preprocess_2/ preprocess/
```
Install emoV discrete token
```
wget https://dl.fbaipublicfiles.com/textless_nlp/emotion_conversion/data.tar.gz  # (still in fairseq/examples/emotion_conversion)
tar -xzvf data.tar.gz
```
Go back in the main folder with fairseq and install dependencies
```
pip install --editable ./
pip install -r examples/emotion_conversion/requirements.txt
```
Now download emoV dataset and put it in a folde named `dataset` in main folder

Download the folder with all the weights for the model in this [Drive]() and put them in a folder name save in the emotion conversion folder
```
cd fairseq/examples/emotion_conversion/save
```

After you use the notebook **generate_dataset.ipynb** to create all the audio files

## NoteBook control



## Audio Example
You can listen to some examples of audio generated

[Audio Example](https://drive.google.com/drive/folders/1HnyVwVjERHKs_aIR7H0eZaWzWf-23UlO?usp=sharing)
