**Presenting Knowledge Clues in a Generated Image? Towards Improving
 Image-Sequence Reasoning with Assisted Visual Inputs**
-

The full code will be released upon acceptance of the paper.

<img width="1906" height="1231" alt="image" src="https://github.com/user-attachments/assets/05c196a3-a4ef-4c39-b76f-5bfa742f79aa" />


(a) Our method outperforms a variety of MLLMs, averaged in each task group. (b) Motivation illustration of our novel concept VizKC. (c,d,e) Examples of image-sequence reasoning tasks. (f) Illustration of our method which encompasses two modules: generation and utilization.


**Intruduction:**
  1. We introduce the novel concept VizKC, which integrates visual knowledge as an image rather than as text or features. The extension of textual knowledge representation into visually-grounded, multi-modal clues is both original and impactful. VizKC also enjoys extra advantages, e.g., task-independent and model-agnostic, showing that it can be applicable to a variety of tasks and models. 

  2. We propose the novel framework  VizKC-ISR, which generates VizKC to enhance ISR tasks in MLLMs. The methodological innovations focus mostly on (1) the see-find-fuse generation pipeline systematically organizes and transforms visual and external knowledge into structured visual clues, and (2) extending textual triples to multi-modal, spatially grounded entity descriptions, and explicit categorization of relations provides an interpretable and task-aligned knowledge representation.

 3. Our experiments span nine benchmarks and multiple model categories, including task-specific approaches and single-/multi-image MLLMs. Our method achieves new state-of-the-art (SOTA) results in all tasks, surpassing GPT3-based methods and all MLLMs compared. 
    


**VizKC-ISR consists of four stages**: 

(1) visual scene perception; (VizKC generation)

(2) external knowledge generation; (VizKC generation)

(3) knowledge image editing;  (VizKC generation)

(4) multi-image reasoning. (VizKC utilization)  

**Preprocess datasets：** 
-
We perform experiments spanning nine ISR
benchmarks released by MIBench (Liu et al. 2024b). In
summary, these tasks can be categorized into three scenar-
ios: (i) Multi-Grained Comparison (MGC) which represents
the most fundamental aspect of multi-image capabilities, (ii)
Vision-Linked Reasoning (VLR) which reasons the relation-
ships of objects or events based on the overall content con-
veyed by input images, and (iii) External-Knowledge Seek-
ing (EKS) which queries external knowledge to better an-
swer the question.  
Link: https://huggingface.co/datasets/StarBottle/MIBench

**Large language models and multimodal tools**
-
· Prepare Scene graph :
HiKER-SGG:https://github.com/zhangce01/HiKER-SGGHiKER-SGG 

· Prepare Visualisation tools
graphviz:https://graphviz.org/

· Knowledge Generation: OPT-66B

·Seed-x-edit:https://github.com/AILab-CVC/SEED-X

·Image Object:
GLEE:https://github.com/FoundationVision/GLEE

·real-world knowledge
K-replay:https://huggingface.co/datasets/StarBottle/MIBench.

·entity-aware knowledge
Trope: https://github.com/JoshuaFeinglass/TROPE


<img width="2119" height="1267" alt="image" src="https://github.com/user-attachments/assets/f2f38d3f-0bf0-4df1-8566-61c3d1e9e54d" />



**Results:**

-  VizKC-MIR exhibits superior performance than all other methods and can be implemented with distinct MLLMs.
  
<img width="1981" height="709" alt="image" src="https://github.com/user-attachments/assets/83214979-f7fa-4f74-ba97-f12f2fc23e0e" />




**Qualitative Analysis**

-VizKC enjoys a good interpretability by providing a trace of knowledge clues with related visual concepts.

<img width="1470" height="855" alt="image" src="https://github.com/user-attachments/assets/792c0c50-1926-46ec-9356-7a63e41d337d" />






