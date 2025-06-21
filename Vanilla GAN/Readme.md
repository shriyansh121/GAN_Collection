# Workflow of Vanilla GAN using Tensorflow

A Vanilla Generative Adversarial Network (GAN) consists of two neural networks: the Generator and the Discriminator, which are trained simultaneously in a competitive setting. These two networks engage in a zero-sum game where the Generator aims to create data that is indistinguishable from real data, while the Discriminator seeks to distinguish between real and generated data.

### The Generator:

The Generator network takes random noise (a vector of random numbers) as input and transforms it into a data sample, such as an image. Initially, the generated data is far from realistic, but over time, the Generator learns to produce data that increasingly resembles the real data.

### The Discriminator:

The Discriminator's role is to evaluate whether a given data sample is real (from the actual dataset) or fake (produced by the Generator). It outputs a probability indicating the likelihood that the sample is real. The Discriminator is trained to distinguish between real and fake data as accurately as possible.

### Training Process:

The training of a Vanilla GAN involves an iterative process where both networks are updated through backpropagation:

Generator's Goal: The Generator aims to fool the Discriminator by producing realistic data. It is trained to minimize the Discriminator's ability to differentiate between real and fake data.

Discriminator's Goal: The Discriminator is trained to correctly classify data as real or fake. Its objective is to maximize the accuracy in distinguishing the real data from the Generator’s output.

The loss functions for the Generator and Discriminator are based on binary cross-entropy:

The Discriminator's loss is a combination of the error in classifying real data as real and fake data as fake.

The Generator's loss is determined by how effectively it is able to fool the Discriminator into classifying its generated data as real.

### Optimization:

Both networks are optimized using gradient descent (commonly with the Adam optimizer). The Generator's parameters are updated to improve the quality of the generated data, while the Discriminator's parameters are updated to enhance its ability to distinguish real from fake data.
