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
IP-adapter checkpoint you can download it from
[IP-adpater](https://drive.google.com/drive/u/0/folders/1TPbiVx4ijjd2tdbLNmwPgpR8UUoRizmj)

## Parameter in inference.py

AudioMAE will do pooling to both time and frequncy tokens in order to avoid just reconstruct the original audio. Largeer pooling rate will abandon information, thus will enhance the editability.

