# ImiTools

Boilerplate free Image toolkit for PyTorch notebooks.
Make one-liners like this. 

```python
I.download(some_image_urls).crop(224).show()
I.download(some_image_urls).to_dir("/path/to/images")
pytorch_images = I.from_dir("path/to/images").resize(256).pt()
images = I.wrap(pytorch_images ).crop(224)
images.show()
pil_images = images.pick(0, 3, 4).normalize().pil()
I.merge(images, pil_images, pytorch_images, pil_images[0]).resize(128).to_dir("thumbs")
```

> Play with the Tutorial: [Colab](https://colab.research.google.com/github/GDi4K/imitools/blob/main/docs/tutorial.ipynb), [GitHub](./docs/tutorial.ipynb)

## Why?

![ImiTools Architecture](https://user-images.githubusercontent.com/50838/201626247-7975a670-d727-49cb-b93d-b355f710391d.png)

- Bring in images from all sources into a single place like PyTorch images, PIL images, Disk, or Internet
- Apply various transformations like crop, resize, normalization, etc
- Then output them as you like including displaying, PyTorch tensors, inline video, and to disk.
- Imagine all those things without some boilerplate free code and one-liners

> Play with the Tutorial: [Colab](https://colab.research.google.com/github/GDi4K/imitools/blob/main/docs/tutorial.ipynb), [GitHub](./docs/tutorial.ipynb)

## Installation

```
!rm -rf ./imitools && git clone https://github.com/GDi4K/imitools.git
```

## Usage

```
import imitools as I
```

Now you can use all the utility functions via the `I` global namespace.

## Tutorials

For more usage, check the tutorial: [Colab](https://colab.research.google.com/github/GDi4K/imitools/blob/main/docs/tutorial.ipynb), [GitHub](./docs/tutorial.ipynb)

You can also look at the [source code](./imitools.py) for more info.
