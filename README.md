# PhysicsInformedFlow
This repository contains Physics-Informed Neural Networks (PINNs) for simulating laminar incompressible flow in a pipe using DeepXDE and TensorFlow. 
  
## Physics Informed Networks: 
Neural Network used to solve supervised learning tasks while making sure physical laws are valid. The approach, known as physics-informed neural networks (PINNs), involves minimizing the residual of the equation evaluated at various points within the domain. Boundary conditions are incorporated either by introducing soft constraints with corresponding boundary data values in the minimization process or by strictly enforcing the solution with hard constraints.

In Physics-Informed Neural Networks (PINNs), the goal is to minimize the residual of a differential equation at predefined collocation points where the predicted solution is required to satisfy the equation. A physics-based loss function is formulated to quantify this residual, and a second loss function, typically based on the mean squared error, is used to enforce the initial and boundary conditions at training points, where the solution is known or assumed. The total loss function is a combination of these two losses, and the neural network's parameters are optimized by minimizing this total loss through gradient descent. This process enables the neural network to learn solutions that satisfy both the differential equation and the necessary boundary/initial conditions.

A convolutional network assumes special spatial structure in its input. In particular, it assumes that inputs that are close to each other in the original input are semantically related. Recurrent neural network layers are primitives which allow neural networks to learn from sequences of inputs. This layer assumes that the input evolves from sequence step to next sequence step following a defined update rule which can be learned from data.

## Results 
Here is an example of the PINN model's velocity field output:  
![PINN Output](/velocity_heatmap_animation.gif)

## References
- Raissi, M., Perdikaris, P., & Karniadakis, G. E. (2019). "Physics-informed neural networks: A deep learning framework for solving forward and inverse problems involving nonlinear partial differential equations."
- DeepXDE Documentation: https://deepxde.readthedocs.io/
- Experience report of physics-informed neural networks in fluid simulations: pitfalls and frustration (https://arxiv.org/pdf/2205.14249)

## License
This project is licensed under the MIT License.

---
Feel free to contribute or report issues!
