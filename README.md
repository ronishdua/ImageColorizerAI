<!--<h3><b>ImageColorizerAI</b></h3>-->
## <b>Colorful Image Colorization</b> [[Project Page]](http://ronishdua.github.io/ImageColorizerAI/) <br>

**+ automatic colorization functionality for Real-Time User-Guided Image Colorization with Learned Deep Priors, SIGGRAPH 2017!**

**[Sept20 Update]** Since it has been 3-4 years, I converted this repo to support minimal test-time usage in PyTorch. I also added our SIGGRAPH 2017 (it's an interactive method but can also do automatic). See the [Caffe branch](https://github.com/richzhang/colorization/tree/caffe) for the original release.

![Teaser Image](http://richzhang.github.io/colorization/resources/images/teaser4.jpg)

**Clone the repository; install dependencies**

```
git clone https://github.com/ronishdua/ImageColorizerAI.git
pip install requirements.txt
```

**Colorize!** This script will colorize an image. The results should match the images in the `imgs_out` folder.

```
python demo_release.py -i imgs/ansel_adams3.jpg
```

**Model loading in Python** The following loads pretrained colorizers. See [demo_release.py](demo_release.py) for some details on how to run the model. There are some pre and post-processing steps: convert to Lab space, resize to 256x256, colorize, and concatenate to the original full resolution, and convert to RGB.

```python
import colorizers
colorizer_eccv16 = colorizers.eccv16().eval()
colorizer_siggraph17 = colorizers.siggraph17().eval()
``
