# ML-Agents with Google Colab

<h4 align="center">
    Training Unity's built environment in server/headless mode with <a href="https://github.com/Unity-Technologies/ml-agents">ML-Agents</a> on Google Colab.
</h4>

> **Important details about this repository:**
> - Unity engine version used to build the environment = 2019.3.15f1 (Different versions will work but make sure that you don't get errors while generating the binaries)
> - ML-Agents branch = release_1
> - Environment name = 3dball (sample environment provided in ML-Agents repo) (Upload all the files )
>
> **Environment in this repo is build for Linux with server/headless mode enabled using the Unity engine.**
>
> **Upload all the files which are generated for the environment binary. Check out [this link](./headless_build/3DBall_example) to get an idea.**

---

<div align="center">
    <p>Try Google Colab Notebook</p>
    <p>
        <a href="https://colab.research.google.com/drive/12fuayKu7OjNN_4CycAXttdsUSIEkxesy#scrollTo=bW2MH47s5Gya">
          <img alt="colab link" src="https://colab.research.google.com/assets/colab-badge.svg" />
        </a>
    </p>
</div>

---

## What’s In This Document
- [Introduction](#introduction)
- [Prerequisites Tools](#prerequisites-tools)
- [Setup Instructions](#setup-instructions)
- [Extra Information](#extra-information)
- [License](#license)
- [Acknowledgements](#acknowledgements)

## Introduction

After struggling, on a particular question (**How to run ML-Agents on Google Colab?**) for days, I thought it would be great to create a github repo to share my findings on this topic as there is little to no information on the internet. This repo gives information on the above question by testing an example environment on colab. (This example environment is taken from ML-Agents [**repo**](https://github.com/Unity-Technologies/ml-agents))

So when I started working on Reinforcement Learning with ML-Agents (an interface provided by Unity, which is used to communicate with the learning environment made using the Unity engine). I felt the need to have one more PC because training requires hours to get completed and also using my RAM to its full potential (until it is exhausted 🙁). So I decided to shift the training process to Google Colab. And here I am gonna tell how I did this.

## Prerequisites Tools

- **Unity Game Engine :**
It is used to create, modify, and build the training environment in server/headless mode for the Linux system. Get the latest version of this software [here](https://unity3d.com/get-unity/download/archive).


## Setup Instructions

Run [**this**](./ML_Agents-with-Colab.ipynb) python notebook on Google Colab. This will clone the release_1 branch from ML-Agents github repo to colab. For the next step, it will clone this repo to get the example environment and provides the appropriate permissions to the Linux executable i.e. (.x86_64). And after this, it will enable the tensorboard and start the training process.

In the end, you can download the .nn file from the /content/models/${run_id} folder to embed that in your Unity environment for the inference process.


## Extra Information

The above-mentioned notebook only gives the trained (.nn) file and no visual observation while training, which I personally think has no fun at all. So after hunting down this question on the internet (i.e How to live stream the training process to twitch from Google Colab?) now I can observe and find any errors or new behavior in agents. So if you are interested then keep reading, or else you are good to go with the above settings.

<p align="center">
<a href="https://youtu.be/dLMkE8R5nTA">
    <img alt="video stats" src="https://youtube-stats-card.vercel.app/api/video?videoid=dLMkE8R5nTA&layout=compact&theme=dark_pink" />
</a>
</p>
Check out the above youtube video as an example that I have trained on google colab and live-streamed the whole training visuals to twitch and then export to youtube (because twitch only saves the video for 14 days).

To explain the process on how to live stream from colab, I have written an article on [**Medium**](https://dhyeythumar.medium.com/training-ml-agents-with-google-colab-live-streaming-to-twitch-5324a8dfa8ef).


## License
Licensed under the [MIT License](./LICENSE).


## Acknowledgements
1. [Unity ML-Agents Toolkit](https://github.com/Unity-Technologies/ml-agents/tree/release_1_branch)
