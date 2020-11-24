# Trainable Quantum Convolution (aka Quanvolutions)

**Authors**
  * Denny Mattern (denny.mattern@fokus.fraunhofer.de)
  * Darya Martyniuk (darya.martyniuk@fokus.fraunhofer.de)
  * Fabian Bergmann (fabian.bergmann@fokus.fraunhofer.de)
  * Henri Willems (henri.willems@fokus.fraunhofer.de)


**Affiliation**

Data Analytics Center at Fraunhofer Institute for Open Communication Systems (Fraunhofer FOKUS) [1]. This demo results from our research as part of the PlanQK consortium [2].


**Abstract**

We implement a trainable version of Quanvolutional Neural Networks [3] using parametrized RandomCircuits. Parameters are optimized using standard gradient descent. Our code is based on the "Quanvolutional Neural Networks"-Demo of Andrea Mari [4].

We find that due to the randomized circuits training process is challenging and might take for some randomly generated circuits quite long, while other random circuits seem to be more suitable. For more stable results one might want to use hand crafted circuits instead of randomly generated ones. Otherwise one can use static seeds for the random circuit in order to get reproducable results.


**Further Research Questions**


1. What is the impact of the quantum layer to the result?
2. Is our hybrid quantum-classical neural net learning because of the trainable quanvolution or despite the quantum layer? I.e. is the quantum layer learning anything useful which helps the following layer to better classify the digits? Or is the dense layer "strong enough" to perform a classification despite the quantum circuit before?
3. If the quantum circuit is useful, what kinds of circuit architectures perform best?


[1] https://www.fokus.fraunhofer.de and https://www.data-analytics-center.org.

[2] https://www.planqk.de.

[3] Maxwell Henderson, Samriddhi Shakya, Shashindra Pradhan, Tristan Cook, "Quanvolutional Neural Networks: Powering Image Recognition with Quantum Circuits", 2019, arxiv:1904.04767.

[4] https://pennylane.ai/qml/demos/tutorial_quanvolution.html.
