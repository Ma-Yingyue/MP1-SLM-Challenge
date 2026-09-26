# MP1-SLM-Challenge
MP1 assignment for DASE7506
## Installation

```bash
cd code
python -m venv .venv
.venv\Scripts\activate
python -m pip install torch==2.7.1 --index-url https://download.pytorch.org/whl/cpu
python -m pip install -r requirements.txt
python -m unittest discover -s tests -v
Training
bash
python train.py --implementation student --config configs/my_config.json --seed 17 --steps 2400 --eval-every 600 --run-dir runs/my-model-w256-s2400
Evaluation
bash
python evaluate.py --checkpoint runs/my-model-w256-s2400/checkpoint.pt --device cpu --precision fp32 --split test
Results
Validation BPB: 1.689
Test BPB: 1.7117
Evaluation time: ~23 s (compliant with 5× baseline limit)
Model size: ~16 MB (compliant with 64 MiB limit)
AI Assistance Disclosure
I acknowledge the use of AI assistance (ChatGPT/DeepSeek) for environment setup guidance, experiment design suggestions, and report drafting. All experiments, code modifications, data analysis, and conclusions were independently performed and verified by me.
