# Associative Memory with Hopfield Recurrent Neural Networks

## 1. Project Overview
This project explores the design and implementation of a **Hopfield Network**, a form of recurrent artificial neural network that serves as an **associative memory** system. The network is trained to store and retrieve specific 2D digit patterns (0, 1, 2, 3, 4, 6, 9, and ".") through **Attractor Dynamics**. 

The primary focus is on analyzing the network's ability to reconstruct original patterns from incomplete or noisy inputs (10% and 25% noise) using different update strategies.
<img width="919" height="336" alt="image" src="https://github.com/user-attachments/assets/7e8ee05d-6d31-4c78-9b81-2bc6083a1faf" />
<img width="925" height="333" alt="image" src="https://github.com/user-attachments/assets/73ba3cd1-dc05-431c-9b04-ab7973732d81" />


## 2. Technical Methodology
### Training: Hebbian Learning
Unlike standard feedforward networks, the Hopfield network uses **Hebbian Learning** to store patterns in a symmetric weight matrix with no self-connections ($w_{ii}=0$). 

### Dynamics: Update Rules
Two fundamental update procedures were implemented and compared:
* **Synchronous Update:** All neurons update their states simultaneously in each iteration.
* **Asynchronous Update:** Neurons are updated sequentially, providing a more biological and often more stable path to convergence.

### Energy Minimization
The network's stability is governed by an **Energy Function ($E$)**. During the recall process, the network evolves toward "Attractors" or stable states that minimize this energy, ideally corresponding to the stored memories.

## 3. Key Findings & Performance Analysis
* **Recall Accuracy:** The network achieved perfect recall for most patterns (0, 1, 3, 6, 9).
* **Pattern Similarity Challenge:** Certain patterns (e.g., "2" and ".") showed minor Hamming distances even in clean recall, due to high overlap with other stored states leading to local minima.
* **Noise Robustness:** The system successfully recovered original digits from 10% noise. At 25% noise, while reconstruction was attempted, the network occasionally settled into "false memories" or hybrid patterns.

## 4. Visualizations

### Stored Digit Patterns
*The 120-neuron state vectors representing the 8 stored patterns.*
<img width="1250" height="346" alt="image" src="https://github.com/user-attachments/assets/3d32b46a-2f73-4234-8114-c48c3d3cca62" />
<img width="1237" height="342" alt="image" src="https://github.com/user-attachments/assets/ebfd2e83-f257-4f9f-8e21-2b40be9c332e" />

<img width="1173" height="325" alt="image" src="https://github.com/user-attachments/assets/52d75de2-20c6-4fbe-9367-6b877e4cedf4" />
<img width="1208" height="334" alt="image" src="https://github.com/user-attachments/assets/bd2d8982-c313-4043-beb2-5171ee1f6b86" />


### Energy Convergence (Stability Analysis)
*Demonstrating how the network minimizes its global energy to reach a stable attractor.*
<img width="999" height="495" alt="image" src="https://github.com/user-attachments/assets/555b80bc-8703-4c2f-92ef-87474a6e8718" />
<img width="1017" height="503" alt="image" src="https://github.com/user-attachments/assets/499c9e4f-75d8-49cb-b700-cb277b33918d" />

<img width="1026" height="508" alt="image" src="https://github.com/user-attachments/assets/a57f9202-b631-4135-9892-7971b149b186" />
<img width="997" height="493" alt="image" src="https://github.com/user-attachments/assets/a01b60c7-ea7f-475d-adad-6de2d854922b" />


---
> **Academic Integrity Note:** The original source code is maintained in a private repository to comply with university policies. This public repository serves as a showcase for methodology, dynamics, and analytical results.
