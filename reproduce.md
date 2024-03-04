

## Environment

```bash
conda create -n codeplan python==3.11 -y
conda activate codeplan
pip install tqdm evaluate textdistance
# Successfully installed aiohttp-3.9.3 aiosignal-1.3.1 attrs-23.2.0 certifi-2024.2.2 charset-normalizer-3.3.2 datasets-2.18.0 dill-0.3.8 evaluate-0.4.1 filelock-3.13.1 frozenlist-1.4.1 fsspec-2024.2.0 huggingface-hub-0.21.3 idna-3.6 multidict-6.0.5 multiprocess-0.70.16 numpy-1.26.4 packaging-23.2 pandas-2.2.1 pyarrow-15.0.0 pyarrow-hotfix-0.6 python-dateutil-2.9.0.post0 pytz-2024.1 pyyaml-6.0.1 requests-2.31.0 responses-0.18.0 six-1.16.0 textdistance-4.6.1 tqdm-4.66.2 typing-extensions-4.10.0 tzdata-2024.1 urllib3-2.2.1 xxhash-3.4.1 yarl-1.9.4
pip install joblib
# Successfully installed joblib-1.3.2
```

## Run

### t1 

```bash
HF_ENDPOINT=https://hf-mirror.com python scripts/eval.py --repo t1 --approach codeplan --save_path t1_codeplan_stats.json
```

```bash
WARNING:evaluate.loading:Using the latest cached version of the module from /home/taow/.cache/huggingface/modules/evaluate_modules/metrics/evaluate-metric--bleu/9e0985c1200e367cce45605ce0ecb5ede079894e0f24f54613fca08eeb8aff76 (last modified on Mon Mar  4 13:26:56 2024) since it couldn't be found locally at evaluate-metric--bleu, or remotely on the Hugging Face Hub.
WARNING:root:File-wise diff bleu metric not computed for /mnt/workspace/taow/CodePlan/data/t1.
WARNING:root:File-wise levenshtein metric not computed for /mnt/workspace/taow/CodePlan/data/t1.
Metrics for approach codeplan on repo t1:
{'avg_diff_bleu': None, 'total_ld': None, 'matched_blocks': 8, 'missed_blocks': 2, 'spurious_blocks': 0}
```

### t2

```bash
python scripts/eval.py --repo t2 --approach codeplan --save_path t2_codeplan_stats.json
```

```bash
WARNING:evaluate.loading:Using the latest cached version of the module from /home/taow/.cache/huggingface/modules/evaluate_modules/metrics/evaluate-metric--bleu/9e0985c1200e367cce45605ce0ecb5ede079894e0f24f54613fca08eeb8aff76 (last modified on Mon Mar  4 13:26:56 2024) since it couldn't be found locally at evaluate-metric--bleu, or remotely on the Hugging Face Hub.
WARNING:root:File-wise diff bleu metric not computed for /mnt/workspace/taow/CodePlan/data/t2.
WARNING:root:File-wise levenshtein metric not computed for /mnt/workspace/taow/CodePlan/data/t2.
Metrics for approach codeplan on repo t2:
{'avg_diff_bleu': None, 'total_ld': None, 'matched_blocks': 4, 'missed_blocks': 0, 'spurious_blocks': 0}
```

### t3

```bash
python scripts/eval.py --repo t3 --approach codeplan --save_path t3_codeplan_stats.json
```

```bash
WARNING:evaluate.loading:Using the latest cached version of the module from /home/taow/.cache/huggingface/modules/evaluate_modules/metrics/evaluate-metric--bleu/9e0985c1200e367cce45605ce0ecb5ede079894e0f24f54613fca08eeb8aff76 (last modified on Mon Mar  4 13:26:56 2024) since it couldn't be found locally at evaluate-metric--bleu, or remotely on the Hugging Face Hub.
WARNING:root:File-wise diff bleu metric not computed for /mnt/workspace/taow/CodePlan/data/t3.
WARNING:root:File-wise levenshtein metric not computed for /mnt/workspace/taow/CodePlan/data/t3.
Metrics for approach codeplan on repo t3:
{'avg_diff_bleu': None, 'total_ld': None, 'matched_blocks': 11, 'missed_blocks': 0, 'spurious_blocks': 0}
```

### ext1

```bash
python scripts/eval.py --repo ext1 --approach codeplan --save_path ext1_codeplan_stats.json
```

```bash
WARNING:evaluate.loading:Using the latest cached version of the module from /home/taow/.cache/huggingface/modules/evaluate_modules/metrics/evaluate-metric--bleu/9e0985c1200e367cce45605ce0ecb5ede079894e0f24f54613fca08eeb8aff76 (last modified on Mon Mar  4 13:26:56 2024) since it couldn't be found locally at evaluate-metric--bleu, or remotely on the Hugging Face Hub.
WARNING:root:File-wise levenshtein metric not computed for /mnt/workspace/taow/CodePlan/data/ext1.
Metrics for approach codeplan on repo ext1:
{'avg_diff_bleu': 0.8639000314767546, 'total_ld': None, 'matched_blocks': 64, 'missed_blocks': 0, 'spurious_blocks': 0}
```


### ext2

```bash
python scripts/eval.py --repo ext2 --approach codeplan --save_path ext2_codeplan_stats.json
```

```bash

```
