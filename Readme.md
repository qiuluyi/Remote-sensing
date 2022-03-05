### step 1 -> python cut_data.py
 In order to improve the generalization ability of the model and avoid overfitting of the model during the training process. In the training phase, we use some data enhancement operations to increase the amount of data.
 
### step 2 -> Setting parameters in config.py
Moreover, due to the server memory limitation, the high-resolution remote sensing images cannot be directly input into the proposed DCNN for training. 
Therefore, we first slide the IRRG image and DSM auxiliary data in the ISPRS dataset into 512×512 size data, and set the overlap stride to 32px.
Then, We train all our models using the Adam optimization algorithm with a base learning rate of 0.001, a momentum of 0.9, a weight decay of 0.99 and a batch size of 4. 

### step 3 -> python train.py
The root of the DSMSFNet network used is at ../networks/deeplab/DSMSFNet.py.
Users can adjust the network architecture according to their own needs.

### step 4 -> cd ./tools and python metrics.py
In order to be able to effectively verify the effectiveness of the proposed method, we use the classical evaluation metrics to evaluate the network model proposed in this model, including: F1 score and Overall Accuracy.

### For more details, please contact the author: 458831254@qq.com