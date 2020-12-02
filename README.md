# SINONE

![fish](rendered_fish.png)

We propose an architecture, SINONE, for implicit representations, which performs at the same level and has similar convergence to the Fourier Features proposed in [1], but doesn't require any preprocessing of the data! Specifically, we propose a model whose first layer's activation is sin, which is initialized with a uniform distribution, and with a scale hyperparameter that behaves very similarly to the scale parameter in the aforementioned paper. In this document, we will delve into two very promising directions of implicit representations in computer vision from [1] and [2]. Specifically, we will investigate a close relative to SIREN networks from the lens of the Neural Tangent Kernel (NTK) [3], especially the suggested uniform initialization scheme and scale hyperparameter w_0 in the first layer of the network, i.e., the output of the first layer of a SIREN is sin(w_0 * Wx + b) where w_0 is a scalar. We note that SIREN networks can memorize things (like images) well, but may not perform as well in tasks which require generalization. Here, we find that SINONE achieves better performance in generalization in image regression, while exhibiting very similar convergence properties to ReLU MLPs with Fourier Features when varying the scale parameter. 

For experiments and results on image regression, check out the Jupyter Notebook PeriodicActivations.ipynb above.

[1] Tancik, M., Srinivasan, P., Mildenhall, B., Fridovich-Keil, S., Raghavan, N., Singhal, U., ... & Ng, R. (2020). Fourier features let networks learn high frequency functions in low dimensional domains. Advances in Neural Information Processing Systems, 33.

[2] Sitzmann, V., Martel, J., Bergman, A., Lindell, D., & Wetzstein, G. (2020). Implicit neural representations with periodic activation functions. Advances in Neural Information Processing Systems, 33.

[3] Jacot, A., Gabriel, F., & Hongler, C. (2018). Neural tangent kernel: Convergence and generalization in neural networks. In Advances in neural information processing systems (pp. 8571-8580).
