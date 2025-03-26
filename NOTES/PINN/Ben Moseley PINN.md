
```embed
title: "Physics-Informed Neural Networks (PINNs) - An Introduction - Ben Moseley | Jousef Murad"
image: "https://i.ytimg.com/vi/G_hIppUWcsc/hqdefault.jpg"
description: "👉 PINNS in #MATLAB: https://www.youtube.com/watch?v=RTR_RklvAUQ🌎 Website: http://jousefmurad.com Physics-informed neural networks (PINNs) offer a new and v…"
url: "https://www.youtube.com/watch?v=G_hIppUWcsc"
```


```embed
title: "GitHub - benmoseley/harmonic-oscillator-pinn: Code accompanying my blog post: So, what is a physics-informed neural network?"
image: "https://opengraph.githubassets.com/147d5d4ba23aaefdc45f3a293456c4f16f8c09408450dc55bca3f068fd7e8c3b/benmoseley/harmonic-oscillator-pinn"
description: "Code accompanying my blog post: So, what is a physics-informed neural network? - benmoseley/harmonic-oscillator-pinn"
url: "https://github.com/benmoseley/harmonic-oscillator-pinn"
```

# what is PINS blog

```embed
title: "So, what is a physics-informed neural network? - Ben Moseley"
image: "https://benmoseley.blog/wp-content/uploads/2021/08/pinn-feature-1024x577.png"
description: "Machine learning has become increasing popular across science, but do these algorithms actually understand the scientific problems they are trying to solve? In this article we explain physics-informed neural networks, which are a powerful way of incorporating existing physical principles into machine learning."
url: "https://benmoseley.blog/my-research/so-what-is-a-physics-informed-neural-network/"
```

![nn](nn.gif)
If we use neural network :
![](Pasted%20image%2020250326233354.png)

- $\theta$ = free parameters
	- tune it so --> networks predictions matches available experimental data
- minimising the mean-squared-error between its predictions and the training points
  $$
   \min \frac{1}{N} \sum_{i}^{N} \left( u_{\text{NN}}(x_i; \theta) - u_{\text{true}}(x_i) \right)^2
   $$
   - $u_{NN}​(xi​;θ)$ = neural network's predicted output for input $x_i$
   - $u_{true}​(x_i​)​$ = true or expected output corresponding to $x_i$
## The “naivety” of purely data-driven approaches

![oscillator](oscillator.gif)
$$
m \frac{d^2 u}{dx^2} + \mu \frac{du}{dx} + k u = 0
$$
```ad-important
add the known differential equations directly into the loss function when training the neural network
```
![](Pasted%20image%2020250326235449.png)


$$\min \frac{1}{N} \sum_{i}^{N} \left( u_{\text{NN}}(x_i; \theta) - u_{\text{true}}(x_i) \right)^2
+ \frac{1}{M} \sum_{j}^{M} \left( \left( m \frac{d^2}{dx^2} + \mu \frac{d}{dx} + k \right) u_{\text{NN}}(x_j; \theta) \right)^2$$

```ad-question
If I know the equation then why i need then why don't i jus use the function instead of the neural network ?

In general we don't know the solutions to complex equations (like NS, wave equation)
```





```embed
title: "harmonic-oscillator-pinn/Harmonic oscillator PINN.ipynb at main · benmoseley/harmonic-oscillator-pinn"
image: "https://opengraph.githubassets.com/147d5d4ba23aaefdc45f3a293456c4f16f8c09408450dc55bca3f068fd7e8c3b/benmoseley/harmonic-oscillator-pinn"
description: "Code accompanying my blog post: So, what is a physics-informed neural network? - benmoseley/harmonic-oscillator-pinn"
url: "https://github.com/benmoseley/harmonic-oscillator-pinn/blob/main/Harmonic%20oscillator%20PINN.ipynb"
```


```embed
title: "Damped Harmonic Oscillator - Derivation and solution of the differential equations"
image: "https://beltoforion.de/images/title_s/infinite_zoom.webp"
description: "A complete derivation and solution to the equations of the damped harmonic oscillator."
url: "https://beltoforion.de/en/harmonic_oscillator/"
```


## 3 typical scientific task
![](Pasted%20image%2020250326203410.png)
![](Pasted%20image%2020250326203521.png)

Naive approach : Algorithm is not informed by any physics
	- just generating lots of training data
	- put a neural network in the middle of this
![](Pasted%20image%2020250326203750.png)
without PINS :
- input :  Velocity
- output : Pressure

> Just throw away all the existing science and physics knowledge

![](Pasted%20image%2020250326204040.png)
![myImage (1)](myImage%20(1).png)


> Physics-informed machine learning: from concepts to real-world applications
> https://ora.ox.ac.uk/objects/uuid:b790477c-771f-4926-99c6-d2f9d248cb23
> [Moseley_2022_Physics-informed_machine_learning](Moseley_2022_Physics-informed_machine_learning.pdf)


## pros and cons compared to traditional systems

![](Pasted%20image%2020250327011422.png)











