# Thesis_Audio_Uncertainity
Feature Uncertainty from Audio Noise

# 14th July

I uploaded the files With_Spectrogram_Experiment_v05.ipynb and Without_Spectrogram_Experiment_v05.ipynb. The former file includes the code where the input for the model is both MFCC spectrogram + Audio Transcript, whereas in the later code file, has the model input only Audio Transcripts. The directory for the input files in the code files needs to be changed to include noisy audio files or to include noiseless audio files.

There are also other code files such as:
--> GenerateNoiseAudioFiles.ipynb - In this code file, random noise is added to all the WAV audio files.
--> Merger_Files.ipynb - In this code file, the test and training data are merged together initially to include the oversampling technique and to lower the dimensionality of input data.
--> Transcription_Generator_v05.ipynb - In this code file, we generate the transcription for audio wav files in the text format and store them in a different directory.
--> Wav_Files_Generator_v05.ipynb - In this code file, mp3 audio files are converted to WAV format.

## 17th August

In the above code, I also added the code where I use the oversampling technique to balance the imbalance dataset and also I added the code for the Keras tuner and K-fold cross-validation to improve the Validation and test accuracy. After all the steps, validation accuracy reached 87%, whereas the test accuracy was around 50%.

## 27th August

Today I also added the code, where I now use now three most frequent label obseravtions from the data and then analyze the accuracy and uncertainty using entropy per class for 3 classes only, and analyze what the change in uncertainty is there when we use MFCC spectrograms with audio transcripts. We found out that the uncertainty value values are very low when we use a spectrogram with audio data as compared to the input with no spectrograms, even though there is a huge difference between the uncertainty values of the two categories. 

It shows using Mel spectrograms or MFCC, the model is more confident in predicting the class label or likelihood phoneme in a particular range rather than without MFCC spectrograms.



