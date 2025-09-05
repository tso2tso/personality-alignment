
# Personality Alignment of Large Language Models [ICLR 2025]

Welcome to the official repository for Personality Alignment with PASO (Personality Activate Search Optimize). This repository is dedicated to advancing the field of personalized AI by aligning large language models (LLMs) with individual user preferences and personality traits. Here, you'll find the code and data supporting our groundbreaking research.

## Overview

In the evolving landscape of AI, personality alignment stands as a pivotal advancement. Traditional models align with broad human values, but PASO goes further by fine-tuning models to reflect the nuanced preferences and traits of individual users. This repository provides the tools and data to implement and evaluate such alignment, making AI interactions more relevant, meaningful, and personalized.

## Features

- **Personality Alignment**: Implement PASO to dynamically adjust model activations, achieving nuanced alignment with user-specific traits.
- **Comprehensive PAPI Dataset**: Utilize a rich dataset of personality profiles to train and evaluate models.
- **Benchmarking**: Compare the performance of PASO against state-of-the-art methods like DPO, PPO, and various prompt-based techniques.
- **Open-Ended Generation**: Assess model performance on complex reasoning and personalized response tasks.

## Installation


Install the required packages:

```bash
pip install .
```

## Data: PAPI Dataset

The Personality Alignment with Personality Inventories (PAPI) dataset is central to our approach. It consists of detailed personality profiles collected from over 300,000 individuals using the IPIP-NEO personality inventory. This dataset forms the backbone of our alignment process, enabling models to learn and adapt to individual user traits.

### Download Test-Set Dataset
If you only need to reproduce our work, including the IPIP-NEO part and the Dark-Triad part from the paper, we have stored the Test-Set data in this Github repository, which you can access directly by git clone.

##### IPIP-NEO
- **IPIP-NEO-ItemKey.xls**: Contains the item keys for the IPIP-NEO personality inventory.
- **mpi_120.csv**: Responses to the IPIP-NEO-120 questionnaire.
- **mpi_300.csv**: Responses to the IPIP-NEO-300 questionnaire.
- **mpi_300_split.json**: The Test-Set split for PAPI dataset (IPIP-NEO).
- **Test-set.json**: The Test-Set data for PAPI dataset (IPIP-NEO).

##### Dark-Triad
- **dark_triad-ItemKey.xls**: Contains the item keys for the dark_triad personality inventory.
- **dark_triad_Test_set.json**: The Test-Set data for PAPI dataset (Dark-Triad).
- **dark_triad_split.json**: The Test-Set split for PAPI dataset (Dark-Triad).

  
### Download All Dataset
If you are interested in the Dev-Set, you are welcome to download the full version of the PAPI dataset through Huggingface or Google Drive.

We have released the PAPI dataset in Google Drive! 

**PAPI-300K**: the 300K datasets for PAPI, it include IPIP-NEO-120 and IPIP-NEO-300 Questionnaire, with 300K Subject's answer.
- [Google Drive](https://drive.google.com/file/d/1KRhpTCwSMS47GYnmHwYRPnmxF6FOGYTf/view?usp=sharing)

**Dark-Triad**: the 18K datasets for Dark-Triad, it include 27 Questionnaire about Dark-Triad, with 18K Subject's answer.
- [Google Drive](https://drive.google.com/file/d/1TTjbHDg5BvPRHJStBx_xf7f0aHXbaOIM/view?usp=drive_link)


**PAPA-120-600K**: the 600K datasets for PAPI, but it ONLY include IPIP-NEO-120 Questionnaire. 
- [Google Drive](https://drive.google.com/file/d/1V0JkJL3KMn6ZpOqOFVkfbLZD1HqQJgS5/view?usp=drive_link)



### Data Permissions

This project uses IPIP items, scales, and inventories, which are in the public domain. Permission has been automatically granted for any use, commercial or non-commercial. Refer to [IPIP Permission](./IPIP_Permission.pdf) for more details.



## Method: PAS (Personalized Activate Search)

PAS is an innovative method designed to fine-tune LLMs to align with individual user preferences. It dynamically adjusts model activations based on user-specific traits, ensuring that the model's responses are personalized and relevant.

### Key Steps in PASO

1. **Personality Alignment**: Use the PAPI dataset to train the model on individual user profiles.
2. **Activation Intervention**: During inference, adjust the model's activations in real-time to reflect user-specific traits.
3. **Evaluation**: Assess the model's performance using both multiple-choice and open-ended tasks to ensure robust alignment.

### Training and Evaluation

To train and evaluate the models using the PAS method, execute:

```bash
python main.py
```

This script aligns the language model with the specified user profiles and evaluates its performance on multiple-choice tasks.


## Contributions

We welcome contributions to enhance the personalized alignment capabilities of LLMs. Please feel free to fork this repository, make your changes, and submit a pull request.

## References

For a detailed understanding of our methods and results, refer to our latest paper on personalized alignment using the PAS method. Additionally, you can find implementations of DPO, PPO, and other baseline methods within this repository.

```
@inproceedings{
zhu2025personality,
title={Personality Alignment of Large Language Models},
author={Minjun Zhu and Yixuan Weng and Linyi Yang and Yue Zhang},
booktitle={The Thirteenth International Conference on Learning Representations},
year={2025},
url={https://openreview.net/forum?id=0DZEs8NpUH}
}
```

Explore the future of personalized AI with PAS, and let's build models that truly understand us! 🚀

---

## 🎉 What's Next?

This is one of our "causal intervention" projects. If you're hungry for more AI safety goodness, check out these related projects:

- [SafetyLock](https://github.com/zhu-minjun/SafetyLock) (Stay safe, stay aligned, and may your LLMs always respond appropriately! 🦜✨)

Happy Aligning!



