## Description
This is the code Jack Dinsmore, a freshman at MIT, wrote during his 2019 summer UROP with Phil Harris and SangEon Park. 

The focus of this project is to compare the train time and time per inference of MNIST on CPUs, GPUs, and TPUs. In order to facilitate an accurate comparison, the code for each device must be as similar as possible, and the dataset uses must be the same for all devices. This is why we are writing our own implementations of MNIST.

The motivation for conducting this comparison is that we hope the expected speed gain in TPUs will allow us to run other machine learning algorithms on TPUs with greater speed. Ultimately, we intend to investigate porting the Large Hadron Collider's level 1 trigger over to TPUs, thereby increasing the maximum-processable data rate and improving the speed of the collider.

## Notebooks
The notebooks were written in the following order
1) mnist-keras
2) mnist-estimator
3) mnist-tpu-estimator

mnist-keras simply implements MNIST with both MLP and CNN network structures using `keras` and plots the time per train iteration and the time per inference for both.

mnist-estimator does the same as mnist-keras, but using the `tf.estimator.Estimator` api, not the `keras` api.

mnist-tpu-estimator is a migration of mnist-estimator from `tf.estimator.Estimator` to `tf.contrib.tpu.TPUEstimator`. That way it can run on TPUs.
