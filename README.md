# VU Amsterdam - Computer Security

I always forget what I've learned.

## Security Courses

### Software Security

- Shellcode Injection
- ROP
- Blind ROP
- Glibc Heap Exploitation
- ASLR Bypasses
- Automatic exploits generation

### Network Security

<details>
<summary>Content:</summary>

- TCP attacks:
  + Sniffing
  + Spoofing (on-path, off-path)
  + Joncheray-style hijacking
- DoS attacks:
  + Fragmentation
  + SYN flooding
  + Botnets
  + Amplifiers
  + Detection (Sketches)
- DNS attacks:
  + Simple (Kaminsky, Birthday attack)
  + Advanced
- DNS enhancements:
  + DNSSEC
  + DoH
  + ODNS
  + Paged DNS
- PKI:
  + Certificates
  + Certificates types
  + Certificates validation and revocation
  + TLS
  + CT Logs
- CDN
- BGP:
  + Prefix hijacking
  + IRR
  + RPKI
  + Spoofing and filtering strategies
- Censorship:
  + GFW
  + Evasion (Geneva, VPNs)

Most interesting papers:
  + Off-Path TCP Exploits: Global Rate Limit Considered Dangerous
  + Off-Path TCP Exploits of the Mixed IPID Assignment
  + DNS Cache Poisoning Attack Reloaded: Revolutions with Side Channels
  + DNS Cache Poisoning Attack: Resurrections with Side Channel
  + DNS Cache Poisoning Attack Reloaded: Revolutions with Side Channels
  + How Great is the Great Firewall? Measuring China’s DNS Censorship
  + Weaponizing Middleboxes for TCP Reflected Amplification
  + Detection, Classification, and Analysis of Inter-Domain Traffic with Spoofed Source IP Addresses
  + An End-to-End Measurement of Certificate Revocation in the Web’s PKI
  + Geneva: Evolving Censorship Evasion Strategies
</details>


### Binary and Malware Analysis

TODO

### Cryptographic Engineering

<details>
<summary>Content:</summary>

- Mathematics:
  + GCD, XGCD
  + Groups, Rings, Galois Fields
- RISC-V ISA
- Software Optimizations:
  + AES Tbox
  + Multiprecision arithmetic
  + Bitslicing
- Hardware Design:
  + Flow (Synthesis, Simulation, Place & Route)
  + Optimizations:
    * Area
    * Energy
    * Scan Registers
- Hardware Attacks:
  + Cache timing
  + Power Analysis (CPA)
  + Templates
  + Fault injection
  + Information Theory (Entropy, mutual information)
  + Countermeasures:
    * Masking (Boolean with ISW)
    * Hiding (WDDL, MDPL)
    * Time, space, information redundancy
- PUFs
- LWE

Most interesting papers:
  + Atomic-AES: A Compact Implementation of the AES Encryption/Decryption Core
  + Pushing the Limits: A Very Compact and a Threshold Implementation of AES
  + Midori: A Block Cipher for Low Energy
  + Cache-timing attacks on AES
  + Correlation Power Analysis with a Leakage Mode
  + Efficient Template Attacks
  + Differential Fault Analysis on A.E.S

</details>

## Research Oriented Courses

### Security and Machine Learning

<details>
<summary>Content:</summary>

 - Gradient Descent
 - Stochastic Gradient Descent
 - Goal, Variance, Bias, Diversity
 - Classification and Regression
 - RNNs and LSTM
 - LLMs (Embedding, Vector Representation, BERT, Trustworthiness)
 - APUF, iPUF
 - ML Analaysis of PUFs
 - Poisoning Attacks
 - XAI
 - Differential Privacy
 - Fairness and Bias
 - Trusted Computing Base (e.g enclaves)
 - Secure Multi Party Computation and Oblivious Transfer
 - Brain Computer Interface and Idealized Computing

##### Papers

This is a non-exhaustive list of papers that I read for the assignments,
provided by the professor or found by myself.
There are other papers that we have analyzed during the lectures, and other topics
that could be investigated for the assignments.

ML based cryptanalysis:
 - Differential cryptanalysis of DES-like cryptosystems
 - Improving Attacks on Round-Reduced Speck32/64 using Deep Learning
 - An Assessment of Differential- Neural Distinguishers
 - A deep learning aided differential distinguisher improvement framework with more lightweight and universality

XAI:
 - Post hoc Explanations may be Ineffective for Detecting Unknown Spurious Correlation
 - Sanity Checks for Saliency Maps
 - Assessing the (Un)Trustworthiness of Saliency Maps for Localizing Abnormalities in Medical Imaging
 - Guided Integrated Gradients: An Adaptive Path Method for Removing Noise
 - Beyond interpretability: developing a language to shape our relationships with AI.
 - SmoothGrad: removing noise by adding noise

Data Extraction Attacks on LLMs:
 - Training a Helpful and Harmless Assistant with Reinforcement Learning from Human Feedback
 - Extracting Training Data from Large Language Models
 - Quantifying Memorization Across Neural Language Models
 - Trustworthy LLMs: a Survey and Guideline for Evaluating Large Language Models’ Alignment
 - Scalable Extraction of Training Data from (Production) Language Models
 - Membership Inference Attacks against Machine Learning Models

Large Scale Cybernetic/AGI Infrastructure:
 - Advances and open problems in federated learning
 - Blockchain and Federated Learning for Privacy-Preserved Data Sharing in Industrial IoT
 - An integrated brain-machine interface platform with thousands of channels
 - A Survey of Published Attacks on Intel SGX
 - Explainable Artificial Intelligence (XAI): What we know and what is left to attain Trustworthy Artificial Intelligence
 - Targeted backdoor attacks on deep learning systems using data poisoning
 - Split-brain: what we know now and why this is important for understanding consciousness
 - Artificial general intelligence: concept, state of the art, and future prospects
 - The combination of brain-computer interfaces and artificial intelligence: applications and challenges

Ethics And Morality in Security and AI:
 - The moral character of cryptographic work
 - The Russell-Einstein Manifesto
 - What happened to the crypto dream?
 - NSA Spying on America
 - A survey on bias and fairness in machine learning
 - Fairness in machine learning: Lessons from political philosophy
 - Gender shades: Intersectional accuracy disparities in commercial gender classification
 - How do fairness definitions fare? Examining public attitudes towards algorithmic definitions of fairness
 - The Road to Digital Unfreedom: How Artificial Intelligence Is Reshaping Repression
 - The global expansion of AI surveillance
 - The debate on the ethics of AI in health care: a reconstruction and critical review
 - Ai in finance: challenges, techniques, and opportunities
 - Deep neural networks improve radiologists
 - Diagnostic evaluation of a deep learning model for optical diagnosis of colorectal cancer
 - End-to-end lung cancer screening with three-dimensional deep learning on low-dose chest computed tomography
 - Detection of brain activation in unresponsive patients with acute brain injury
</details>


### Systems Seminar

TODO

## CS Courses

### Programming Large-Scale Parallel Systems

TODO

### Dynamic Programming and Reinforcement Learning

- Finite Horizon
- Dynamic Programming
- Bellman-Ford
- Knapsack
- Stochastic Knapsack
- Revenue Management
- Markov Chains
- Poisson and Bellman Equations
- Discounting
- Semi-Markov Process
- Exploration Policies (Thompson Sampling, greedy)
- Gittins Index
- Contextual bandits
- Monte-Carlo Tree Search
- Deep Learning
- Q-Learning
- Policy Gradient methods

### Distributed Algorithms

TODO

