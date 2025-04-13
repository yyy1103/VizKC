# Presenting Knowledge Clues in a Generated Image? Towards Improving Image-Sequence Reasoning with Assisted Visual Inputs



The full code will be released upon acceptance of the paper.

![image](https://github.com/user-attachments/assets/f5527cca-3d3b-4646-af7a-418b9fac91cd)




Intruduction:
-
Several recent multi-modal large language models (MLLMs) have exhibited powerful abilities in addressing image-sequence reasoning (ISR) tasks. However, significant challenges remain, e.g., it is difficult for the MLLMs to fully capture complicated vision knowledge (e.g., scene, attribute, and named entity) across multiple images, which hinders them from better solving ISR. To alleviate this, we introduce the novel concept Visualized Knowledge Clues (VizKC) that can capture key vision knowledge from raw images and then integrate such knowledge as task clues, which we call knowledge clues, by generating a new image. Accordingly, we propose an accompanying framework named VizKC-ISR, which is composed of two modules: VizKC generation and VizKC utilization. Specifically, in the generation module, we present a see-find-fuse procedure: (i) “See - Scene Perception”, to construct an initial VizKC that incorporates the spatial information of key visual entities detected from the image (i.e., scene-specific knowledge) ; (ii) “Find - Knowledge Generation”, to generate external-knowledge-injected and fine-grained captions about images and then extract named entities and entity details from generated captions (i.e., entity-related knowledge); (iii) “Fuse - Image Editing”, to integrate the extracted knowledge tuples from (ii) into the initial VizKC from (i), thus generating the final VizKC. In the utilization module, we employ a state-of-the-art (SOTA) multi-image MLLM (mPLUG-Owl3) to solve enhanced ISR tasks with VizKC. We evaluate VizKC-ISR on nine ISR benchmarks categorized into three multi-image scenarios (multi-grained comparison, vision-linked reasoning, external-knowledge seeking).

VKC-MIR consists of four stages: 

(1) visual scene perception;

(2) external knowledge generation;

(3) knowledge image editing; 

(4) multi-image reasoning.


![image](https://github.com/user-attachments/assets/e2439e07-8714-4827-95f2-1ebaa2fa6201)


Preprocess datasets： 


MI-Bench: [https://paperswithcode.com/dataset/infoseek](https://huggingface.co/datasets/StarBottle/MIBench)

Large language models and multimodal tools
-
· Prepare Scene graph :
HiKER-SGG:  https://github.com/zhangce01/HiKER-SGGHiKER-SGG 

· Prepare Visualisation tools
graphviz:https://graphviz.org/

· Knowledge Generation:OPT-66B

·Seed-x-edit:https://github.com/AILab-CVC/SEED-X

·Image Object:
GLEE:https://github.com/FoundationVision/GLEE

·Knowledge Caption:

1.real-world caption generation: https://github.com/njucckevin/KnowCap

2.entity-attribute caption generation: https://github.com/JoshuaFeinglass/TROPE


Results:
-

![image](https://github.com/user-attachments/assets/9967d668-20a2-4ee4-af7f-7de77b1fec42)


**Qualitative Analysis**
-
themodel(1)firstattendsthekeywordsofthequestionand
 thekeyentitiesinthequeryimage;(2)thenmatchessimilarparts
 betweentheoriginalimagesandtheirVizKCs;(3)nextconstructs
 theconnectionbetweendifferentVizKCs;(4)andfinallycaptures
 thekeyknowledgerepresentedinaVizKC.Forinstance,avision
 linkcouldbefoundbetweentheanonymousentity“Man1”inthe
 firstVizKCandthenamedentity“LionelMessi”inthelastVizKC.
 
![image](https://github.com/user-attachments/assets/802f0acd-3544-491f-9347-cb75e264995e)






