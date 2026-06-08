---
license: mit
dataset_info:
  features:
  - name: id
    dtype: string
  - name: general_domain
    dtype: string
  - name: subdomain
    dtype: string
  - name: field
    dtype: string
  - name: query
    dtype: string
  - name: date
    dtype: timestamp[ns]
  - name: rubric
    list:
    - name: citation_metadata
      struct:
      - name: first_author
        dtype: string
      - name: title
        dtype: string
      - name: url
        dtype: string
      - name: year
        dtype: int64
    - name: rubric_item
      dtype: string
    - name: type
      sequence: string
  splits:
  - name: valid
    num_bytes: 1211536
    num_examples: 703
  - name: test
    num_bytes: 6515983
    num_examples: 3750
  - name: full
    num_bytes: 37155771
    num_examples: 21414
  - name: test_mini
    num_bytes: 1338444
    num_examples: 776
  download_size: 16275449
  dataset_size: 46221734
configs:
- config_name: default
  data_files:
  - split: valid
    path: data/valid-*
  - split: test
    path: data/test-*
  - split: full
    path: data/full-*
  - split: test_mini
    path: data/test_mini-*
---
<h1 align="center">
  ResearchQA
</h1>
<p align="center">
  🌐 <a href="https://researchqa.cylumn.com/">Website</a> | 
  📄 <a href="https://arxiv.org/abs/2509.00496">Paper</a> | 
  💻 <a href="https://github.com/realliyifei/ResearchQA">Github</a>
</p>

ResearchQA is designed to evaluate scholarly question answering across 75 fields, using questions and rubrics mined from survey papers. The dataset consists of 3,750 questions in the test set (776 questions in the test-mini set), 703 in the validation set, and  a total of 21,414 questions. Both the questions and rubrics have been validated by 31 Ph.D.-level annotators across 8 fields.