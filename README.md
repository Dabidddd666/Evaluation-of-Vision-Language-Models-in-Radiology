# Undergraduate_Research
This is my undergraduate research project with Professor João Sedoc.

## Research Proposal
### Title
Development of an Advanced Medical Visual Question Answering System Using Multimodal Models.
### Introduction
The advent of Vision Language Models (VLMs) such as Flamingo has marked a new era in AI, particularly in the processing of interleaved visual and textual data. This research aims to harness these advances to develop a medical visual question answering system. The system will analyze medical imaging, generating relevant responses in text or visual format, thereby aiding medical diagnostics and patient care.
### Background
Recent strides in VLMs, including adaptations for the medical field like Med-Flamingo, highlight the immense potential of these models. However, challenges persist in contextual understanding of multimodal medical data. Models like CheXzero showcase the potential of deep learning in interpreting medical images without extensive manual annotations, a direction our research intends to expand upon.
### Objectives
* To create a versatile system that can process and analyze medical imaging, offering insights and interpretations through a combination of text and images.
Target specific medical imaging types (e.g., MRI, CT scans) and conditions, enhancing the model's applicability in real-world medical scenarios.
Achieve adaptability across various medical specialties, ensuring comprehensive applicability of the system.
### Methodology
#### Pre-training Process
Vision Encoder: Adoption of the NFNet F6 model for its proficiency in converting pixels to features, tailored to medical images.
Language Encoder: Utilization of the BERT architecture for its exceptional performance in natural language understanding, critical for parsing medical literature.
#### Vision-Language Embedding Integration
Detailed process of training the vision and language encoders in tandem, with emphasis on achieving a shared, normalized embedding space.
Implementation of a dual Contrastive Loss mechanism using CLIP, enhancing the model's ability to correlate text and image data accurately.
#### Enhanced Evaluation with BERT-Sim
Application of BERT-Sim to evaluate semantic similarities, ensuring a more nuanced and accurate assessment of the model's output compared to traditional metrics.
#### Dataset Expansion Using GPT-4
Utilization of GPT-4's generative capabilities to create an enriched and diverse set of medical questions, aiding in the fine-tuning process and ensuring the model's exposure to a wide array of medical scenarios.
#### Ensemble Refinement (ER) for Improved Accuracy
Concept: Implement ER, a novel prompting strategy combining chain-of-thought and self-consistency techniques for refined model outputs.
Two-Stage Process:
Stage 1: Generate multiple potential answers using temperature sampling, each comprising an explanation and answer.
Stage 2: Condition the model on the original prompt, question, and Stage 1 generations, refining explanations and answers iteratively. A plurality vote over these answers will determine the final output.
### Experiments
#### Datasets
NYU fastMRI: This dataset has been provided by NYU Langone and mainly consists of raw k-space data divided into multiple sub-dataset groups. The dataset is de-identified and has been approved by an IRB for research purposes. Additionally, precautions were taken to remove any traces of PHI (Protected Health Information).
MIMIC-CXR: This is a massive, publicly accessible dataset of chest X-rays in DICOM format which is paired with free-text radiology reports. It houses 377,110 images taken from 227,835 radiographic studies at the Beth Israel Deaconess Medical Center, Boston, MA. Like the NYU fastMRI, the MIMIC-CXR dataset also has been meticulously de-identified to ensure the removal of all PHI, compliant with the US Health Insurance Portability and Accountability Act of 1996 (HIPAA) Safe Harbor regulations.
### Evaluation
The evaluation of our Medical Visual Question Answering System will be comprehensive, utilizing a blend of traditional metrics and advanced techniques to ensure a thorough assessment of the model's performance.
#### Traditional Metrics
Accuracy: Measure the percentage of correctly answered questions to evaluate the basic performance of the system.
Precision and Recall: Assess the system's ability to provide relevant and accurate answers, especially important in medical diagnostics where accuracy is paramount.
Response Time: Evaluate the efficiency of the system in processing queries and generating responses, an essential factor in clinical settings.
#### Advanced Methods
BERT-Sim: Employ BERT-Sim for a nuanced evaluation, comparing semantic similarities between the model's outputs and the correct answers. This approach is particularly effective in understanding the model's capability to capture complex medical terminologies and concepts.
#### Utilization of Specific Datasets
VQA-RAD: a manually constructed VQA dataset in radiology where questions and answers about images are naturally created and validated by clinicians. Trading off quantity of automatic generation, VQA-RAD is a high-quality design with only 60 hours of specialist contributions.
Path-VQA: PathVQA consists of 32,799 open-ended questions from 4,998 pathology images where each question is manually checked to ensure correctness.
### Risks and Limitations
Overfitting to Training Data: There's always a risk that the system might overfit to specific datasets or types of questions during its training phase. This can reduce the model's capability to generalize to novel and unseen data, making its real-world application limited.
Computational Overhead: The proposed system, given its intricacy and reliance on multiple models and components, could prove to be computationally intensive. This can limit its scalability and usability, especially in resource-constrained settings.
Dependency on High-Quality Annotations: The model's performance heavily relies on the quality of data annotations, particularly for fine-tuning. Poor or inconsistent annotations can hamper the model's ability to produce accurate results.
Transferability to Diverse Medical Domains: While the system is designed to be general-purpose, its effectiveness might vary across different medical specialties. Results on a radiology dataset might not necessarily translate to equal success in, say, dermatology.
#### Ethical Considerations and Patient Privacy
Emphasis on ethical data usage, ensuring patient confidentiality and consent, and adherence to medical data regulations.
Impact and Future Directions
Exploration of the system's potential impact on healthcare, including patient outcomes and diagnostic processes.
Future scalability plans, integration possibilities with existing healthcare systems, and ongoing improvement strategies based on professional feedback.
### Conclusion
This research proposal outlines a comprehensive plan to develop a state-of-the-art medical visual question answering system. Leveraging advanced AI technologies and methodologies, this system aims to revolutionize medical imaging analysis and enhance healthcare delivery.


