# Youtube Video Download and Semantic Segmentation via PyTorch (Deeplabv3-ResNet101)

This is another fun project that allows automatically downloading youtube videos and running semantic segmentation on the videos. It may be used to quickly test/visualize pretrained models on the desired youtube videos. 

An example is:
![Alt Text](https://github.com/iodriller/Semantic-Segmentation/blob/master/example.gif)

### Requirements

Install the requirements by running the code below at the command window, at the project's directory (if pytorch doesn't install, install from [PyTorch](https://pytorch.org/)):

	pip install -r requirements.txt

At the examples given in jupyter notebooks, you need to replace <insert youtube link> with the youtube link that you would like to run the semantic segmentation algorithm:

### Examples

- __[example_1:](https://github.com/iodriller/Semantic-Segmentation/blob/master/example_1.ipynb)__ - With the given youtube link, it downloads the video, separates into a set of images (frame rate is adjustable), runs the desired semantic segmentation algorithm and reconstructs a video as the original video at the background overlayed with the object detection from the net.

### Comments

The project requires only the youtube link at minimum, yet it is easily costumizeble with a few lines of code. For example, you can pass a different net as:

	process_and_run(net='vgg11').run(youtube_link)

You might need to modify the semantic_images.py according to the: [PyTorch pretrained models](https://pytorch.org/hub/) for that specific net.

***

There are further modifications can be done easily, such as the frame rate limitation when separating the video into images. "frame_rate_limiter" in the separate_to_jpgs.py can be decreased to populate more images. If the program takes too much time, consider decreasing that value.