#Deep Q Learning for ATARI using Tensorflow

(Version 1.0, Last updated :2016.03.17)

###1. Introduction

This is tensorflow implementation of 'Playing Atari with Deep Reinforcement Learning'.

This is renewal of (https://github.com/mrkulk/deepQN_tensorflow)

I used mrkulk's emulator interface and replay memory code and I made networks and main module

It needs 1~3 days to training.

I'm working on multiprocessing version for fast training.

###2. Usage

    python main_multithread.py (args)

    where args :

    -weight (checkpoint file) : for test trained network or continue training (default : None)
    -network_type (nips or nature) : nature version is more complex, need more time for training but has better performance.(default : nips)
    -visualize (y or n) : show opencv window for game screen or not (default : y)
    -gpu_fraction (0.0~1.0) : fraction of gpu memory to use. Needs roughly 1~1.5 Gb. (default : 0.9)
    -db_size (integer) : size of replay memory. Take 8Gb for size 1,000,000 (default : 1,000,000)
    -only_eval (y or n) : doing only evaluation without training if set to y (default : n)

###3. Testing with pretrained networks

    python main_multithread.py -network_type (nips or nature) -weight pretrained/(nips or nature)_pretrained -only_eval y

###4. Requirements:

- Tensorflow
- opencv2
- Arcade Learning Environment ( https://github.com/mgbellemare/Arcade-Learning-Environment )

###5. Video

https://www.youtube.com/watch?v=GACcbfUaHwc

###6. Changelog

-2016.03.17 : First upload!
