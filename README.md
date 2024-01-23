## <b>ImageColorizerAI</b> [[Project Page]](https://github.com/ronishdua/ImageColorizerAI.git) <br>

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
```
**Want To Add Your Own Image?**
1. Find any B&W image on Google.
2. Conver image to JPG.
3. Upload image into imgs folder.
4. Change end of line 7 to your image name.
5. Run demo_release.py
