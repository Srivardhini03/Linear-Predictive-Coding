# Linear-Predictive-Coding

In this project, Linear Predictive Coding (LPC) has been implemented and studied through MATLAB Graphical User Interface (GUI).

Linear predictive coding (LPC) is a widely used technique in audio signal processing, especially in speech signal processing. It has been particularly used to estimate the basic parameters of speech such as pitch (through frequency) and intensity (through loudness)

## Methodology:-

A Graphical User Interface (GUI) in MATLAB was designed to study the working of LPC.

#### Recording the Input Audio Signal

The user is asked to enter the duration of input speech signal 'x' in seconds.
When the 'Record' push button is pressed, the audio signal gets recorded and saved as a file.
When the 'Play' push button is pressed, the original audio signal is played and gets plotted.

#### User Inputs and Choices

The user is asked to enter the length of audio segment in ms to divide the recorded speech signal into smaller segments.
The percentage of overlap is entered by the user.
The user can choose from any of the 4 window functions - Hanning, Hamming, Barlett and Blackman.
The user can choose from any of the 4 Linear Predictor Filters of orders 12, 48, 72 and 96.

#### Encoding the speech signal and Computing Pitch

The sampled input speech signal is applied to an analyzer, which computes the parameters of the speech signal to be transmitted to the synthesizer, ie, the filter coefficients of LP Filter and the pitch of each segment.
The pitch of each segment of the speech segment is plotted.

#### Decoding the signal with and without Pitch

This speech synthesizer reconstructs the approximated speech signal. The input provided to the encoder is the comparison between the sampled signal and the approximated signal with the parameters.
This encoder forms the digital signal known as LPC output.
The LPC output is provided to the Low Pass Filter, which reconstructs the audio signal by performing the interpolation of samples in the input, with and without using the information of pitch.

## Results:-

### Original Speech Signal:
![](https://i.imgur.com/R5gZG8c.png)

### Plot of Pitch:
![](https://i.imgur.com/Mq5IaKy.png)

### Reconstruction of Speech Signal Without Pitch:
![](https://i.imgur.com/uzcQcnu.png)

### Reconstruction of Speech Signal With Pitch:
![](https://i.imgur.com/y6AAfGG.png)

## Analysis:-

### LP Filter of Order 12:
The quality of the reconstructed speech signal output was relatively low. Due to higher rate of compression, the output speech signal was distorted and less clear. The pitch of output signal was also low, as the output sounded deeper than the input speech.

### LP Filter of Order 48:
The quality of output speech signal increases as the number of previous samples (order of the LP filter) for prediction increases. Due to a lesser rate of compression the reconstructed speech signal was less distorted and more legible than before. The pitch of output was also marginally higher.

### LP Filter of Order 72:
The speech is more understandable due to very less distortion since the rate of compression is less. Thus, the overall output quality is better for the LP filter of order 72.

### LP Filter of Order 96:
Quality of output speech signal is the best for the LP filter of order 96. Since 96 previous samples have been considered to reconstruct the output, the compression rate is less, and thus the distortion of the output is also less. The output quality is clearer as compared to the previous lower order filters.

### Comparison of Quality of Speech Reconstruction With and Without Pitch Detection:-

### With Pitch Detection,

The rate of compression of the input speech signal was lower
The distortion of the output was lesser
The quality of the reconstructed output speech signal was better
The speech signal was clearer and the nasality tone of the output was more prominent.

### Without Pitch Detection,

The depth/pitch of the output speech was considerably higher.
