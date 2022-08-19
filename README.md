# Sport-match-video-to-text
We created a model that predict the situation of the match using frame of a video. (Currently it's acc. is ~50%).

# Idea
Here we try to apply this research paper. link: https://www.mdpi.com/1424-8220/20/6/1702/htm <br>
We have one video and don't want to watch it so our model summarise that video in text form so you can read that text in few minutes.

# Data preprocessing 
We use cricket as a sport for our project. Dowload few videos of length ~30min and catagories it's frames to 5 classes manually.
1. Batting
2. Bowling
3. Crowd
4. Close-up
5. Boundry

After that we apply image augmentation on images but it is not bnificial for us. So we redce the size of the image as 227x227 and pass to our model.<br>
Train set contains the 80% of the data and test set contains the 20% of the data. 

# Model
as per research paper we have to use pretrain Alexnet with imagenet data and use there weight for transfore learning but for experiment purpose we apply alexnet direclt on our data.<br>
During training we got acc. ~50% after 20 epochs learning rate is 0.001 and loss function is cross-entropy.
Also, we improve our model with pretrained vgg16 model. Using that we try to classify between 2 classes. Accuracy around 98%.

# Testing
We test our model using one frame. Pass that into the model. 
After imporvemnt we take one short video of length 14s and fetch one frame per second pass it to traied model and predict the class.

# Contributor
1. Akash Kumar
2. Ashish Pandey
3. Jaimin Chauhan
4. Rupasai Ranagarju
5. Sumon Nath
