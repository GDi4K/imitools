# imitools

Handy image utility built for pytorch & iPython notebooks (supports Google Colab).

* [Watch the tutorial on Youtube]()
* [Play with the Colab Tutorial](https://colab.research.google.com/drive/1-MN0M_76kP80SCBn1DPpGFWFSteJLThY?usp=sharing)

## Features

* Work with PIL images & Pytorch images
* Convert into each other as needed
* Zero boilterplate & fast workflow
* Show images inside the notebook
* Create a video from images
* Resize images easily
* Immutable workflow & create checkpoints
* Easy dyanmic plotting support for realtime feedback for long running tasks

## Installation

```
!rm -rf ./imitools && git clone https://github.com/GDi4K/imitools.git
```

## Usage

```
import imitools as I
```

Now you can use all the utility functions via the `I` global namespace.

## Examples

```
# show images
pt_images = torch.rand(10, 3, 8, 8)
I.wrap(pt_images).show()
```

```
# convert to pil images & wise versa
I.wrap(pt_images).pil()
I.wrap(pil_images).pt()
```

```
# create an immutable checkpoint for later use
# here we convert a set of pytorch images to PIL images internally & resize them
images = I.wrap(pt_images).cpil().resize(256)
```

```
# create a video from images
images.to_video().show()
```

```
# save images to disk
images.to_dir("./path/to/images")
```

```
# load images from disk & save to disk
I.from_dir("./path/to/images").show()
```

For more usage, check the [tutorial](https://colab.research.google.com/drive/1-MN0M_76kP80SCBn1DPpGFWFSteJLThY?usp=sharing).
