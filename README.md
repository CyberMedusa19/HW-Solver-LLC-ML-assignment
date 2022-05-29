# HW-Solver-LLC-ML-assignment
ML assignment. Read file 'Machine Learning Assignment' prior to rest of readme. This file is intended to explain my approach to solving the problem described in the file. 

## Approach

__Goals:__ <br>
Given a list of example technical skills, extract the technical skills of a given dataset

__Step 1: Extracting the data__<br>
Read in skills from "Example_Technical_Skills.csv" and 'Raw_Skills_Dataset.csv' and store them in their own dataframe. <br>
This is done with the "dataframe_create" function. <br>

Extract the information from "Technology Skills" and "RAW DATA" columns from "Example_Technical_Skills.csv" and 'Raw_Skills_Dataset.csv' respectively and store the extracted info into their own lists. <br>

__Step 2: Comparing the data__<br>
Compare the 2 lists and extract only the skills found in "Example_Technical_Skills.csv" from 'Raw_Skills_Dataset.csv' <br>

__Step 3: Separating soft skills from technical skills__
Upon examing the data in 'Raw_Skills_Dataset.csv' I notice that the entries can be classified as __technical skills__, __soft skills__, or __random words__.<br>

I attempt to sepate soft skills from technical skills by extracting the soft skills from the 'raw_data' list I created earlier.<br>

To do this I create a regex expression that covers commonly desired soft skills such as: 
- Good Attitude
- Communication Skills 
- Work ethic
- Teamwork
- Leadership qualities
- Time management
- Decision making
- Conflict resolution
- Critical thinking
- Networking
- Empathy
- Problem-solving 

Of course this list is not exhaustive and can be prone to return values that are not considered soft skills. However it will filter out most of the entries considered __"random words"__ and give you a decent idea of what soft skills are present in your dataset.<br>

With this I now have a function that can extract the techincal skills and soft skills. I can then apply the "uniq_skills" function created earlier to filter out repeated skills. 



