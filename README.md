# CS854: Fall 25 - Model Serving Systems for GenAI

## Course Description
Generative AI (GenAI) applications are revolutionizing the world. The latest GenAI models such as GPT-4 have achieved unprecedented performance in various tasks such as code generation, text classification, and problem reasoning. However, serving GenAI applications, i.e., deploying trained GenAI models on a compute cluster and conducting model inference for incoming user requests, presents challenges in systems design. 

This seminar-based course will introduce you to the key concepts and the state-of-the-art in model serving systems for emerging Generative AI (GenAI) and encourage you to think about either building new tools or applying an existing one in your own research. The course will cover various important topics for serving systems for GenAI, including efficient batching, memory/cache management, request scheduling and load balancing, and compound AI systems such as Retrieval-Augmented Generation. Note that this course is **NOT focused on AI methods**. Instead, we will focus on how to build efficient serving systems for existing AI methods. 


### Prerequisites
Students are expected to have strong programming skills and have completed at least one undergraduate-level systems-related course, such as Operating Systems, Databases, Distributed Systems, or Computer Networks. While an undergraduate course in Machine Learning or Artificial Intelligence would be beneficial, it is not a requirement.

### Textbook and Exams
This course has **no** textbooks or exams.
We will read recent papers to understand trends and important topics in serving systems for GenAI.

## Tentative Schedule and Reading List
*This is an evolving list and the schedule is subject to changes.* 

| Date    | Readings                       | Presenter |   Reviewer
| --------| -------------------------------| --------- |   -------
| Sept 6  | **Introduction** | Hong
|         | [How to Read a Paper](http://svr-sk818-web.cl.cam.ac.uk/keshav/papers/07/paper-reading.pdf) 
|         | [How to Give a Bad Talk](http://www.cs.berkeley.edu/~pattrsn/talks/BadTalk.pdf) 
|         | [Writing Reviews for Systems Conferences](http://people.inf.ethz.ch/troscoe/pubs/review-writing.pdf)
|         | [LLM Inference Serving: Survey of Recent Advances and Opportunities](https://arxiv.org/pdf/2407.12391)
|         | [Towards Efficient Generative Large Language Model Serving: A Survey from Algorithms to Systems](https://arxiv.org/pdf/2312.15234)   
|         | [The Datacenter as a Computer](https://link.springer.com/book/10.1007/978-3-031-01761-2) (Chapters 1 and 2, optional)
|         | [The Llama 3 Herd of Models](https://arxiv.org/abs/2407.21783) (optional)
| Sept 13 | **Serving Systems for GenAI _vs._ Serving Systems for traditional DNN** 
|         | [The Illustrated Transformer](https://jalammar.github.io/illustrated-transformer/) (Required) | Xiaodian
|         | [The Illustrated GPT2](https://jalammar.github.io/illustrated-gpt2/) (optional)
|         | [Attention is All You Need](https://dl.acm.org/doi/10.5555/3295222.3295349) (optional)
|         | [Serving DNNs like Clockwork: Performance Predictability from the Bottom Up](https://www.usenix.org/system/files/osdi20-gujarati.pdf) (Required) |Hong
|         | [Orca: A Distributed Serving System for Transformer-Based Generative Models](https://www.usenix.org/system/files/osdi22-yu.pdf) (Required) |Hong
| Sept 20 | **Memory Management**
|         | [Efficient Memory Management for Large Language Model Serving with PagedAttention](https://dl.acm.org/doi/10.1145/3600006.3613165) (Required) | Prashanth | Sairaj 
|         | [vAttention: Dynamic Memory Management for Serving LLMs without PagedAttention](https://arxiv.org/abs/2405.04437) (Required) | Wenhao | Xiaodian
|         | [FlexGen: High-Throughput Generative Inference of Large Language Models with a Single GPU](https://proceedings.mlr.press/v202/sheng23a.html) (Required) | Hongzhou
|         | [LLM in a flash: Efficient Large Language Model Inference with Limited Memory](https://arxiv.org/pdf/2312.11514) (optional)
| Sep 27  | **Prefill _vs._ Decode**
|         | [Distserve: Disaggregating Prefill and Decoding for Goodput-optimized Large Language Model Serving](https://www.usenix.org/system/files/osdi24-zhong-yinmin.pdf)  (required)  | Gaurav | Khushee
|         | [Splitwise: Efficient generative LLM inference using phase splitting](https://arxiv.org/pdf/2311.18677) (Optional)
|         | [SARATHI: Efficient LLM Inference by Piggybacking Decodes with Chunked Prefills](https://arxiv.org/pdf/2308.16369) (required)   | Ronak | Eric
|         | [Taming Throughput-Latency Tradeoff in LLM Inference with Sarathi-Serve](https://arxiv.org/pdf/2403.02310) (Required)   | Michael |  
|         | [Mooncake: A KVCache-centric Disaggregated Architecture for LLM Serving](https://arxiv.org/pdf/2407.00079) (Optional)
| Oct 4   | **Parallelism**
|         | [AlpaServe: Statistical Multiplexing with Model Parallelism for Deep Learning Serving](https://www.usenix.org/system/files/osdi23-li-zhuohan.pdf) (Required)  |   Kerem | Amir
|         | [Liger: Interleaving Intra- and Inter-Operator Parallelism for Distributed Large Model Inference](https://dl.acm.org/doi/abs/10.1145/3627535.3638466) (Required)     |  Dongfu | Bishwajit
|         | [LoongServe: Efficiently Serving Long-context Large Language Models with Elastic Sequence Parallelism](https://arxiv.org/pdf/2404.09526) (Required)    |  Benjamin | Wenhao
| Oct 11  | **Scheduling**
|         | [Fast Distributed Inference Serving for Large Language Models](https://arxiv.org/pdf/2305.05920) (Required)        |  Khushee |  Ronak
|         | [Response Length Perception and Sequence Scheduling: An LLM-Empowered LLM Inference Pipeline](https://arxiv.org/pdf/2305.13144) (Optional)     
|         | [Llumnix: Dynamic Scheduling for Large Language Model Serving](https://www.usenix.org/conference/osdi24/presentation/sun-biao) (Required)  |   Eric |   Michael
|         | [Andes: Defining and Enhancing Quality-of-Experience in LLM-Based Text Streaming Services](https://arxiv.org/pdf/2404.16283) (Required)  |   Rui Felipe |  Gaurav
|         | [ExeGPT: Constraint-Aware Resource Scheduling for LLM Inference](https://dl.acm.org/doi/pdf/10.1145/3620665.3640383)(Optional)
|         | [Aladdin: Joint Placement and Scaling for SLO-Aware LLM Serving](https://arxiv.org/pdf/2405.06856) (Optional)
| Oct 25  | **Faster Decoding + Project Proposal**
|         | [SpecInfer: Accelerating Large Language Model Serving with Tree-based Speculative Inference and Verification](https://dl.acm.org/doi/10.1145/3620666.3651335) (Required) | Sairaj | Hongzhou
|         | [Break the Sequential Dependency of LLM Inference Using Lookahead Decoding](https://arxiv.org/pdf/2402.02057) (Optional) 
| Nov  1  | **Compound AI Systems**
|         | [Parrot: Efficient Serving of LLM-based Applications with Semantic Variable](https://www.usenix.org/system/files/osdi24-lin-chaofan.pdf) (Required)   | Amir | Rui Felipe
|         | [Teola: Towards End-to-End Optimization of LLM-based Applications](https://arxiv.org/abs/2407.00326) (Required)     |   Hongzhou    | Dongfu
|         | [ALTO: An Efficient Network Orchestrator for Compound AI Systems](https://arxiv.org/pdf/2403.04311) + [Conveyor: Efficient Tool-aware LLM Serving with Tool Partial Execution](https://arxiv.org/pdf/2406.00059) (Optional)
|         | [INFERCEPT: Efficient Intercept Support for Augmented Large Language Model Inference](https://arxiv.org/pdf/2402.01869) (Required) |  Ronak    | Benjamin
|         | [The Shift from Models to Compound AI Systems](https://bair.berkeley.edu/blog/2024/02/18/compound-ai-systems/) (Background)
| Nov 8   | **Invited talks**
|         | [Punica: Multi-Tenant LoRA Serving](https://proceedings.mlsys.org/paper_files/paper/2024/file/054de805fcceb78a201f5e9d53c85908-Paper-Conference.pdf) (Invited Talk)  | [Lequn Chen](https://abcdabcd987.com/about/)
|         | [dLoRA: Dynamically Orchestrating Requests and Adapters for LoRA LLM Serving](https://www.usenix.org/conference/osdi24/presentation/wu-bingyang) (Optional)
|         | [S-LoRA: Serving Thousands of Concurrent LoRA Adapters](https://arxiv.org/abs/2311.03285) (Optional)
|         | [LoRA: Low-Rank Adaptation of Large Language Models](https://openreview.net/forum?id=nZeVKeeFYf9) (Optional)
|         | Serving and evaluating LLMs in the wild  (Invited Talk)  | [Hao Zhang](https://cseweb.ucsd.edu/~haozhang/)
| Nov 15  | **Serving with Retrieval-Augmented Generation**
|         | [Prompt Cache: Modular Attention Reuse for Low-Latency Inference](https://arxiv.org/pdf/2311.04934) (Required)     |  Xiaodian   | Prashanth          
|         | [RAGCache: Efficient Knowledge Caching for Retrieval-Augmented Generation](https://arxiv.org/pdf/2404.12457) (Required) | Khushee |  Kerem
|         | [CacheBlend: Fast Large Language Model Serving for RAG with Cached Knowledge Fusion](https://arxiv.org/abs/2405.16444) (Required) | Prashanth |  Michael, Rui Felipe
| Nov 22  | **Serving in the Wild**
|         | [SpotServe: Serving Generative Large Language Models on Preemptible Instances](https://arxiv.org/pdf/2311.15566) (Optional)
|         | [ServerlessLLM: Locality-Enhanced Serverless Inference for Large Language Models](https://arxiv.org/pdf/2401.14351)  (Required) | Eric  | Gaurav, Amir
|         | [M´elange: Cost Efficient Large Language Model Serving by Exploiting GPU Heterogeneity](https://arxiv.org/pdf/2404.14527) (Optional) 
|         | [Helix: Distributed Serving of Large Language Models via Max-Flow on Heterogeneous GPUs](https://arxiv.org/pdf/2406.01566) (Optional)
|         | [Stateful Large Language Model Serving with Pensieve](https://arxiv.org/pdf/2312.05516) (Optional)
|         | **Other Important Topics (Cache management, Multi-tenancy, MoE, Fairness, Serving Simulator Design, etc.)**
|         | [InfiniGen: Efficient Generative Inference of Large Language Models with Dynamic KV Cache Management](https://arxiv.org/pdf/2406.19707) (Required) | Dongfu  | Benjamin, Sairaj
|         | [CacheGen: KV Cache Compression and Streaming for Fast Large Language Model Serving](https://arxiv.org/abs/2310.07240) (Optional)
|         | [Cost-Efficient Large Language Model Serving for Multi-turn Conversations with CachedAttention](https://arxiv.org/abs/2403.19708) (Optional)
|         | [Infinite-LLM: Efficient LLM Service for Long Context with DistAttention and Distributed KVCache](https://arxiv.org/abs/2401.02669) (Optional)
|         | [Fairness in Serving Large Language Models](https://www.usenix.org/conference/osdi24/presentation/sheng) (Required)  | Wenhao   |  Kerem
|         | [DeepSpeed-MoE: Advancing Mixture-of-Experts Inference and Training to Power Next-Generation AI Scale](https://arxiv.org/abs/2201.05596) (Optional)
|         | [MuxServe: Flexible Spatial-Temporal Multiplexing for Multiple LLM Serving](https://openreview.net/forum?id=R0SoZvqXyQ) (Optional)
|         | [Mixture of LoRA Experts](https://openreview.net/forum?id=uWvKBCYh4S) (Optional)
|         | [Vidur: A Large-Scale Simulation Framework For LLM Inference](https://arxiv.org/abs/2405.05465) (Optional)
|         | [LLMServingSim: A HW/SW Co-Simulation Infrastructure for LLM Inference Serving at Scale](https://arxiv.org/abs/2408.05499v1) (Optional)
| Nov  29 | **Final Project Presentations**


