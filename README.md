# MMLU-Pro-TR

|[**🤗 Dataset**](https://huggingface.co/datasets/bezir/MMLU-pro-TR) | [**🏆Leaderboard(SOON!)**] | [**📖 Original Dataset Paper**](https://arxiv.org/abs/2406.01574) |

This repository contains the evaluation code for the Turkish-translated version of the paper "[MMLU-Pro: A More Robust and Challenging Multi-Task Language Understanding Benchmark](https://arxiv.org/abs/2406.01574.pdf)"

## Introduction
We introduce MMLU-Pro-TR, a benchmark that is the translated version of MMLU-Pro, an enhanced benchmark designed to evaluate language understanding models across broader and more challenging tasks. Building on the Massive Multitask Language Understanding (MMLU) dataset, MMLU-Pro integrates more challenging, reasoning-focused questions and increases the answer choices per question from four to ten, significantly raising the difficulty and reducing the chance of success through random guessing. MMLU-Pro comprises over 12,000 rigorously curated questions from academic exams and textbooks, spanning 14 diverse domains including Biology, Business, Chemistry, Computer Science, Economics, Engineering, Health, History, Law, Math, Philosophy, Physics, Psychology, and Others.  


## Dataset Creation
Please refer to huggingface [**🤗 Dataset**](https://huggingface.co/datasets/TIGER-Lab/MMLU-Pro) and [**🤗 Dataset-TR**](https://huggingface.co/datasets/bezir/MMLU-pro-TR) for more details.

## Evaluation

To run local inference, modify the model name in the following script and execute it:

```bash
cd scripts/examples/
sh eval_tr_llama_3_8b.sh
```

## 🏆 Mini-Leaderboard
| Model                                                     |   MMLU-PRO-TR   | MMLU-TR | 
|-----------------------------------------------------------|:---------------:|:-------:|
| Metin/LLaMA-3-8B-Instruct-TR-DPO                          | 27.00           | 49.71
| ytu-ce-cosmos/Turkish-Llama-8b-Instruct-v0.1              | 23.90           | 51.75
| Orbina/Orbita-v0.1                                        | 22.95           | 49.51
| KOCDIGITAL/Kocdigital-LLM-8b-v0.1                         | 21.83           | 47.35
| meta-llama/Meta-Llama-3-8B-Instruct                       | 20.93           | 49.40
| curiositytech/MARS                                        | 20.80           | 46.73
| Trendyol/Trendyol-LLM-7b-chat-v1.8                        | 18.15           | 41.91
| TURKCELL/Turkcell-LLM-7b-v1                               | 17.15           | 39.03
| ytu-ce-cosmos/turkish-gpt2-large-750m-instruct-v0.1       | 10.88           | N/A

For more details on various models and their accuracy across different subjects, please visit our [**Leaderboard(SOON!)**].

## Benchmarking Answer Extraction
We provide different alternatives to do answer extraction. We found that different answer extraction mechanisms have minor impact on the results.
```
python compute_accuracy.py results/llama-3-8b-quantized/CoT/all/
```

## Citation

**BibTeX:**
```bibtex
@misc{wang2024mmlupro,
      title={MMLU-Pro: A More Robust and Challenging Multi-Task Language Understanding Benchmark}, 
      author={Yubo Wang and Xueguang Ma and Ge Zhang and Yuansheng Ni and Abhranil Chandra and Shiguang Guo and Weiming Ren and Aaran Arulraj and Xuan He and Ziyan Jiang and Tianle Li and Max Ku and Kai Wang and Alex Zhuang and Rongqi Fan and Xiang Yue and Wenhu Chen},
      year={2024},
      eprint={2406.01574},
      archivePrefix={arXiv},
      primaryClass={cs.CL}
}
```
