# Human_Face_recognize
## Description
&nbsp;&nbsp;&nbsp;&nbsp;An simple demo to recognize human face using keras and tensorflow
<br />&nbsp;&nbsp;&nbsp;&nbsp;Reprint from https://www.cnblogs.com/neo-T/p/6426029.html
<br />&nbsp;&nbsp;&nbsp;&nbsp;Reference https://zhuanlan.zhihu.com/p/36962109
## Environment
&nbsp;&nbsp;&nbsp;&nbsp;Win10\Anaconda 3.7\Python 3.7\Opencv 3.4.2\Tensorflow 1.13.1\Keras 2.2.4
## How to use
### First. Prepare Face Data
&nbsp;&nbsp;&nbsp;&nbsp;Open the shell in path <Your Path\1_catch_face_data>, enter the command <python Save_face_data.py 0 1000 YourPath> twice to collect 1000 face images of two people. 
<br />&nbsp;&nbsp;&nbsp;&nbsp;Command <python\Filename.py\camera_id\number_of_photos\YourPathToSavePhotos>.
<br />&nbsp;&nbsp;&nbsp;&nbsp;Face images must be saved in the 'data' folder under the 'model' folder.
### Second. Train Your Model
&nbsp;&nbsp;&nbsp;&nbsp;Use the code segment line:218 in face_train_use_keras when training the model and comment out the code segment line:225. The model will be saved in the model folder;
<br />&nbsp;&nbsp;&nbsp;&nbsp;To evaluate the model, use the code segment line:225 and comment out the code segment line:218
```
    #训练模型。评估时这段代码不用，注释掉
    model = Model()
    model.build_model(dataset)
    model.train(dataset)
    model.save_model(file_path = './model/me.face.model.h5')

    # 评估模型。训练时，这段代码删除注释
    model = Model()
    model.load_model(file_path='./model/me.face.model.h5')
    model.evaluate(dataset)
```
&nbsp;&nbsp;&nbsp;&nbsp;Enter shell command 'python face_train_use_keras.py'
### Last. Run
&nbsp;&nbsp;&nbsp;&nbsp;Comment out the two code segments above<br />&nbsp;&nbsp;&nbsp;&nbsp;Open the shell in path <Your Path\2_model>, enter the command <python face_predict.py 0>

  
