IDEA/OMEIFE INTERNSHIP - TEAM FOUR 

📌 Overview
This repository contains the work completed by Team Four during our 3-months internship period with OMEIFEI DIGITAL GROUP OF COMPANIES.
One of our main focus during the period of the intership was medically related data gathering; 
We also went through the process of building a chatbot which was meant to answer questions and give non-critical advice, the model was fine-tuned to enable it respond better to questions asked.
This GitHub repository has an inclusion of the following:
1. Datasets some of which were used to build the chatbot,
2. Data processing notebooks
3. 
4. Documentation of our research process.

🩺 Internship Task
We were tasked with:

Gathering high-quality medical text datasets in multiple specialties.
Preprocessing and cleaning these datasets for machine learning.
Experimenting with fine-tuning large language models (LLMs) to create non-critical medical chatbots.
Documenting our data gathering process and findings.
💡 Purpose of Data Gathering
Medical chatbots require domain-specific datasets to:

Answer questions accurately within their field.
Offer safe, non-critical advice and guidance.
Identify cases that require escalation to a doctor. Our goal was to collect specialized datasets so future AI models can give clear, factual, and patient-friendly responses.
🛠 Process & Challenges
1. Data Collection
We gathered five datasets across different medical specialties:

Allergy & Immunology.docx
Questions and Answers under Cardiology.docx
Hematology and Oncology.docx
Pediatric Pulmonology.docx
Oncology.docx
Each dataset was placed in the Datasets/ folder.
Our data gathering report is stored in the Documentation/ folder.

Challenges Faced From our Allergy & Immunology research and other datasets:

Limited updated guidelines for certain rare diseases (e.g., Hyper-IgM syndrome) meant we had to combine older studies with recent meta-analyses.
Region-specific data gaps: Many prevalence studies focused on North America and Europe, with very limited coverage for Africa and Nigeria.
Access restrictions: Several relevant research papers were behind paywalls, forcing us to rely on open-access journals and alternative databases.
Inconsistent diagnostic criteria: Definitions and antibody testing methods varied across studies, affecting data consistency.
Under-recognition in LMICs: Certain diseases (e.g., autoimmune encephalitis) are underreported in low- and middle-income countries.
Hospital-based bias: Many studies were hospital-based instead of population-based, limiting generalizability.
How We Overcame These Challenges

We:

Cross-referenced multiple reputable sources such as PubMed, WHO, CDC, and Cleveland Clinic to verify accuracy.
Used systematic review filters (2019–2025, English-language, meta-analyses, and guidelines) to ensure relevance and quality.
Relied on regional case studies from Nigeria where available.
Incorporated expert consensus guidelines where direct epidemiological data was missing.
Standardized terminology and diagnostic definitions across all datasets to improve consistency.
Focused on patient-friendly summaries without losing medical accuracy.
2. Data Preprocessing
We:

Converted .docx datasets into plain text.
Removed duplicate and irrelevant entries.
Standardized formatting for chatbot training.
3. Model Experiments
Used Hugging Face Transformers and PEFT LoRA to fine-tune models.
Created the notebook Medical Chatbot GPT [Pediatric Pulmonology].ipynb (stored in Notebooks/).
Tested multiple model sizes, including TinyLlama-1.1B for CPU training.
4. Challenges & Solutions
Model training on CPU was extremely slow: We optimized with smaller models and LoRA.
Limited RAM: We reduced dataset size during debugging and testing.
Tokenizer padding issues: Fixed by setting pad_token for LLaMA-based models.
Loss computation errors: Solved by adding labels during tokenization.
📊 Outcome – Skills & Discoveries
During this project, we gained hands-on experience in:

Data collection & preprocessing for NLP.
Dataset formatting for instruction-based fine-tuning.
Tokenization, embedding creation, and model evaluation.
Model fine-tuning using LoRA on CPU.
Building interactive chatbot interfaces with Gradio.
Key discovery:
Training even small LLMs on CPU is possible but very slow —
on our test machine (Intel Core i5-7300), fine-tuning larger models could take days, while smaller models (1–3B parameters) could train in a few hours.

📂 Repository Structure
Datasets/ # Raw medical datasets
Notebooks/ # Jupyter notebooks containing the entire training lifecyle of the model
Documentation/ # Data gathering report and supporting docs
README.md # Main repository summary
🙏 Acknowledgements
Special thanks to OMEIFEI DIGITAL GROUP OF COMPANIES for providing this internship opportunity, guidance, and resources.

About
This medical chatbot offers non-critical advice when made aware of patients symptoms
