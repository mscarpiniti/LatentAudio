# Generating new sounds by vector arithmetic in the latent space of the MelGAN architecture

This script implements the training of a MelGAN for generating new sounds that are then combined in a convex manner for new sonority. The idea is presented in paper [1], while the training is based on the MelGAN architecture [2] whose source code is available at: https://github.com/descriptinc/melgan-neurips/blob/master/scripts/train.py

1. M. Scarpiniti, E. Massaro, D. Comminiello and A. Uncini, “Generating new sounds by vector arithmetic in the latent space of the MelGAN architecture”, in *Applications of Artificial Intelligence and Neural Systems to Data Science* (A. Esposito, M. Faundez-Zanuy, F. C. Morabito and E. Pasero, Eds.), ISBN: , pp. , Springer 2023.
2. Kundan Kumar, Rithesh Kumar, Thibault de Boissiere, Lucas Gestin, Wei Zhen Teoh, Jose Sotelo, Alexandre de Brebisson, Yoshua Bengio, and Aaron Courville, "MelGAN: generative adversarial networks for conditional waveform synthesis", in *Proceedings of the 33rd International Conference on Neural Information Processing Systems (NIPS'19)*, Red Hook, NY, USA, pp. 14910–14921, 2019.

The folder "Examples" contains some sounds generated by the proposed approach.

Specifically, we perform the linear combination of three test files and use this combination, after the mel spectrogram extraction, as input to the MelGAN.

The first case is regarding the linear combination: "*Mallet 2* - *String 1* + *Keyboard 1*". The resulting spectrogram is shown below.
![Alt text](Examples/Example1.jpg?raw=true "Example 1")

For the second combination, we use the linear combination: "*Keyboard 1* + 0.4 x *Organ 2* - 0.4 x *String 4*". The resulting spectrogram is shown below.
![Alt text](Examples/Example2.jpg?raw=true "Example 2")

Finally, the third linear combination is: "0.4 x *Organ 3* - 0.4 x *String 1* + 0.9 x *Organ 1*". The resulting spectrogram is shown below.
![Alt text](Examples/Example3.jpg?raw=true "Example 3")
