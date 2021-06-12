# SpeechBubbleSegmenter

This project's goal is finding speech bubbles in scans of comic book pages.

For example, the output for this image:

![1](https://user-images.githubusercontent.com/47719338/121791457-8ba06180-cbf2-11eb-961e-5036b5a1bc85.jpg)

should look like this:

![2](https://user-images.githubusercontent.com/47719338/121791460-92c76f80-cbf2-11eb-8a92-c6ef33e2bbc7.jpg)

The repository implements a Unet, which is a powerful architecture for problems of semantic segmentation.
The idea of using a Unet to segment speech bubbles was first suggested in [this article](https://arxiv.org/pdf/1902.08137.pdf), which the project is actually based on.

The Unet was chosen because it requires fairly little input data while producing highly accurate results. It does so by expanding the standard structure of a deep CNN, by adding several "expanding layers" which are symmetrical to the usual layers of convolution and pooling.
The Unet model was quite groundbreaking at the time of its release. More about it can be read [in this article](https://arxiv.org/pdf/1505.04597.pdf).

The model was trained using the publicly available [eBDtheque](http://ebdtheque.univ-lr.fr/database/) dataset.
Access to the dataset was granted to me by the ever-kind Christophe Rigaud PhD.

I picked a subset of the images and labelled them manually.

