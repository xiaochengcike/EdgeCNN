# Expression-Clasification
EdgeCNN:Improved CNN for Edge Computing  Devices and Its Applications on Facial Expression  Clasification

Datasets and EdgeCNN-G's trained models can be obtained in the following two ways：

1.Google Cloud Disk：https://drive.google.com/drive/folders/1WHebQdZrACVms0_3RDGxTTTSyuzfR48C?usp=sharing
2.Baidu cloud disk：链接：https://pan.baidu.com/s/1mZw9O-cqWhnwH_gu629v2A 
提取码：xucr 

Please put fer2013_data.h5, RAF_data.h5, CK_data.h5 in the data folder downloaded from the above link into the ./data path.Then, put the RAF_EdgeCNN and FER2013_EdgeCNN folders under the models folder downloaded from the above link into ./models.

That is, the data folder contains the following files: 
        
        ./data:         
                --RAF_data.h5          
                --RAF.py             
                --fer2013_data.h5             
                --fer.py
                --CK_data.h5         
                --CK.py
                
                
The models folder contains the following files: 

        ./models: 
                --RAF_EdgeCNN folder  
                  --PrivateTest_model.t7  
                --FER2013_EdgeCNN
                  --PrivateTest_model.t7
                --EdgeNet.py
                --vgg.py
                --resnet.py
                --__init__.py
        
Experimental environment：

        python 3.6
        pytorch 0.4.0
       
Running on the Raspberry Pi 3B+：
        
        pytorch2onn.py： Pytorch cannot be directly converted to an IR file. 
                Therefore, you need to convert the pytorch model to an onxx file using the pytorch2onn.py file.
                Finally, you can convert the onnx file to an IR file on ubuntu.
        
        pi_demo.py： Run on the Raspberry Pi 3B+ using an IR file.
In addition, the modified path of the file is required.

First, we use the dlib library to capture faces. The  implementation of this part can be viewed in our other project  implementation：https://github.com/tobysunx/face_recognition
