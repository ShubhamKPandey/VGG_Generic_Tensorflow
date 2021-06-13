# VGG_Generic_Tensorflow

It is primarily made up of a series of Conv2D layers followed by a softmax activated layers to classify the image.

* block_a: 64 filters, kernel_size 3, repetitions 2
* block_b: 128 filters, kernel_size 3, repetitions 2
* block_c: 256 filters, kernel_size 3, repetitions 3
* block_d: 512 filters, kernel_size 3, repetitions 3
* block_e: 512 filters, kernel_size 3, repetitions 3


After block 'e', we add the following layers:

* flatten
* fc: create a fully connected layer using[Dense](https://keras.io/api/layers/core_layers/dense/)
* classifier: create the classifier using a Dense layer. The number of units equals the number of classes. For multi-class classification, use a`'softmax'` activation
