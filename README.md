# VU Amsterdam - Computer Security

An overview of the courses I took during my Master's in [Computer Security](https://vu.nl/en/education/master/computer-security/curriculum) at VU Amsterdam.
Course content and assignments may vary both by academic year and by students' selection from available assignment options.

## Mandatory Courses

### [Software Security](https://studiegids.vu.nl/en/Master/2023-2024/computer-security/X_400127#/)

<details>
<summary>Content:</summary>

- Vulnerabilities and Attacks:
  + Buffer overflow
  + Integer overflow
  + Uninitialized variables
  + C++ Type Confusion
  + Format strings
  + Shellcode injection
  + ROP
  + Blind ROP
  + DOP
  + Use After Free
  + Double Free
  + Kernel exploits with Spectre
- Defenses:
  + Canary
  + DEP
  + ASLR
  + Shadow Stack
  + CFI 
- Web Security:
  + Session fixation
  + XXS, CSRF
  + SSRF, XXE
  + HTTP request Smuggling
  + SQLI
  + Type juggling
  + Command injection
  + SOP, CSP, CORS
- Advanced Topics:
  + Automatic Exploit Generation
  + Fuzzing (Generation, Mutational)
  + Sanitizers (ASan, TSan, UBSan, ...)

Practical assignments on the topics seen during the lectures.

Most interesting papers:

- Unwinding The Stack For Fun and Profit
- The Dynamics of Innocent Flesh on the Bone: Code Reuse Ten Years Later
- DangZero: Efficient Use-After-Free Detection via Direct Page Table Access
- FloatZone: Accelerating Memory Error Detection using the Floating Point Unit
- Speculative Probing: Hacking Blind in the Spectre Era
- Hacking Blind

</details>

### [Network Security](https://studiegids.vu.nl/en/Master/2023-2024/computer-security/XM_0100#/)

(Not mandatory from 2024)

<details>
<summary>Content:</summary>

- TCP attacks:
  + Sniffing
  + Spoofing (On-path, Off-path)
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

Practical assignments:
  + Mitnick attack
  + Kaminsky attack

Most interesting papers:
  + Off-Path TCP Exploits: Global Rate Limit Considered Dangerous
  + Off-Path TCP Exploits of the Mixed IPID Assignment
  + DNS Cache Poisoning Attack Reloaded: Revolutions with Side Channels
  + DNS Cache Poisoning Attack: Resurrections with Side Channel
  + How Great is the Great Firewall? Measuring China’s DNS Censorship
  + Weaponizing Middleboxes for TCP Reflected Amplification
  + Detection, Classification, and Analysis of Inter-Domain Traffic with Spoofed Source IP Addresses
  + An End-to-End Measurement of Certificate Revocation in the Web’s PKI
  + Geneva: Evolving Censorship Evasion Strategies

</details>


### [Binary and Malware Analysis](https://studiegids.vu.nl/en/Master/2023-2024/computer-security/X_405100#/)

<details>
<summary>Content:</summary>

- Dynamically linked ELF (with glibc) execution flow
- Anti-Analysis techniques:
  + Anti-debugging
  + Anti-VM
  + Anti-disassembly (Return address patching, Opaque predicates)
  + Obfuscation
  + Packers
- PIN framework
- Dynamic Taint Analysis
- Static analysis automation
- Automatic data structure recovery
- Symbolic execution
- Lifters

Practical assignments on the topics seen during the lectures.

</details>

### [Advanced Operating Systems](https://studiegids.vu.nl/en/Master/2024-2025/computer-security/XM_40014#/)

<details>
<summary>Content:</summary>

- Boot process and 2-stage bootloader
- Memory Management:
  + UMA vs NUMA
  + Nodes, Zones, Pages
  + Allocators: Memblock, Buddy, Slab, vmalloc
  + Page tables:
    * Initialization
    * MMU
    * Walk
    * Permissions
    * Security
    * TLB
    * KASLR
    * Huge Pages
- User mode & Interrupts:
  + GDT
  + IDT
  + TSS
  + Priviliges
  + KPTI
  + ASLR
  + System Calls
  + VDSO
- Paging:
  + Page fault handling (Kernel vs User)
  + VMAs
  + Memory mappings
  + Transparent Huge Pages (THP)
- Multiprocess:
  + fork(), exec()
  + COW
  + Time Management:
    * Real Time Clock
    * HPET
    * APIC
  + Schedulers:
    * O(1)
    * CFS
  + IPC:
    * System V vs POSIX
    * Shared Memory
    * Semaphores
    * Message Queues
    * tmpfs
- Multicore
  + APIC, ACPI, RSDP, MADT, IPIs
  + Starting APs
  + Kernel locking (Fine grained vs Biglock)
  + Spinlock, Mutexes, RCU
  + Bottom Halves, SoftIRQs, Tasklets
- Page Reclaiming:
  + Memory pressure and page reclaiming
  + Cache shrinking
  + OOM killing
  + Swapping
  + Compression (zram, zswap, zcache)
  + Deduplication (KSM)

Practical Assignments:

Build a multicore multitask fine grained locked kernel based on [OpenLSD](https://github.com/vusec/aos-labs-2024) for x86-64.

Bonus Assignments:

1. Security sanitizers for buddy allocator (page guard, UAF/double free detection)
2. Huge Pages support
3. KPTI
4. Vsyscall
5. exec() syscall, zero page deduplication
6. Kernel threads, core hotplug, sched affinity
7. User space ASAN

</details>

### [Hardware Security](https://studiegids.vu.nl/en/Master/2024-2025/computer-security/XM_40019#/)

<details>
<summary>Content:</summary>

- DRAM
  + Organization (Channel, DIMM, Rank, Chip, Bank, Row/Column)
  + Row Buffer
  + Open/Closed Row Policy
  + DRAM Address Mapping
  + Side-channel attacks
  + Rowhammer and mitigations
- CPUs:
  + Caches:
    * Levels
    * Inclusivity
    * Indexing and Tagging
    * Sets in L1, L2, L3
    * Flush+Reload
  + Meltdown
  + Spectre-v1
  + Mitigating Transient Execution Attacks
  + Spectre-v2:
    * BTI
    * Aliasing
    * Bypassing eIBRS
    * Retbleed
    * Inception
  + Advanced Cache Attacks:
    * Building eviction sets
    * Prime+Probe
    * Evict+Time
    * TLB eviction
    * Prime+Abort
    * Prime+Scope
- Embedded Systems:
  + Communication protocols (I^2C, SPI, UART, etc) and Bus Attacks
  + Firmware analysis
  + ARM exploitation and defenses

Assignments:

- Implement partially "DRAMA: Exploiting DRAM Addressing for Cross-CPU Attacks" to leak information about the geometry of memory addresses in DRAM.
- Flush+Reload, Meltdown and Meltdown+Spectre
- Analyze embedded firmware and communication protocols
- Rehosting, ROP and shellcode on ARM

The final project for microarchitectural security was to implement a privilege escalation exploit by chaining three hardware vulnerabilities:

- CrossTalk: Speculative Data Leaks Across Cores Are Real
- Rage Against the Machine Clear: A Systematic Analysis of Machine Clears and Their Implications for Transient Execution Attacks
- RIDL: Rogue In-Flight Data Load

</details>

### [Systems Seminar](https://studiegids.vu.nl/en/Master/2023-2024/computer-security/XM_0122#/)

<details>
<summary>Content:</summary>

- Reviewed papers:
   + Hello Bytes, Bye Blocks: PCIe Storage Meets Compute Express Link for Memory Expansion
   + Direct Access, High-Performance Memory Disaggregation with DirectCXL
   + Hybrid Execution: Combining Ahead-of-Time and Just-in-Time Compilation, VMIL
   + A Distributed and Hybrid Ground Station Network for Low Earth Orbit Satellites
   + Tango or Square Dance? How Tightly Should we Integrate Network Functionality in Browsers?
   + Sidecar: In-Network Performance Enhancements in the Age of Paranoid Transport Protocols
- Artifact evaluation:
   + Risotto: A Dynamic Binary Translator for Weak Memory Model Architectures

</details>

### [Programming Large-Scale Parallel Systems](https://studiegids.vu.nl/en/Master/2023-2024/computer-security/XM_40017#/)

<details>
<summary>Content:</summary>

- Processors Topologies (Mesh, Tree, Hypercube)
- Parallel Machines (Processor arrays, GPUs, NUMA, DSM)
- Parallel Algorithms:
  + Matrix Multiplication
  + Successive Over Relaxation
  + All-pairs Shorts Paths
  + Solving Linear Equations (Jacobi, Gaussian)
  + Solving Partial Differential Equations (Conjucate gradient method)
  + Traveling Salesperson Problem
  + Barnes-Hut (with Cost model and Costzones)
  + Transposition Driven Scheduling
- Performance Metrics:
  + Linear, Super linear speedup
  + Amdahl's Law
  + Weak and Strong scalability
- MPI:
  + Sync/Async
  + Buffered/Unbuffered
  + Ready
  + Blocking/Non-Blocking
  + Global Operations (Barrier, Bcast, Gather, Scatter, Reduce)
- Julia:
  + Tasks
  + Sync/Async
  + Channels
  + Distributed computing (Workers, Remote channels, Spawn/Fetch)
  + MPI.jl

Practical assignment: Parallel Floyd's algorithm in Julia with MPI.

</details>

## Elective Courses

### [Cryptographic Engineering](https://studiegids.uva.nl/xmlpages/page/2023-2024-en/search-course/course/110259)

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

Practical assignments:
  + Katan and Rectangle ciphers in RISC-V assembly
  + Present cipher in Verilog with parity check
  + Template attack against AES cipher

Most interesting papers:
  + Atomic-AES: A Compact Implementation of the AES Encryption/Decryption Core
  + Pushing the Limits: A Very Compact and a Threshold Implementation of AES
  + Midori: A Block Cipher for Low Energy
  + Cache-timing attacks on AES
  + Correlation Power Analysis with a Leakage Mode
  + Efficient Template Attacks
  + Differential Fault Analysis on A.E.S

</details>

### [Project Systems Testing](https://studiegids.vu.nl/en/vakken/2023-2024/X_405124#/)

<details>
<summary>Content:</summary>

Project:

 - Implemented `IJON {SET(), MAX()}` for AFL++ in Frida Mode in a scriptable and flexible way.
 - Evaluated the fuzzer using similar examples present in the original IJON paper.
 - Found simple and effective ways to adapt our solution to real world examples (State Transition List).
 - Proposed new improvements to our solution (Separate coverage and state map).

Papers:

 - IJON: Exploring Deep State Spaces via Fuzzing
 - Stateful Greybox Fuzzing (SGFuzz)
 - Fuzzers for Stateful Systems: Survey and Research Directions

</details>

### [Deep Learning](https://dlvu.github.io/)

<details>
<summary>Content:</summary>

- Introduction:
  + Neural Networks
  + Classification and Regression
  + Autoencoders
- Backpropagation (Scalar, Vector, Tensor)
- CNNs and TCNNs
- Tricks:
  + Optimizers (Momentum, Adam)
  + Weight initialization
  + Residual connections
  + Regularization
- RNNs (GRU, LSTMs, ELMo)
- VAEs:
  + Latent variable models
  + KL divergence
  + MMD-VAE
- Graphs:
  + Embeddings
  + GCNs
  + Query embedding
- Transformer architecture
- Diffusion (Naive, Gaussian)
- Generalization problem and Information Bottleneck
- XAI

Assignments:

- Build Neural Network from scratch
- Build a mini version of pytorch
- RNNs
- GNNs

</details>

### [Security and Machine Learning](https://studiegids.vu.nl/en/Master/2023-2024/computer-security/XM_0135#/)

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

This is a non-exhaustive list of papers that I read/skimmed through for the assignments,
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

### [Dynamic Programming and Reinforcement Learning](https://studiegids.vu.nl/en/Master/2023-2024/computer-security/XM_0093#/)

<details>
<summary>Content:</summary>

- Key concepts:
  + Reward
  + State
  + Markov property
  + Policies
  + Transistions
- Dynamic Programming:
  + Shortest path
  + Inventory control
  + Knapsack
  + Stochastic settings (Knapsack, Inventory control, Revenue Management)
- Markov chains:
  + Communicating path
  + Period
  + Time-average
  + Limit and Stationary distribution
  + Poisson equation
- Markov decision chains:
  + Policy iteration
  + Value iteration
  + Bellman Equation
  + Q-Values
  + Discounted rewards
- Continuos time and Markov processes
- Bandits:
  + Gittins index
  + Stateless bandits and Bayesian framework
  + Exploration policies and Thompson sampling
  + Contextual bandits
- Monte-Carlo Tree Search
- Reinforcement Learning
- Deep Learning
- Q-Learning
- Policy Gradient methods

Practical assignments:

  - Stochastic knapsack problem
  - Markov Decision process
  - Connect 4 solver with MCTS
  - Maze solver with Q-Learning

</details>

### [Advanced Machine Learning](https://studiegids.vu.nl/en/vakken/2024-2025/XM_0010#/)

<details>
<summary>Content:</summary>

- Introduction:
  + Matrix properties
  + Vector Calculus
  + Normal Distribution
- Curve fitting and linear regression:
  + Overfitting
  + Order
  + Linear basis function
  + Maximum Likelihood
  + Moore-Penrose pseudo-inverse
  + Regularization
  + Gradient Descent
- Bayesian linear regression
- Classification:
  + Discriminant functions
  + K-class classifier
  + Perceptron algorithm
  + Continuos inputs
  + Logisitc regression
  + Iterative reweighted least squares
- Neural Networks:
  + Activation functions and non-linearity
  + Training
  + Backpropagation
  + Regularization in NN
  + Activation functions
  + Invariances
- Deep Neural Networks:
  + Vanishing and exploding gradient problem
  + Optimization algorithms (Momentum, RMSProp, Adam)
  + Hyperparameter tuning
- Convolutional Neural Networks:
  + Filters
  + Padding and stride
  + Pooling
  + Examples (LeNet, AlexNet, VGG, ResNet, Inception)
  + Object detection
  + Face recognition (Siamese network)
  + Neural style transfer
  + Visualizing deep layers
- Recurrent Neural Networks:
  + Named Entity Recognition
  + Language Modeling
  + GRU
  + LSTM
  + Word Embeddings
  + Beam Search

</details>

### [Performance of Networked Systems](https://studiegids.vu.nl/en/vakken/2024-2025/X_405105#/)

<details>
<summary>Content:</summary>

- Networking principles
- Performance Modeling:
  + Poisson processes and properties
  + Markov chains, equilibrium distributions
  + Erlang-B model
  + Multi-rate models and Kaufman/Roberts recursion
- TCP/IP:
  + QoS mechanisms for IP networks
  + TCP (Slow Start, Flow Control, Congestion Control, Congestion Avoidance, Fast Recovery and Fast Retransmit)
  + HTTP evolution
- Mobile Networks:
  + GSM
  + GPRS 
  + WiFi/802.11 (DCF 4-way handshake)
  + Bianchi's model
  + UMTS and Kelly's Loss Networks
  + 4G and 5G
</details>

## Constrained Choice Course

### [Distributed Algorithms](https://studiegids.vu.nl/en/Master/2023-2024/computer-security/X_400211#/)

<details>
<summary>Content:</summary>

- Logical clocks (Lamport's, Vector)
- Snapshots:
  + Chandy-Lamport (FIFO)
  + Lai-Yang
- Wave:
  + Traversal (Tarry, DFS, Awerbuch, Cidon)
  + Echo
  + Tree
- Deadlock detection (Bracha-Toueg)
- Termination detection:
  + Dijkstra-Scholten, Shavit-Francesz, Rana, Safra
  + Weight Throwing
- Distributed garbage collection:
  + Reference counting (indirected, weighted)
  + Tracing (mark-scan)
- Routing:
  + Chandy-Misra
  + Merlin-Segall
  + Toueg's
- Election algorithms:
  + Ring (Chang-Roberts, Franklin, Dolev-Klawe-Rodeh)
  + Tree 
  + Echo with extinction
  + MST (Gallager-Humblet-Spira)
- Anonymous networks:
  + Itai-Rodeh
  + Echo with extinction
  + Itai-Rodeh Ring Size
- Consensus with fault tolerance:
  + Bracha-Toueg
  + Chandra-Toueg
- Mutual Exclusion algorithms:
  + Ricart-Agrawala
  + Raymond's
  + Agrawal-El Abbadi
- Self-stabliziation (Dijkstra's token ring, Afek-Kutten-Yung)
- Dynamic networks:
  + Chord ring
  + AODV routing
  + Walter-Welch-Vaidya
- Rollback recovery (Peterson-Kearns)
- Distributed transactions:
  + Two-phase locking
  + Time stamps
  + Optimistic concurrency control
  + Two- and Three-phase commit.
- Security:
  + Kerberos
  + Key Exchange (Diffie-Hellman, BB84)
  + Digital signatures (Lamport, Winterniz, Merkle)
  + Bitcoin

</details>

