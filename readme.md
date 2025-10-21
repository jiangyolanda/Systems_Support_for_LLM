# **System Support Challenges in Large Language Model Training**

As large language models (LLMs) continue to grow in scale, training them efficiently and reliably across massive GPU clusters has become a fundamental systems challenge. The presentation highlights two major issues: how to make heterogeneous GPUs work efficiently together, and how to ensure stable training even when failures occur.

<img width="1134" height="639" alt="image" src="https://github.com/user-attachments/assets/50264094-403c-42b0-b276-46154d25be72" />


**Challenge 1: Support Large Model Training in Heterogeneous Clusters**
This section discusses the difficulty of training large models on clusters composed of different types of GPUs. Because high-end and low-end GPUs differ significantly in speed and memory, training efficiency can vary by more than nine times across devices. Such imbalance creates serious coordination problems. We introduce adaptive parallel strategies, such as data, pipeline, and tensor parallelism, to intelligently distribute workloads and allow all GPUs, regardless of performance level, to contribute efficiently to large-model training.


<img width="1133" height="638" alt="image" src="https://github.com/user-attachments/assets/af799c70-c712-4033-a1dc-3780d31161ce" />


**Challenge 2: Fault Tolerance for Large-Scale Deep Learning Training**
This section focuses on reliability. When hundreds or even thousands of GPUs train a model over days or weeks, hardware or network failures are inevitable. Traditional systems often crash and must restart from scratch, wasting massive time and cost. To address this, fault-tolerant mechanisms such as checkpointing, dynamic task reassignment, and communication recovery are essential. These enable the system to automatically recover from partial failures, making large-scale training not only fast but also stable and self-healing.

