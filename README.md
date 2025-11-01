# Customer IT Support using HuggingFace Models and PyTorch : Overview 

![Intro](images/image_2.webp)

The objective of this project is to enhance the customer request management process by leveraging Natural Language Processing (NLP) and Large Language Models (LLMs) tools. The system is designed to translate, summarize, and classify incoming requests to ensure they are routed to the appropriate department. This will significantly improve the efficiency of the client-facing teams and enhance the company's operational performance.

Tools and Technologies  : 

>- Python (Pandas, Scikit-learn, PyTorch)
>- LLMs  (NLLB, T-5, BERT) via Hugging Face
>- Git for version control; 

The dataset used comes from kaggle. You can acces by clicking on the following link : https://www.kaggle.com/datasets/tobiasbueck/multilingual-customer-support-tickets

## Variables description

**🔀 Queue** :	Specifies the department to which the email ticket is routed

**🚦 Priority** :	Indicates the urgency and importance of the issue	🟢Low 🟠Medium 🔴Critical

**🗣️ Language**:	Indicates the language in which the email is written	EN, DE, ES, FR, PT

**Subject** :	Subject of the customer's email

**Body**:	Body of the customer's email

**Answer**:	The response provided by the helpdesk agent	

**Type**:	The type of ticket as picked by the agent

**Tags**:	Tags/categories assigned to the ticket, split into ten columns in the dataset



# Project steps and results:

**Data preprocessing**
Selection of relevant columns and combination of some of them (e.g Type + Priotity --> Type_priority, Subject + Body --> Topic)
Basic cleaning and translation into one unique language : english 
with NLLB seq2seq model

**Text Summary with T-5 Model** : Perform a summary for each topic in order to print it in the final streamlit application

***Text classification with BERT and PyTorch**

For this task we are going to fine-tune the BERT model with our data in order
to predict 2 elements :
-< The type and priority of the request from the customer
-< The departement concerned by the message 

***Streamlit deployment**

# Licence and Contact Information : 
You are free to use clone and use this project as your wish.

**Clone project :** 
git clone https://github.com/MayeneBS99/Customer_IT_Support

**Install requirements :** 
pip install -r requirements.txt

If you have any questions or suggestions, feel free to reach me out on my LinkedIn https://www.linkedin.com/in/sch%C3%A9kina-mayene-2a5931244/ or Email: Mayene2212@gmail.com