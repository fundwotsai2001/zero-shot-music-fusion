# zero-shot-music-fusion(for inference)


One Paragraph of project description goes here

## Table of Contents
- [Installation](#installation)
- [Downloading Checkpoints](#downloading-checkpoints)
- [Usage](#usage)
- [Parameters](#parameters)

## Installation

Provide a step by step series of examples that tell you how to get a development environment running.

```bash
git clone https://github.com/fundwotsai2001/zero-shot-music-fusion.git
cd zero-shot-music-fusion
pip install -r requirements.txt
```
## Downloading checkpoint
for AudioMAE checkpoint you can download it from 
[pretrain](https://drive.google.com/file/d/1ni_DV4dRf7GxM8k-Eirx71WP9Gg89wwu/view?usp=share_link)

You will need to change the path in audio_encoder/AudioMAE.py
IP-adapter checkpoint you can download it from
[IP-adpater](https://drive.google.com/drive/u/0/folders/1TPbiVx4ijjd2tdbLNmwPgpR8UUoRizmj)
```
gdown https://drive.google.com/uc?id=1ni_DV4dRf7GxM8k-Eirx71WP9Gg89wwu
gdown https://drive.google.com/uc?id=1rA1zgCdioOpUpds-CdxL8uOKTx1-cAcH
```
You will need to change the path in inference.py


## Parameter in inference.py

AudioMAE will do pooling to both time and frequncy tokens in order to avoid just reconstruct the original audio. Largeer pooling rate will abandon information, thus will enhance the editability.
```
time_pooling can be set to 1,2,4,8,16,32,64
freq_pooling can only be set to 1,2,4,8
ip_scale can be set from 0~1, 0 stands for not considering the audio input, 1 means considering text and audio equally.
```
