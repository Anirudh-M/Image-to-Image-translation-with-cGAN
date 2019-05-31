# Image-to-Image-translation-with-cGAN
<p>This project uses pix2pix model to colorize black and white images. The model takes in black and white images, creates a color format of the image 
using the pix2pix architecture and stores the image in a folder. <p>
<p> To train the model, Places 365 dataset was used. <p>
<p> Improving on this, I tried to apply the concept for videos, where each video is converted to individual frames and each frame is 
passed through the model and the outputs are combined into a video. The method is explained in Video.ipynb. </p>
<h3> Training</h3>
<p> The following snippet shows how to run pix2pix.py while training</p>

```
python pix2pix.py \
  --mode train \
  --output_dir model \
  --max_epochs 200 \
  --input_dir photos/train \
  --lab_colorization
  ```
  <h3> Testing</h3>
  <p> While testing, change the mode to test </p>
  
  ```
  python pix2pix.py \
  --mode test \
  --output_dir colorize \
  --input_dir photos/test \
  --checkpoint model
  ```
 <h3> Acknowledgements </h3>

[pix2pix](https://github.com/phillipi/pix2pix) 
 model is used in this project which is a very efficient model and performs various tasks brilliantly.
 Thanks to [affinelayer](https://github.com/affinelayer/pix2pix-tensorflow) for porting pix2pix to TensorFlow. 
 The [Image-to-Image Translation with Conditional Adversarial Networks](https://arxiv.org/pdf/1611.07004.pdf) paper where we can find the explanation of working of the model and its various implementations.
  
 
