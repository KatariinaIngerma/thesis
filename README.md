# LLM-Generated Text Classification Using Zero-Shot Prompts

This repository contains the code and data for studying linguistic differences between human-written and LLM-generated texts, evaluating the machine-generated text detection performance of various language models, and analyzing the impact of text length on detection accuracy. The study uses the AuTexTification Dataset and involves experiments with BigScience's BLOOM models and OpenAI's GPT-3.5-Turbo in zero-shot settings.

### Models
* BigScience’s BLOOM-1b7 (Open-source); <br>
* BigScience’s BLOOM-3b (Open-source); <br>
* OpenAI’s GPT-3.5 turbo (Proprietary); <br>

### Data
Data folder has 1000 sample sub-datasets I extracted from this dataset: https://huggingface.co/datasets/symanto/autextification2023 

### Repository Structure
GPT_classification -  code used to classify the data using GPT-3.5-Turbo. <br>
GPT_dataset_selection - code for creating GPT-3.5-Turbo dataset (1000 samples, various text lengths, and 3 domains). <br>
GPT_prompt_selection - testing different prompts with GPT-3.5-Turbo on 20 sample test dataset.  <br>
Classification_BLOOM - code used to classify the data using BLOOM models. <br>

### Implementation Details
The practical tasks were conducted using Google Colab Pro with Jupyter Notebooks, utilizing the Python programming language. Colab Pro was chosen due to its higher RAM capacity and longer runtime, necessary for handling the computational demands of the tasks. The following Python libraries were used:

* Pandas for data manipulation. <br>
* Transformers for BLOOM model implementation. <br>
* LexicalRichness and spaCy for text analysis. <br>
* The GPT model was accessed via the OpenAI API. <br>


### Key Findings
Lexical Complexity: Smaller LLMs (e.g., BLOOM) exhibit higher lexical complexity compared to human texts, while larger models (e.g., GPT-3.5-Turbo) produce text closer to human writing styles. <br>
Detection Capability: LLMs vary in their ability to detect their generated texts. LLMs like GPT-3.5-
Turbo have limited human-like ability to identify their own generated text because the
text they generate resembles closely human-written text. A less capable model, BLOOM1b7 demonstrated some level of ability to recognize their own generated texts. Finally,
BLOOM-3b detected some portion of the texts correctly, still its detection capability was
behind BLOOM-1b7 when detecting their own generated texts. <br>
Text Length Impact: The impact of text length on detection varies; some models show improved accuracy with longer texts, while others perform consistently regardless of length. <br>

