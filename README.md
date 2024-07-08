# Bipedal-gym

This project is a fork of [roboterax/humanoid-gym](https://github.com/roboterax/humanoid-gym).
<br/>video: https://www.youtube.com/watch?v=a2n3hRnzHaw
<div align="center">
  <a href="https://youtu.be/a2n3hRnzHaw">
    <img src="http://img.youtube.com/vi/a2n3hRnzHaw/0.jpg" alt="Video Label" width="600"/>
  </a>
</div>

## Installation

1. Generate a new Python virtual environment with Python 3.8 using `conda create -n myenv python=3.8`.
2. For the best performance, we recommend using NVIDIA driver version 525 `sudo apt install nvidia-driver-525`. The minimal driver version supported is 515. If you're unable to install version 525, ensure that your system has at least version 515 to maintain basic functionality.
3. Install PyTorch 1.13 with Cuda-11.7:
   - `conda install pytorch==1.13.1 torchvision==0.14.1 torchaudio==0.13.1 pytorch-cuda=11.7 -c pytorch -c nvidia`
4. Install numpy-1.23 with `conda install numpy=1.23`.
5. Install Isaac Gym:
   - Download and install Isaac Gym Preview 4 from https://developer.nvidia.com/isaac-gym.
   - `cd isaacgym/python && pip install -e .`
   - Run an example with `cd examples && python 1080_balls_of_solitude.py`.
   - Consult `isaacgym/docs/index.html` for troubleshooting.
6. Install bipedal-gym:
   - Clone this repository.
   - `cd bipedal-gym && pip install -e .`



## Usage Guide

#### Examples
The urdf files of subo and stob are creations of [HRR Lab](http://www.hrrlab.com/) and are not shared.
<br/> If you have urdf files of subo and stob, you can save the file to this path "bipedal-gym/resources/robots" and run it.
```bash
# train cassie
python scripts/train.py --task=cassie_ppo  
# play cassie
python scripts/play.py --task=cassie_ppo
---------------------------------------
# train subo
python scripts/train.py --task=subo_ppo  
# play subo
python scripts/play.py --task=subo_ppo   
---------------------------------------
# train stob
python scripts/train.py --task=stob_ppo  
# play stob
python scripts/play.py --task=stob_ppo  
```
