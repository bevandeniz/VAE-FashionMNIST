# VAE - FashionMNIST 

Utilizing Variational Autoencoder to create FashionMNIST images by sampling from the learned latent space.

## Fashion MNIST Dataset 
Fashion MNIST is a dataset of 70,000 grayscale images of 10 different clothing items, each image being 28x28 pixels. It's designed to replace the original MNIST dataset (handwritten digits) for benchmarking machine learning algorithms.

Key features:
* Image size: 28x28 pixels
* Number of images: 70,000 (60,000 training, 10,000 testing)
* Classes: 10 different clothing items
  
 ![image](https://github.com/user-attachments/assets/fb9eff03-a6ad-4426-97b3-5f408f301f6f)

## Variational Autoencoders
Variational Autoencoders (VAEs) are a type of generative model that learns a probabilistic representation of the input data. Unlike traditional autoencoders that output a single point in the latent space, VAEs output a probability distribution. This probabilistic nature allows them to generate new data instances that are similar to the training data.

How VAEs work:
* Encoder: The encoder maps the input data to a latent space, but instead of outputting a single point, it outputs the parameters of a probability distribution (typically a Gaussian distribution).
* Sampling: A random sample is drawn from the learned distribution.
* Decoder: The decoder takes the sampled latent code as input and reconstructs the original data.
The VAE is trained to minimize reconstruction errors (like a traditional autoencoder) and maximize the likelihood of data under the learned probability distribution. This second term, known as the Kullback-Leibler (KL) divergence, encourages the latent space to be well-organized and prevents the model from collapsing to a deterministic representation.
