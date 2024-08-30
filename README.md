# Term Deposit Marketing model
This is a repository for a machine learning model that leverages information coming from call center data to predict if a customer will subscribe or not for a product. Its goal is improve the success rate for calls made to customers for any offered product, and help clients to make informed decisions.
## Description
The main objective of this project is to develop a robust machine learning system that leverages information coming from call center data. The goal of the model is to improve the success rate for calls made to customers for any product that the clients offer.
The model aims then to offer high success outcomes and interpretability for clients to make an informed decision.
Therefore, the used data comes from a campaign that involves making a phone call to a customer, often multiple times to ensure a term deposit subscription. Term deposits are usually short-term deposits with maturities ranging from one month to a few years. The customer must understand when buying a term deposit that they can withdraw their funds, only after the term ends.
## Solution
The notebook demonstrates how I applied Machine Learning and Exploratory Data Analysis (EDA) techniques to help the company effectively classify its customers and make informed decisions. In the first step, I utilized EDA techniques to assess the diversity of the data and identify the most important features. Next, I employed a two-layer machine learning approach to identify potential customers. In the first layer, I excluded contact-related data such as "day," "month," "duration," and "campaign," because these variables are unknown before contacting the customer. Instead, I focused on other relevant data such as job, education, balance, etc. In the second layer, I used all features to train a model to determine which customers should be followed up on. Finally, I identified customers who are more likely to purchase the investment product by clustering them based on the features selected through recursive feature elimination.
## Conclusion
After running the model, we achieved 79% accuracy and 0.83 recall, indicating that the model correctly identifies 83% of the negative cases (i.e., those who would not register). This demonstrates that the model can effectively predict which individuals are unlikely to register based on non-contact-related parameters, enabling you to focus efforts on calling potential customers who are more likely to register. The total call duration in the database was 2,831 hours, which was reduced to 374 hours, resulting in a time savings of 2,457 hours. Additionally, the number of calls was reduced from 115,287 to 8,332, leading to significant savings in marketing costs by targeting only potential customers with a high likelihood of subscription. The final model achieved 95% accuracy, with the best training algorithms selected using the PyCaret library. The optimal parameters were chosen by Optuna, and the model was ultimately ensembled using voting and stacking classifiers, with the voting classifier performing the best.
At the end, the clustering was optimized using the elbow method, and the data were grouped into four clusters to identify potential subscribers.
#### For more details, see the notebook: **Term_Deposit_Marketing-virtualenv.ipynb**      
> The following image represents the last missed plot in the notebook:
[Screenshot](https://github.com/shahnavaz1992/Term-Deposit-Marketing-Machine-Learning-model/blob/main/clustring_plot.png)
### Below is also a dashboard of the data represented by Tableau
[Dashboard](https://public.tableau.com/app/profile/farid4750/viz/Book1_17249023540900/Dashboard1?publish=yes)
## Requirements
Because this project uses some libraries that need special versions of python as for other modules, it would be better to create a virtual environment. Assuming that you have Anaconda installed. 
To do this:
* Open Anaconda Prompt from the desktop.
* Create a Virtual environment with the following command:    
### **conda create -n yourenvname python=3.6** 
* Activate your env: 
### **conda activate yourenvname**
* Luch Jupyter notebook with the command:
### **jupyter notebook**
* Open a new jupyter notebook.
* Install required packages with the following command:      
### **pip install -r requirements.txt**
