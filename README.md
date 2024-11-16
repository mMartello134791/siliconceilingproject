# Silicon Ceiling Research

### Background

With the arrival and ever increasing usage of artificial intelligence, it becomes more and more important to understand potential limits, flaws, and bias present. Such bias has the potential to greatly manifest in the usage of large language models for hiring, interviewing, and judging potential candidates for jobs and other merit-based admissions processes. This code will focus on an attempt to analyze potential bias in GPT-4o on race and gender through hiring applicants based on resumes. This research is based off of [this paper.](https://arxiv.org/abs/2405.04412)

### Methodology

[Datasource]((https://www.kaggle.com/datasets/snehaanbhawal/resume-dataset)

Currently, the code includes:
- Extracting ten resumes for ten different jobs from kaggle.
- Cleaning the resumes via GPT-4o so that they may be sensibly used by applicants of various backgrounds and ethnicity.
- Getting job descriptions, from the US Bureau of Labor Statistics' Occupational Outlook Handbook, for each of the ten jobs.
- Getting 32 different names signifying different races and genders.
- Getting three seperate prompts for GPT - Rating, Interview, and Hiring. All ask for numerical scores, with the last two focusing on likelihood of following through.
- Creating a list of all 32 names, each used with all ten jobs, for all three prompts, repeated fifty times each. The final list has a length of 48,000.
- Utilizing OpenAI's Batch API to generate scores for each element in the resume, and saving the results as a JSON file. (IN PROGRESS)
