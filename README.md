# Synthetic-Iris-Image-Generation-Using-GANs

This project investigates the use of **Generative Adversarial Networks (GANs)** to produce realistic synthetic iris images, primarily for understanding potential biometric security vulnerabilities such as spoofing attacks. The GAN model consists of a **generator**, which creates artificial iris images, and a **discriminator**, which tries to distinguish between real and fake ones. As training progresses, the generator becomes better at producing images that can trick the discriminator.

Dataset Format
- Each subfolder represents a different iris class.
- Each class folder contains exactly 6 grayscale iris images.

Data Preprocessing
- Resizing to 64x64 pixels
- Conversion to grayscale
- Normalization to values between -1 and 1

GAN Structure
- Generator: Learns to produce synthetic iris images from random noise.
- Discriminator: Learns to classify images as genuine (from the dataset) or fake (from the generator).
- Combined GAN: Used to train the generator to produce increasingly realistic images.

Training Process
- Training the Discriminator: Exposed to both real and generated images to learn classification.
- Training the Generator: Adjusted to produce images capable of fooling the discriminator.

Evaluation Metrics
- Generating new synthetic images using the trained generator.
- Measuring how convincingly they are classified by the discriminator.

Standard Performance Mtetrics:
- Accuracy
- Precision
- Recall
- F1 Score

Output
Generated images are saved to the generated_images/ directory.
