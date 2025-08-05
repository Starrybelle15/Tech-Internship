IDEAS/OMEIFE INTERNSHIP - TEAM FOUR 

GENERAL 📌 OVERVIEW OF THE INTERNSHIP TASKS

This GitHub repository contains a compilation of all the work completed by Team Four during our 3-months internship period with OMEIFEI DIGITAL GROUP OF COMPANIES.

FOCUS OF THE INTERNSHIP

One of our main focus during the period of the intership was medically related data gathering; 
We also went through the process of building a chatbot which was meant to answer questions and give non-critical advice, the model was fine-tuned to enable it respond better to questions asked.
This GitHub repository has an inclusion of the following:
1. Datasets, some of which were used to build the chatbot
2. Data processing notebooks, which also includes a document (.docx) to text (.txt) converter 
3. Documentation of our entire research process, from the first data gathering task to the build of the chatbot.

🩺 TASKS THAT WERE GIVEN DURING THE INTERNSHIP

We were tasked with:
1. Gathering high-quality medical text datasets in multiple specialties.
2. Preprocessing and cleaning these datasets for machine learning.
3. Experimenting with fine-tuning large language models (LLMs) to create non-critical medical chatbots.
4. Documenting our data gathering process and findings.

💡 DATA-GATHERING

Medical chatbots require domain-specific datasets to:
1. Answer questions accurately within their field.
2. Offer safe, non-critical advice and guidance.
3. Identify cases that require escalation to a doctor. Our goal was to collect specialized datasets so future AI models can give clear, factual, and patient-friendly responses.

🛠 CHALLENGES AND PROCESSES THAT OCCURED DURING THE INTERNSHIP

1. Data Collection
We gathered four datasets across different medical specialties:
1. CARDIOLOGY (CONGENITAL HEART DISEASE).docx
2. ENDOCRINOLOGY.docx (part 1 & 2)
3. OPHTHALMOLOGY.docx
4. OTORHINOLARYNGOLOGY.docx (part 1-5)

Each dataset was placed in the Datasets/ folder.
Our data gathering report is stored in the Documentation/ folder.

CHALLENEGS THAT WERE FACED DURING THE GATHERING PROCESS OF THE AFORE MENTIONED DATASETS:

Some challenges were faced during the process of collecting datasets from the different medical specialties, listed below are some of the challenges that were faced. They include: 
1. Limited updated guidelines for certain rare diseases (e.g. Popcorn lungs), which then meant that we had to combine older studies with recent meta-analyses to enable sufficient information was collected on those diseases.
2. Region-specific data gaps: Many prevalence studies focused on North America and Europe, with very limited coverage for Africa and the Sub-Saharan region.
3. Access restrictions: Some relevant research papers by trustworthy hospitals and websites were unavailable for free usage, whic in turn forced us to rely solely on open-access journals, textbooks and alternative databases.
4. Inconsistent diagnostic criteria: There was a lack of consistency between the databases from which we got the data, which made it hard to choose the one that is right, but we decided to pick the most consistent ones.
5. Under-recognition in LMICs: Certain diseases (e.g. Zenkers diverticulumn) are not well reported especially in 3rd world countries which do not have the capacity to conduct a good report.
6. Hospital-based bias: Many studies were based on hospital websites instead of being based on population and statistics report, which thereby has limited our generalizability.

WAYS BY WHICH WE OVERCAME THE AFOREMENTIONED CHALLENGES 

Written below are the ways by which we overcame the challenges we faced during the process of gathering data.

We:
1. Cross-referenced multiple reputable sources such as PubMed, WHO, CDC, and Cleveland Clinic to verify accuracy.
2. Used systematic review filters (2019–2025, English-language, meta-analyses, and guidelines) to ensure relevance and quality.
3. Relied on regional case studies from Nigeria where available.
4. Incorporated expert consensus guidelines where direct epidemiological data was missing.
5. Standardized terminology and diagnostic definitions across all datasets to improve consistency.
6. Focused on patient-friendly summaries without losing medical accuracy.

THE PROCESS OF DATA-PREPROCESSING

We:
1. Converted .docx datasets into plain text.
2. Removed duplicate and irrelevant entries.
3. Standardized formatting for chatbot training.
4. Experimentations with different models to get the best
5. Used Hugging Face Transformers to fine-tune models.
6. Created the notebook Pedbot.ipynb (stored in the Medbot folder).
7. Tested multiple model sizes, including TinyLlama-1.1B for CPU training.

CHALLENGES AND THE SOLUTIONS

1. Model training on CPU was extremely slow: We optimized with smaller models and LoRA.
2. Limited RAM: We reduced dataset size during debugging and testing.
3. Tokenizer padding issues: Fixed by setting pad_token for LLaMA-based models.
4. Loss computation errors: Solved by adding labels during tokenization.

📚 Reliable Sources Used for Data Gathering Mayo Clinic:
1. PubMed Central (PMC)
2. National Institutes of Health (NIH)
3. World Health Organization (WHO)
4. Mayo Clinic
5. Clinical guidelines and educational materials from National Institute of Health (NIH, etc.
6. Additional reputable medical platforms including Medscape and Cleveland Clinic were used

🧪 2. METHODS BY WHICH THE DATA WAS GATHERED:

Keywords: definition, epidemiology, causes, risk factors, etc of the various diseases
Selected: Review articles, meta-analyses, clinical practice guidelines, and patient education content.
Cross-verified data across sources.

Extracted:
Definitions, symptoms, causes, risk factors, diagnosis, treatment, prevention, FAQs, epidemiology, prevention, complications.

💾 File Format and Size of Microsoft Word .docx that were created during the period of this internship which was later converted to .txt for model integration. They include:
1. ENDOCRINOLOGY Part 1.docx - 5.3MB
2. ENDOCRINOLOGY Part 2.docx - 721KB
3. Ophthalmology (EYE AND VISION).docx - 6.7MB
4. OTORHINOLARYNGOLOGY.docx - 4.9MB
5. OTORHINOLARYNGOLOGY Part 2.docx - 4.7MB (might be heavier)
6. OTORHINOLARYNGOLOGY Part 3.docx - 4.6MB
7. OTORHINOLARYNGOLOGY Part 4.docx - 4MB
8. OTORHINOLARYNGOLOGY Part 5.docx - 126KB
9. Team 4 Congenital heart diseases.docx - 2.5MB

📊 Outcome – Skills & Discoveries

During this project, we gained hands-on experience in:
1. Data collection & preprocessing for NLP.
2. Dataset formatting for instruction-based fine-tuning.
3. Tokenization, embedding creation, and model evaluation.
4. Model fine-tuning using LoRA on CPU.
5. Using Google colab when necessary.
6. Building interactive chatbot interfaces with Gradio.

Key discovery:

Training even small LLMs like Mistral.ai and ollama models on CPU is possible but very very slow —
on our test machine (Intel Core i5-8300), fine-tuning larger models could take days, while smaller models (1–3B parameters) could train in a few hours while using google colab.

📂 Repository Structure

Text/ # Raw medical datasets

Code/ # Jupyter notebooks containing the entire training lifecyle of the model

docs/ # Data gathering report and supporting docs

README.md # Main repository summary

🙏 Acknowledgements
A special thanks to OMEIFEI DIGITAL GROUP OF COMPANIES for providing this internship opportunity, the guidance, and the resources to enable me improve my knowledge base.

About:
This medical chatbot offers non-critical advice when made aware of patients symptoms
