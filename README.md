# Tamil Summarization and English-to-Tamil Translation Model

## Overview
This repository contains a fine-tuned model for both Tamil summarization and English-to-Tamil translation. The model was fine-tuned using the Hugging Face Transformers library. This README provides information on how to use the model and its capabilities.

## Model Details
- **Model Name**: [Tamil-Summarization]
- **Model Type**: [Summarization, Translation]
- **Framework**: Hugging Face Transformers
- **Original Model**: [Mr-Vicky-01/Fine_tune_english_to_tamil](Mr-Vicky-01/Fine_tune_english_to_tamil)
- **Fine-tuning Dataset**: [HariprasathSB/tamil_summarization](https://huggingface.co/datasets/HariprasathSB/tamil_summarization)
- **Languages Supported**: English, Tamil

## Usage
### Installation

You can install the necessary dependencies using pip:

```bash
pip install transformers
```
# Load model directly
from transformers import AutoTokenizer, AutoModelForSeq2SeqLM

tokenizer = AutoTokenizer.from_pretrained("Mr-Vicky-01/Finetuned_tamil_summarization")
model = AutoModelForSeq2SeqLM.from_pretrained("Mr-Vicky-01/Finetuned_tamil_summarization")

# Example English-to-Tamil Translation:

input_text = "Be the change that you wish to see in the world."
input_ids = tokenizer.encode(input_text, return_tensors="pt").input_ids
outputs = model.generate(input_ids,max_length=128)
translated_text = tokenizer.decode(outputs[0], skip_special_tokens=True)
print("Translated Tamil Sentence:", translated_text)

# Example Tamil Summarization:

prefix = "summarize: "
tamil_article = """இது குறித்து அவர் பிபிசி தமிழிடம் கூறுகையில், "இத்தீர்ப்பை மிகச் சிறந்த முற்போக்கான தீர்ப்பாக பார்க்கிறேன்.
அடிப்படை உரிமை என்ன என்பதை மிகவும் தீவிரமாக இத்தீர்ப்பு விளக்கியுள்ளது" என்றார்.
"இந்திய அரசியலமைப்பின் 21-ஆவது விதியை மிகவும் ஆழமாக நீதிமன்றம் விளக்கியுள்ளது என்றும்,
ஏற்கனவே இரு வேறு வழக்குகளில் தனி நபர் அந்தரங்கத்தை அடிப்படை உரிமை பாதுகாக்காது எனக் குறிப்பிட்ட தீர்ப்புகளைத் திருத்தி
அந்த உரிமையை தற்போது உச்ச நீதிமன்றம் பாதுகாத்துள்ளது" என்று என்.ராம் கூறினார்.
"ஆதார் பதிவு விவகாரத்தில் இந்த தீர்ப்பு நிச்சயமாக பிரதிபலிக்கும் என்று கூறும் அவர், ஆதார் முறையைத் திணிக்க முயற்சிக்கும்
மத்திய அரசின் எண்ணம் இனி கடினமாக இருக்கும்" என்றார். "நெருக்கடி காலத்தில் நீதிபதி எச்.ஆர். கன்னா அளித்த தீர்ப்பு ஏற்படுத்திய
மாற்றத்தைப் போல இந்தத் தீர்ப்பும் சமூகத்தில் மாற்றத்தை ஏற்படுத்தலாம் என்று சிலர் கருதுவதாகவும்,மொத்தத்தில் இது ஒரு மு

## Demo 

![image](https://github.com/Mr-Vicky-01/tamil_summarization/assets/143078285/0e32be54-dd7f-433c-9910-68437760f0c0)
![image](https://github.com/Mr-Vicky-01/tamil_summarization/assets/143078285/b4d7a48e-f090-44cb-b4d9-62a14880d0a7)

## model link

[Hugging Face](https://huggingface.co/Mr-Vicky-01/Finetuned_tamil_summarization)
