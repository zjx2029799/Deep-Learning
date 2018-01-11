Datasets:

1. imgs-train.txt: N*720 2D matrix, each line stands for a flatted image of size 60*12 from real data;

2. bbs-train.txt:  N*800 2D matrix, each line stands for a flatted bounding box of size 40*20, from the corresponding image in file imgs-train.txt;

3. list-train.txt: N*8 2D matrix, each line store: Series NO.(from 0), mz_bin, rt_bin, mz, rt, Int_max_of_bb, bb_w_ratio, bb_h_ratio, respectively;

4. label-train.txt: N*2 matrix, each line contains the series NO. followed by 1 or 0, standing for good or bad signal, respectively;

5. train-goods/ train-bads folders: each file contains the raw image and its bounding box, named with its series NO.

6. Test data includes eight sets, for each set contains images and labels.

## To change the label, move images between the two folders and then run the label.py script in folder train-goods.


The steps I did:

1. Analyze the 4564 pictures of single-cell graph and narrow down the number of targets on the graph into 2D data. 
2. Implement single layer, multiple layers and CNN neuron network to train the processed data by Tensorflow (up to 95% accuracy).
3. Improve the model’s loss and accuracy by initializing the data set with Autoencoder (Reduce 90% of training time)

