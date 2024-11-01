# Sphinteract

## Overview
This repository contains the code, data, and resources for our research on NL2SQL with Sphinteract framework.

## Repository Structure
- **zeroshot_experiments.ipynb** - Source code for running zero shot experiments on KaggleDBQA and BIRD.
- **FewShotAmbSQL.ipynb** - Source code for running fewshot experiments on KaggleDBQA and BIRD.

## Experiment Logs and User Studies
We have made our experiment logs and user study data available for public access. You can find them on our Google Drive:

[Experiment Logs & User Studies](https://drive.google.com/drive/folders/1Mn-h6OdZAAGHxxMJ94ruDptRWK0zxNO8?usp=sharing)
- **batchRequests.zip** - This folder contains the 0th round requests and answer using the DAIL prompts. To reduce the experimental costs, we decided to use OpenAI Batch API to generate the initial SQL queries.

- **experiment_logs.zip** - This folder contains the experimental logs of Sphinteract using 0, 1, 3, and 5 demonstrations with gpt-3.5-turbo and gpt-4-turbo. Each pkl file contains a list of dictionaries. The keys for each dictionary is `sql_log`, `cq_log`, `feedback_log`, and `num_cq_asked`.

- - **sql_log** - Contains a list of (order, sql_generation_prompt, predicted_sql, pscore). The order field is an int which helps tracking the ordering between sqls, cqs, and feedback. The sql_generation_prompt follows the same format as DAIL-SQL (code repsentation with rule).
- - **cq_log** - Contains a list of (order, SRA_prompt, clarification question, pscore).
- - **feedback_log** - Contains a list of (order, feedback_prompt, feedback, pscore).
 
- **kaggle_userstudy.jsonl** - This file contains the 64 KaggleDBQA questions and the response from users. Through this userstudy, we find that for the same questions, users may have totally different expectations on the SQL ansewr.

- **sphinteract_user_study.zip** - This folder contains our Sphinteract user study web pages. Open the `frontpage.html` to start the user study. Before starting the user study, please fill in the `apiKey` field in `study.html`.





