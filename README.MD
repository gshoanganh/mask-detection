# Mask Tensorflow Object Detection

This set of Notebooks is part of the tutorial [Custom object detection model using the Tensorflow Object Detection API](https://github.com/gshoanganh/mask-detection).
Youtube: [Gs Hoang Anh](https://www.youtube.com/c/GsHoangAnh).
A Mask detector was trained as a demo, it will produce results similar to the shown below:

![Object detection demo](./git_media/mask-data-01.png)
<br/> 

## Getting started
<pre>
Info my project:
- Python 2.7.16
- Tensorflow 2.4.0
- cuDNN 8.0
- CUDA 11.0
</pre>
Install [Tensorflow, cuDNN, CUDA](https://www.tensorflow.org/install/source#macos)
<br/>
<b>Step 01: </b> `git clone https://github.com/gshoanganh/mask-detection.git` 
or you can run on [Colab](https://colab.research.google.com/drive/)
<br/>
<b>Step 02: </b> open Terminal (or cmd) at `cd mask-detection` run
<pre>
python3 -m venv tfod
</pre>  

<br/>
<b>Step 3.</b> Activate your virtual environment
<pre>
source tfod/bin/activate # Linux (or macOS)
.\tfod\Scripts\activate # Windows 
</pre>
<br/>
<b>Step 4.</b> Install dependencies and add virtual environment to the Python Kernel
<pre>
python -m pip install --upgrade pip
pip install ipykernel
python -m ipykernel install --user --name=tfod
</pre>
<br/>
<b>Step 5.</b> Collect images using the Notebook <a href="#">1. Image Collection.ipynb</a> - ensure you change the kernel to the virtual environment as shown below 
<br/>
<b>Step 6.</b> Manually divide collected images into two folders train and test. So now all folders and annotations should be split between the following two folders. <br/>

```js
\TFODCourse\Tensorflow\workspace\images\train
\TFODCourse\Tensorflow\workspace\images\test
```
<br/><br/>
<b>Step 7.</b> Begin training process by opening <a href="#">2. Training and Detection.ipynb</a>, this notebook will walk you through installing Tensorflow Object Detection, making detections, saving and exporting your model. 
<br /><br/>
<b>Step 8.</b> During this process the Notebook will install Tensorflow Object Detection. You should ideally receive a notification indicating that the API has installed successfully at Step 8 with the last line stating OK.  

If not, resolve installation errors by referring to the <a href="#">Error Guide.md</a> in this folder.
<br /> <br/>
<b>Step 9.</b> Once you get to step 6. Train the model, inside of the notebook, you may choose to train the model from within the notebook. I have noticed however that training inside of a separate terminal on a Windows machine you're able to display live loss metrics. 

<br />
<b>Step 10.</b> You can optionally evaluate your model inside of Tensorboard. Once the model has been trained and you have run the evaluation command under Step 7. Navigate to the evaluation folder for your trained model e.g. 
<pre> cd Tensorlfow/workspace/models/my_ssd_mobnet/eval</pre> 
and open Tensorboard with the following command
<pre>tensorboard --logdir=. </pre>
Tensorboard will be accessible through your browser and you will be able to see metrics including mAP - mean Average Precision, and Recall.
<br />


<br />

<p>(c) Gs Hoang Anh</p>

