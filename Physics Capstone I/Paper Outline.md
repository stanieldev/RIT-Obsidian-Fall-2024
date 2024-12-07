As of 12/6/2024, this is now depreciated and instead is saved on Overleaf.


## Abstract (Complete)
Binary neutron star mergers (BNSMs) are a cornerstone for understanding extreme astrophysical phenomena, offering insights into nuclear microphysics, general relativity, and multi-messenger astronomy. However, high-fidelity simulations of BNSMs are computationally demanding, requiring advanced methods to resolve complex dynamics such as dense nuclear matter, tidal interactions, and gravitational wave emission. In this paper, we explore several optimization techniques to enhance the efficiency and accuracy of these simulations. These include improved equation of state (EoS) calculations through optimized root-finding algorithms and EoS table compression, adaptive mesh refinement (AMR) for dynamic resolution adjustment, and the "table swapping" method to reduce runtime computations. Additionally, we examine parallelization strategies to optimize load balancing and data communication, further enhancing computational performance. By addressing key bottlenecks in simulation workflows, these optimizations aim to push the boundaries of BNSM modeling, enabling more detailed studies of neutron star mergers and their associated astrophysical signatures.


## Background (Complete)
Binary neutron star mergers (BNSMs) are a significant class of astrophysical events, integral for advancing our understanding of fundamental physics and astrophysical processes \cite{chen2024black, foucart2024dynamical}. These systems provide us a natural laboratory to study matter and spacetime under the most extreme conditions, where densities and temperatures of nuclear matter rival those found in stellar cores \cite{magistrelli2024elements, yang2024secondorder}. The dynamics of BNSMs are intricately tied to the properties of neutron-rich matter, offering a rare opportunity to probe of the equation of state (EoS) governing its behavior and properties \cite{kastaun2024modern, pal2024tidal, yelikar2024waveform, mcginn2024rapid, janiuk2024learn, golomb2024using, ecker2024prompt}.

Beyond their inherent physical complexity, BNSMs are central to the rapidly evolving field of multi-messenger astronomy \cite{kastaun2024modern, ascenzi2024neutronstar, pal2024tidal, corsi2024multimessenger, ecker2024prompt}. The first detection of gravitational waves from a BNSM, GW170817 in October 2017 \cite{Abbott_2017, pal2024tidal, kawaguchi2024dimensional, janiuk2024learn}, combined with its accompanying electromagnetic counterparts—kilonovae and short gamma-ray bursts—marked a transformative moment in astrophysics, unlocking new avenues for probing the universe\cite{bhattacharjee2024joint, foucart2024dynamical, pal2024tidal, kawaguchi2024dimensional, jain2024improving, janiuk2024learn, magistrelli2024elements, corsi2024multimessenger}.  These mergers not only illuminate the physics of compact object interactions, but also play a crucial role in explaining the cosmic origin of heavy elements formed via rapid neutron capture (r-process) nucleosynthesis, making them cosmic factories for elements like gold and platinum \cite{magistrelli2024elements, kawaguchi2024dimensional}.

Despite these remarkable advances, significant challenges remain in bridging theoretical predictions with observational data \cite{kastaun2024modern}. High-fidelity simulations of BNSMs are essential for decoding signals from these events, particularly those tied to the EoS, the mass thresholds for neutron star collapse, and the mechanisms driving electromagnetic counterparts \cite{kastaun2024modern, chen2024black}. This study aims to enhance the performance and fidelity of BNSM simulations, addressing critical gaps in understanding the interplay between microphysical processes and their macroscopic manifestations in neutron star mergers.


## Introduction (Complete)
High-fidelity simulations of binary neutron star mergers (BNSMs) are indispensable for accurately modeling the complex interplay of nuclear microphysics, hydrodynamics, and general-relativistic effects. However, the computational demands of these simulations are immense due to the non-linear, multi-scale nature of BNSM dynamics\cite{chen2024black, kawaguchi2024dimensional}. To accurately resolve the dense nuclear matter core, tidal interactions, and the emission of gravitational waves, requires substantial computational resources, often limiting achievable resolution and timescales. Advancing computational methodologies is crucial to bridging this gap and enabling more efficient and precise simulations.

One key area of optimization is improving the equation of state (EoS) calculations. Since the EoS defines the relationship between key thermodynamic quantities, such as pressure $(P)$, density $(\rho)$, and temperature $(T)$, it forms the backbone of any BNSM simulation. However, resolving these properties often involves computationally-expensive root-finding algorithms to interpolate or solve the EoS table at runtime. By implementing optimized algorithms for root-finding and EoS table compression, simulation runtimes can be reduced without compromising physical accuracy or precision. These improvements streamline the retrieval of thermodynamic data, particularly under conditions of rapidly evolving high densities and temperatures.

Another critical enhancement is adaptive mesh refinement (AMR). AMR dynamically adjusts the spatial and temporal resolution of the simulation, providing high-resolution calculations in regions of interest—such as the merging core—while coarsening less dense or dynamic regions\cite{dynamicresolution}. This method reduces computational load while maintaining precision where it matters most. By effectively allocating computational resources, AMR enables the resolution of fine-scale features, such as shock waves and fluid turbulences, which are key to capturing the dynamics of BNSMs.

\begin{figure}
\centering
    \includegraphics[totalheight=8cm]{Figures/dynamicresolution.png}
    \caption{\centering Dynamic Resolution (AMR)\\ Adam Peterson and Don Wilcox\cite{dynamicresolution}}
    \label{fig:verticalcell}
\end{figure}

Parallelization strategies, leveraging high-performance computing (HPC) architecture, are also essential for improving simulation efficiency. Existing simulations already employ significant parallelization to distribute numerically-intensive tasks, such as solving partial differential equations and performing hydrodynamic calculations, across multiple processors\cite{kastaun2024modern}. However, there remains significant room for optimizing and refining these methods to further enhance performance and scalability. By streamlining load-balancing, improving data communication efficiency between processors, and fine-tuning parallel algorithms, substantial reductions in computational overhead can be achieved. These refinements would enable higher-resolution and more physically-realistic models to be executed within practical timescales, improving our ability to capture the intricate details of neutron star mergers and analyze their gravitational wave and electromagnetic signals with greater precision.

Another promising optimization technique is "table swapping," in which a precomputed table replaces an existing one to streamline runtime computations. In this approach, a table that take thermodynamic parameters $A$, $B$, and $C$ as inputs is replaced with a single-time precomputed table parameterized by $X$, $Y$, and $Z$, optimized for the specific needs of the simulation. This new table reduces the computational burden by minimizing the number of interpolations or root-finding steps required during runtime. By shifting part of the computational cost to the pre-simulation phase, the table swap technique can lead to significant speedups in simulations without sacrificing accuracy.

A further avenue for improvement lies in leveraging graphics processing units (GPUs) for computational acceleration. GPUs excel at parallelizing large-scale numerical computations, making them well-suited for tasks such as solving hydrodynamic equations and performing interpolation-heavy operations like those involved in EoS calculations. While the integration of GPU acceleration has the potential to significantly enhance simulation performance, this direction will not be explored in this paper. The focus will instead remain on CPU-based optimization strategies.

In this paper, we explore the different optimization methods—EoS table compression, advanced root-finding algorithms, AMR, and table swapping—for their efficacy and efficiency in enhancing the performance and fidelity of BNSM simulations. By addressing both computational bottlenecks and physical accuracy requirements, our approach aims to push the boundaries of what is computationally feasible for BNSM modeling. These advancements will, not only accelerate current research efforts but also, enable more detailed explorations of the astrophysical processes driving neutron star mergers, their gravitational wave signatures, and their electromagnetic counterparts.


## Literature Review (Complete)
### History of BNSMs Simulations
The simulation of binary neutron star mergers (BNSMs) is a central topic in computational astrophysics, primarily due to its importance in understanding gravitational wave emission, r-process nucleosynthesis, and neutron star physics. Early work in BNSM simulations focused on idealized models, which could only approximate the complex interactions involved in these systems \cite{kastaun2024modern}. However, recent advancements have significantly enhanced the accuracy of these simulations. Modern approaches integrate relativistic hydrodynamics, nuclear equations of state (EoS), and general relativity, while accounting for complex multi-scale phenomena such as shock formation, tidal interactions, and the behavior of matter under extreme densities and temperatures \cite{kastaun2024modern}.

A key simulation techniques had included adaptive mesh refinement (AMR), which dynamically refines the grid resolution based on the evolving features of the merger (e.g., shock waves or high-density regions). This increased computational efficiency by focusing resources on regions of interest while reducing resolution in less-dynamic parts of the system \cite{dynamicresolution}. However, even with AMR, BNSM simulations are computationally expensive due to the large parameter space, the need for high spatial and temporal resolution, and the complexity of the nuclear EoS models.

The use of high-performance computing (HPC) has allowed these simulations to evolve, with large-scale numerical relativity codes such as the Einstein Toolkit facilitating the development of state-of-the-art general-relativistic simulations. The Einstein Toolkit provides core computational infrastructure for modeling BNSMs, supporting a wide range of astrophysical simulations, and enabling the use of supercomputing resources for large-scale, high-fidelity simulations \cite{einsteintoolkit}. These parallelization strategies have significantly improved the speed and accuracy of BNSM simulations; however, despite these advances, there are still notable limitations in computational efficiency, particularly with the handling of the EoS, interpolation routines, and root-finding algorithms.

### Advancements in HPC, Relevant to BNSM Simulations
High-performance computing plays a crucial role in accelerating BNSM simulations. Modern supercomputers, such as Frontera at the University of Texas and Frontier at Oak Ridge National Laboratory, provide the computational power necessary to run large-scale simulations of complex systems like BNSMs. Frontera’s architecture, with its 4.8 teraflops of double-precision calculation capabilities \cite{fronteraspecs}, enables high-resolution simulations, while Frontier, with its exaflop-range capabilities \cite{frontierspecs}, is poised to revolutionize the scale and speed of astrophysical simulations.

Additionally, strategies leveraging multi-core CPUs and GPUs are critical to enhancing the scalability and speed of these simulations. For instance, parallel algorithms for solving partial differential equations (PDEs) and performing hydrodynamic calculations have allowed for significant improvements in simulation times. While much of the focus has been on hardware infrastructure, optimizing the underlying software and computational methods remains essential to fully utilize these advances.

### The Role of the Equation of State (EOS)
The equation of state (EoS) plays a central role in simulating BNSMs, as it dictates the relationship between key thermodynamic variables (such as pressure, density, and temperature) for nuclear matter at extreme conditions \cite{kastaun2024modern}. Accurate EoS calculations are critical to modeling the dynamics of matter within neutron stars and during the merger process. However, EoS table look-ups are computationally expensive, as they often require solving for the roots of a nonlinear equation, making them a significant bottleneck in simulations. Advances in efficient root-finding algorithm compression techniques have been explored to reduce the computational burden of these EoS calculations. Nevertheless, there remains a need for more efficiency that can streamline EoS look-ups without sacrificing physical accuracy.

### Gap Analysis
While BNSM simulations have seen substantial improvements in both accuracy and efficiency, several key areas remain where further advancements are needed. One of the primary bottlenecks in BNSM simulations is the efficiency of EoS look-ups. Despite improvements in root-finding algorithms, the need to interpolate EoS tables during runtime continues to be a major source of computational overhead. Optimizing these algorithms, and leveraging techniques such as table swapping, could help address this limitation and significantly speed up simulations.

Another area for improvement is the optimization of parallelization strategies. Although existing simulations already utilize parallelization extensively, further refinements are possible. These include optimizing load balancing, improving data communication between processors, and fine-tuning parallel algorithms. By addressing these issues, it may be possible to reduce computational overhead and achieve higher resolution simulations with greater computational efficiency.

Additionally, while adaptive mesh refinement (AMR) has proven effective in improving computational efficiency by focusing resources on dynamic regions, further advancements in AMR algorithms could help optimize the balance between computational resource allocation and physical accuracy. Developing more adaptive and intelligent AMR strategies that respond to the evolving dynamics of the merger could enhance simulation precision without incurring additional computational costs.

Finally, while the use of graphics processing units (GPUs) for simulation holds significant promise, it remains an area of future research. While not explored in the current study, the integration of GPUs into the computational workflow could lead to further improvements in simulation speed, especially in tasks that involve heavy numerical computation or interpolation.

In summary, while significant progress has been made in simulating BNSMs, there remain crucial areas where optimization techniques can provide substantial improvements. This study aims to address these gaps, focusing on EoS optimization, root-finding algorithm enhancements, parallelization refinements, and table swapping, in order to push the boundaries of what is computationally feasible for BNSM modeling.

## Methodology (Complete)
### Initial Setup and Computational Environment
This research commenced in the summer of 2024, utilizing the computational resources of the RIT SPORC Cluster to simulate binary neutron star mergers (BNSMs). The SPORC Cluster, equipped with high-performance computing capabilities, provided a robust environment for running large-scale simulations\cite{ritresearch}. The Einstein Toolkit, which serves as the backbone for our simulations, was configured to operate with the Cactus Framework.

Compiling the necessary C code and integrating various libraries were integral steps in this setup. GCC was employed to compile the framework and its associated modules, ensuring compatibility with the SPORC Cluster's architecture. A custom implementation of Lorene and FFTW3 was integrated into the Einstein Toolkit to initialize neutron star data accurately.

### Simulation Setup and Challenges
Once the computational framework was established, the next step involved preparing the Cactus Run File and associated parameter files for simulation. This process required extensive troubleshooting to ensure the compatibility of input files with the specific type of BNSM simulation being conducted. During initial simulation runs, inconsistencies were identified in the input files, which necessitated modifications to align them with the physical parameters and resolution requirements of the study. Addressing these issues was critical for achieving stable and physically meaningful outputs.

### Profiling and Performance Analysis
To identify computational bottlenecks and optimize simulation performance, HPCToolkit was employed as a profiling tool. This software suite is designed to analyze high-performance applications, providing insights into execution efficiency and resource utilization. However, initial attempts to profile the simulation using HPCToolkit were unsuccessful, due to compatibility challenges with the current configuration of the SPORC Cluster and the Einstein Toolkit.

### Ongoing and Future Optimization Efforts
Efforts are ongoing to resolve profiling challenges and fully leverage HPCToolkit for identifying areas of inefficiency, particularly in the equation of state (EoS) calculations, root-finding algorithms, and other computationally intensive processes. Once profiling is operational, targeted optimizations—such as table swapping and adaptive mesh refinement—will be implemented and evaluated for their efficacy in reducing runtime and enhancing simulation accuracy.


## Computational Framework
This study leverages the **Einstein Toolkit**, a widely used open-source software suite for simulating relativistic astrophysical phenomena. At its core is the Cactus Framework, which provides modular, extensible tools for implementing general relativistic and hydrodynamic simulations. The simulations utilize a custom implementation of Lorene for generating neutron star initial data, tailored to the specific needs of binary neutron star mergers (BNSMs). The Einstein Toolkit's extensive documentation and community support facilitate seamless adaptation for our research goals.

The hardware environment for this study consists of computational resources provided by the Center for Computational Relativity and Gravitation (CCRG) at the Rochester Institute of Technology (RIT). Initial testing and simulation runs were conducted on the CCRG's in-house server, which mirrors the architecture of the University of Texas's Frontera system, a petabyte-scale computing facility powered by Intel Cascade Lake processors. Frontera boasts 4.8 teraflops of double-precision computing power, suitable for parallel-intensive computations. Additionally, the CCRG is migrating to Frontier, located at Oak Ridge National Laboratory, the world's first exabyte-scale system. Frontier’s AMD Infinity architecture allows for unprecedented computational speeds, supporting exaflop-scale workloads while maintaining compatibility with x86-64 architecture. This transition ensures access to state-of-the-art computational infrastructure, enabling more demanding simulations in the future.

## Optimization Strategies

### EoS Table Compression
The equation of state (EoS) determines critical thermodynamic relationships—pressure ($P$), density ($\rho$), and temperature ($T$)—and is essential for BNSM simulations. Standard simulations rely on high-resolution EoS tables, which involve extensive interpolation and root-finding operations at runtime, resulting in significant computational overhead. To address this bottleneck, we implement a compression algorithm to reduce table size while preserving its fidelity. This involves approximating high-dimensional data with a sparse, efficiently searchable representation. By minimizing runtime interpolation and storage requirements, EoS table compression streamlines the retrieval of thermodynamic properties, accelerating calculations without sacrificing accuracy.

### Root-Finding Algorithm Optimization
Root-finding operations are integral to solving nonlinear equations derived from the EoS and hydrodynamic conditions. Traditional algorithms such as Newton-Raphson are computationally expensive and sensitive to initial guesses, leading to potential inefficiencies. This research explores optimized variants, including hybrid iterative methods, that combine the robustness of bisection with the rapid convergence of higher-order schemes. By reducing the number of iterations required and improving stability under extreme physical conditions, these enhancements aim to significantly reduce runtime while maintaining numerical precision.

### Adaptive Mesh Refinement (AMR)
AMR dynamically adjusts the spatial and temporal resolution of the simulation grid, providing fine-grained resolution in regions of interest, such as the merging neutron star cores, while coarsening in less dynamic areas. This strategy minimizes computational costs without compromising accuracy. For this study, Berger-Oliger refinement is employed, which integrates error estimation and hierarchical grid structures to target areas requiring higher fidelity\cite{BERGER1984484}. This adaptive approach ensures that critical physical processes, such as shock wave dynamics and fluid turbulence, are resolved at the highest possible resolution while reducing overall computational demands.

## Baseline Profiling
Baseline performance profiling was conducted using the HPCToolki, a software suite designed for high-performance application analysis. Initial profiling efforts focused on identifying computational hotspots within the simulation, including bottlenecks in EoS lookups, root-finding operations, and grid management. While full profiling integration remains a work in progress due to compatibility challenges, these efforts provide preliminary insights into resource allocation and computational inefficiencies, forming a foundation for subsequent optimization efforts.

## Experimental Design
To evaluate the efficacy of the proposed optimization strategies, a series of controlled simulation tests will be conducted:

1. **Baseline Simulations**: Initial runs using unoptimized configurations will establish a benchmark for runtime, memory usage, and resolution accuracy.
2. **EoS Optimization Tests**: The performance of compressed EoS tables will be compared to the standard tables, assessing runtime improvements and interpolation accuracy under varying thermodynamic conditions.
3. **Root-Finding Algorithm Comparisons**: Simulations incorporating optimized root-finding algorithms will be evaluated against traditional methods for convergence speed and stability across different physical regimes.
4. **AMR Performance Evaluation**: The efficiency of adaptive refinement will be tested by comparing fixed-grid simulations with AMR-enabled runs, measuring computational savings and fidelity in resolving small-scale features.

Each test will be performed under identical initial conditions to ensure comparability, with results analyzed to quantify improvements in simulation speed, memory efficiency, and physical accuracy. These evaluations will guide further refinements, ensuring that proposed strategies meet the dual goals of computational efficiency and scientific rigor.




## Results
As of now, the primary focus of this project has been on establishing a robust computational framework necessary for conducting high-fidelity simulations of binary neutron star mergers. While simulation data has not yet been obtained, significant progress has been made toward achieving this goal.
### Setting Up the Computational Environment
The Einstein Toolkit was successfully compiled and configured on the RIT SPORC cluster, leveraging C libraries and the GCC compiler. This required overcoming challenges with compatibility and dependencies to ensure a stable runtime environment. A custom implementation of Lorene was integrated into the toolkit to facilitate accurate equation of state (EoS) handling for neutron star material. This adaptation forms the basis for subsequent simulation accuracy.
### Troubleshooting Input Files and Simulation Consistency
Early attempts to initiate simulations revealed inconsistencies in input file configurations. Extensive debugging and refinement efforts were undertaken to align these files with the physical parameters required for accurate modeling of binary neutron star systems.
### Profiling and Optimization Workflows
Initial steps were taken to profile the computational performance of the simulation environment using HPCToolkit. While a complete performance profile has yet to be generated, this ongoing effort aims to identify bottlenecks and inform future optimization strategies.
### Challenges Addressed
Resolving issues related to software compilation and runtime stability was a significant milestone. These efforts provided valuable insights into the intricacies of high-performance computing environments and laid the groundwork for effective simulation execution.



## Discussion
The initial phase of this project focused on establishing the computational foundation necessary to simulate binary neutron star mergers (BNSMs). While no simulation data has yet been generated, substantial progress has been made in addressing the challenges of setting up and optimizing the simulation environment.

Key achievements include the successful compilation and configuration of the Einstein Toolkit on the RIT SPORC cluster, the integration of Lorene for accurate initial data, and the identification of input file inconsistencies. These milestones highlight the complexity of configuring high-performance computing frameworks for astrophysical simulations but also underscore the importance of a robust foundation for reliable data generation.

A significant area of focus was profiling the simulation environment to identify computational inefficiencies. Initial work with HPCToolkit has paved the way for targeted optimizations, though challenges remain in fully integrating profiling capabilities with the simulation framework. These efforts will inform future improvements in runtime efficiency and scalability.

The work conducted so far also highlights the potential for impactful results once simulations are fully operational. Optimizations such as EoS table compression, advanced root-finding algorithms, and adaptive mesh refinement (AMR) are expected to significantly reduce computational overhead and improve simulation fidelity. These advancements will enable more efficient exploration of BNSM parameter spaces, enhancing the accuracy of gravitational wave predictions and insights into the astrophysical processes driving mergers.

## Conclusion and Future Work
This project represents an important step toward optimizing high-fidelity simulations of binary neutron star mergers. The groundwork laid during this initial phase has resolved key technical challenges and established a functional computational framework, setting the stage for future scientific contributions.

Once fully operational, the optimized simulation environment will provide valuable insights into the complex dynamics of BNSMs, including the behavior of matter at extreme densities, the generation of gravitational waves, and the mechanisms behind r-process nucleosynthesis. These results will contribute to advancing the understanding of neutron star physics and multi-messenger astronomy, bridging the gap between theoretical predictions and observational data.

Moving forward, the focus will be on running initial simulations, validating the computational framework, and refining optimization strategies based on profiling data. With these efforts, this project aims to push the boundaries of what is computationally feasible for BNSM modeling, ultimately enabling more detailed and accurate studies of these astrophysical phenomena.

## Acknowledgments
I would like to express my deepest gratitude to **Dr. Yosef Zlochower** and **Dr. Manuela Campanelli** for their invaluable guidance, expertise, and unwavering support throughout my research. Their mentorship has been instrumental in shaping this project and advancing my understanding of computational astrophysics.

I am grateful to the **Center for Computational Relativity and Gravitation (CCRG)** for granting me access to their state-of-the-art computational resources, especially during periods when SPORC encountered difficulties. Their resources and infrastructure have been crucial for the progress of my work.

Special thanks to **Hasanat Hasan** for assisting in the design of my capstone presentation, providing helpful insights that greatly enhanced its clarity and professionalism. I would also like to thank **Dr. Michael Pierce** for his guidance in navigating project challenges and offering advice that helped me overcome obstacles during critical moments of my research.

Finally, I extend my appreciation to everyone who supported me during this journey, both personally and professionally, making this project possible.



I would like to express my gratitude to **Dr. Yosef Zlochower** and **Dr. Manuela Campanelli** for their mentorship and invaluable guidance throughout my research at the Rochester Institute of Technology (RIT). Their expertise and support have been instrumental in advancing my understanding of computational astrophysics and shaping the direction of this project.

I am also immensely thankful to the **Center for Computational Relativity and Gravitation (CCRG)** for granting me access to their state-of-the-art computational resources, including a high-performance server room critical to ongoing work in numerical relativity and gravitational wave astrophysics. This partnership has provided me with an extraordinary opportunity to engage with cutting-edge tools and methodologies, enabling me to perform high-fidelity simulations of binary neutron star mergers (BNSMs) with accuracy and precision.

Special thanks to **Hasanat Hasan** for assisting in the design of my capstone presentation, providing helpful insights that greatly enhanced its clarity and professionalism. I would also like to thank **Dr. Michael Pierce** for his guidance in navigating project challenges and offering advice that helped me overcome obstacles during critical moments of my research.

Finally, I extend my sincere appreciation to everyone who supported me during this journey, both personally and professionally, helping make this work possible.


## Appendices (Optional)
Include supplementary material like detailed algorithms, additional figures, or tables.