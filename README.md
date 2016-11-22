# deep-listening

_Deep learning experiments for audio classification_

This project consists of several Jupyter notebooks that implement deep learning audio classifiers.

#### 1-us8k-ffn-extract-explore.ipynb 

* this notebook contains code to extract and visualise audio files from the UrbanSound8K data set
* the feature extraction process uses audio processing metrics from the librosa library, which reduces each recording to 193 data points
* as the audio information is highly abstracted, (we can not process successive frames using a receptive field), these features are intended to be fed into a feed-forward neural network (FFN)


#### 2-us8k-ffn-train-predict.ipynb

* this notebook contains the code to load previously extracted features and feed them into a 3-layer FFN, implemented using Tensorflow and Keras
* also included is some code to evaluate model performance, and to generate predictions from individual samples, demonstrating how a trained model would be used to identify the nature of live recordings
