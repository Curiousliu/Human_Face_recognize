# Human_Face_recognize
## Description
An simple demo to recognize human face using keras and tensorflow
<br />Reprint from https://www.cnblogs.com/neo-T/p/6426029.html
<br />Reference https://zhuanlan.zhihu.com/p/36962109
## Environment
Win10\Anaconda 3.7\Python 3.7\Opencv 3.4.2\Tensorflow 1.13.1\Keras 2.2.4
## How to use
### First. Prepare Face Data
Open the shell in path <You Path\1_catch_face_data>, enter the command <python Save_face_data.py 0 1000 YourPath> twice to collect the face image of two people. Command <python\Filename.py\camera_id\number_of_photos\YourPathToSavePhotos>.
<br />Face images must be saved in the 'data' folder under the 'model' folder.
### Second. Train Your Model
Use the code segment line:218 in face_train_use_keras when training the model and comment out the code segment line:225. The model will be saved in the model folder;
<br />To evaluate the model, use the code segment line:225 and comment out the code segment line:218
### Last. Run
Open the shell in path <You Path\2_model>, enter the command <python face_predict.py 0>

  
