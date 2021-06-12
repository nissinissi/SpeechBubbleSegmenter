# SpeechBubbleSegmenter

This project's goal is finding speech bubbles in scans of comic book pages.

For example, the output for this image:

![source](https://user-images.githubusercontent.com/47719338/121791034-2ea2ac80-cbee-11eb-8e58-17a04ea08dd3.jpg)

should look like this:

![destination](https://user-images.githubusercontent.com/47719338/121791040-3a8e6e80-cbee-11eb-875e-074e52f359e1.jpg)

The repository implements a Unet, which is a powerful architecture for problems of semantic segmentation.
The idea of using a Unet to segment speech bubbles was first suggested in [this article](https://arxiv.org/pdf/1902.08137.pdf), which the project is actually based on.

The Unet was chosen because it requires fairly little input data while producing highly accurate results. It does so by expanding the standard structure of a deep CNN, by adding several "expanding layers" which are symmetrical to the usual layers of convolution and pooling.
The Unet model was quite groundbreaking at the time of its release. More about it can be read [in this article](https://arxiv.org/pdf/1505.04597.pdf).

The model was trained using the publicly available [eBDtheque](http://ebdtheque.univ-lr.fr/database/) dataset.
Access to the dataset was granted to me by the ever-kind Christophe Rigaud PhD.

I picked a subset of the images and labelled them manually.

