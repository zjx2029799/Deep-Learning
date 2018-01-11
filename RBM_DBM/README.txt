Datasets:

1. ECFPs.txt: ECFP information of 32 different signals, each being 128 bits. (32*128)

2. imgs_sample_i.txt (1=1,2,…7): Corresponding images for these 32 signals found from 7 different samples. Shape of each file: 32*720


Note: 

(1) Each line stands for the information of one signal and 8 files follow the same order of signals.

(2) Some signals may be not found in certain samples and the image information is filled with 0.


RBM:
1. Make us of all the signal samples to build a RBM model: One layer RBM with the dimension the same as ECFPs.
2. After training, get the parameters from the training process and make prediction of the test image to match the ECFPs

DBM:
1. Use the Autoencoder to simulate DBM model. After applying autoencoder, we will get the final layer called decode layer. The encode layer is the same dimension with ECFPs, which is the properties we want the machine to decipher. 
2. Compare the encode layer with the real ECFPs to see the differences and finally predict the real dataset with to match the ECFPs. Then we can predict each image represent for which kind of chemical signals in ECFPs.
