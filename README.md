# deep-listening

_Deep learning experiments for audio classification_

A full write-up, including technical explanations and design decisions, as well as a summary of results achieved can be found within the associated [Project Report](https://github.com/jaron/deep-listening/blob/master/ProjectReport.pdf).

---

This project consists of several Jupyter notebooks that implement deep learning audio classifiers.


#### 1-us8k-ffn-extract-explore.ipynb 

* this notebook contains code to extract and visualise audio files from the [UrbanSound8K](https://serv.cusp.nyu.edu/projects/urbansounddataset/urbansound8k.html) data set
* the feature extraction process uses audio processing metrics from the [librosa](http://librosa.github.io/librosa/index.html) library, which reduces each recording to 193 data points
* as the audio information is highly abstracted, (we can not process successive frames using a receptive field), these features are intended to be fed into a feed-forward neural network (FFN)


#### 2-us8k-ffn-train-predict.ipynb

* this notebook contains the code to load previously extracted features and feed them into a 3-layer FFN, implemented using [Tensorflow](https://www.tensorflow.org/) and [Keras](https://keras.io/)
* also included is some code to evaluate model performance, and to generate predictions from individual samples, demonstrating how a trained model would be used to identify the nature of live recordings


#### 3-us8k-cnn-extract-train.ipynb

* this notebook extracts audio features suitable for input into a classic 2-layer Convolutional Neural Network (CNN)
* much more of the audio data is preserved in this approach, as the saved numpy feature data is over 2GB I haven't included it with this repository, but you can use the code in this notebook to extract it from the original [UrbanSound8K](https://serv.cusp.nyu.edu/projects/urbansounddataset/urbansound8k.html) data set


#### 4-us8k-cnn-salamon.ipynb

* this notebook implements an alternative CNN, similar to one described by [Salamon and Bello](https://arxiv.org/pdf/1608.04363.pdf) 

#### 5-ffbird-cnn.ipynb

* this notebook uses the Salamon and Bello CNN to process the [FreeField1010](http://machine-listening.eecs.qmul.ac.uk/bird-audio-detection-challenge/) data set of field recordings, with the goal of  recognising the presence of birdsong. 
* the data set is not part of this repository, so if you want to run this code you'll need to download the data yourself (see instructions in the notebook) 

#### 7-us8k-rnn-extract-train.ipynb

* this uses a Recurrent Neural Network to classify [Mel-frequency cepstral coefficients](https://en.wikipedia.org/wiki/Mel-frequency_cepstrum) (MFCC) features. 

--- 

Do get in touch if you've any questions, (me @ jaroncollis . com)
