# OCC Logs Classification - Zero Shot Labeling
This folder contains 
- ipynb that performs the classification
- labled data.csv with around 75 entries  (removed)
- occ logs.csv (removed)
- pretrained BERT model (I think it is unsupervised training with occ log text)
## Approach Summary
- We utilized ChatGPT to generate precise descriptions for the designated categories 
- We used the BERT language model to calculate embeddings for both category descriptions and log entries by comparing the cosine similarity between each category and each log, we tagged each log with the top three labels with the highest similarity
- To improve the accuracy of tagging, we tried 
    - fine-tuning the transformer used for text embedding with labeled data
    - maximizing the distance between the embedded descriptions. 
- Our current approach focused on the most important categories related to fire, life and safety
## Current Categories
- FLS (Fire, Life and Safety)
    - Trapped in Elevator
    - Vandalism
    - Fire
    - Evacuation
    - Henc (Homeless Encampment)
    - Smoke
    - CSE (Computer System Engineering)
- Delay Management
    - Operation
    - Police
    - Track
    - Train Control
    - Traction Power
    - Vehicle

