# AI Lecture Projects – Spring 1404  

This repository contains two main projects developed for the **Artificial Intelligence lecture (Spring 1404)** at SUT.  
Our group implemented and experimented with **Image Segmentation** (Computer Vision) and **Soft Actor-Critic (SAC)** (Reinforcement Learning).  

---

## Projects Overview  

### Project 1. Image Segmentation  
**Goal:** Segment objects of interest from images by assigning each pixel to a class label.  

**Key Points:**  
- Implemented classical and deep learning-based segmentation methods.  
- Preprocessing pipeline includes normalization, augmentation, and resizing.  
- Model trained on  Massachusetts Road Dataset

**Results:**  
- Achieved [insert metric results] on the test set.  
- Visualized segmentation masks alongside original images for comparison.  

## Project 2: Soft Actor-Critic (SAC)

### Introduction
Soft Actor-Critic (SAC) is a **modern reinforcement learning algorithm** that combines the strengths of **policy gradient methods** (actor-critic) with the principle of **entropy maximization**. By encouraging exploration, SAC often achieves more stable learning compared to traditional RL methods.  

### Description
The SAC algorithm is built on three main ideas:  

1. **Actor-Critic Framework**  
   - The *actor* outputs a probability distribution over actions.  
   - The *critic* estimates the value (Q-function) of state–action pairs.  

2. **Entropy Maximization**  
   - SAC does not only maximize expected reward, but also adds an **entropy term** to its objective.  
   - This encourages the policy to remain stochastic and explore more diverse actions instead of converging too early to suboptimal behavior.  

3. **Off-Policy Learning**  
   - Unlike on-policy methods (like PPO), SAC reuses past experiences stored in a **Replay Buffer**, making it more sample-efficient.  

Mathematically, the SAC objective is:  

\[
J(\pi) = \mathbb{E}_{(s,a) \sim \pi} \Big[ Q(s, a) + \alpha \, \mathcal{H}(\pi(\cdot|s)) \Big]
\]

where  
- \( Q(s, a) \): estimated value of action \(a\) in state \(s\),  
- \( \mathcal{H} \): entropy of the policy (how random it is),  
- \( \alpha \): temperature parameter controlling the trade-off between reward and exploration.  

In practice, SAC achieves **robust, stable, and high-performing policies** on continuous control tasks (like robotics or physics simulators).  



### Implementation
- Replay Buffer for experience storage  
- Actor-Critic neural networks  
- Entropy-regularized objective for improved exploration  
- Training with mini-batches sampled from buffer  


---
