

## Environment

```bash
conda create -n codeplan python==3.11 -y
conda activate codeplan
pip install tqdm evaluate textdistance
```

## Run

```bash
python scripts/eval.py --repo t1 --approach codeplan --save_path t1_codeplan_stats.json
```
