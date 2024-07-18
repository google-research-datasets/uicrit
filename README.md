# UICrit Dataset

UICrit is a dataset containing human-generated natural language design critiques, corresponding bounding boxes for each critique, and design quality ratings for 1,000 mobile UIs from [RICO](http://www.interactionmining.org/rico.html). This dataset was collected for our UIST '24 paper: [https://arxiv.org/abs/2407.08850](https://arxiv.org/abs/2407.08850).

## Description

All the data can be found in the CSV file: uicrit_public.csv<br/>
Each row contains data provided by one human annotator, and each UI Screen was evaluated by three different annotators.<br/>
The columns in the CSV file are as follows:
- “rico_id”: The corresponding Screen ID from the [RICO dataset](http://www.interactionmining.org/rico.html), which can be used to get the Mobile UI screenshot
- “task”: The main task that the UI screen is designed for
- “aesthetics_rating”: A numerical rating (on a scale of 1-10) of the quality of the UI screen’s aesthetics
- “learnability”: A numerical rating (on a scale of 1-5) of the quality of the UI screen’s learnability (i.e. inuititiveness)
- “efficency”: A numerical rating (on a scale of 1-5) of the quality of the UI screen’s efficiency (i.e. how quickly users can complete tasks)
- “usability_rating”: A numerical rating (on a scale of 1-10) of the quality of the UI screen’s usability (i.e. how easy it is to use)
- “design_quality_rating”: A numerical rating (on a scale of 1-10) of the quality of the UI’s overall design, which depends on its usability and aesthetics ratings
- “comments_source”: A list, where each item specifies the source of its corresponding comment in the “comments” column. The different sources are “human” (from a human annotator), “llm” (from Gemini), and “both” (from both a human rater and Gemini)
- “comments”: A list of design comments for the UI screen. Each comment also includes bounding box coordinates for its relevant region in the UI screenshot. The bounding box coordinates are normalized by the screenshot's dimensions. The source for each comment (human, llm, or both) can be found at its corresponding list index in “comments_source”.

Note that this version of the dataset is around 3 times larger than the one discussed in the paper, where each UI screen was evaluated by a single human annotater. This larger version of the dataset contains 11,344 design critiques. 
