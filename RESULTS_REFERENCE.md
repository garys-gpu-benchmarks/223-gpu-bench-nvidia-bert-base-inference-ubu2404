# Results: 223 BERT Inference Sweep

**Main goal:** Measure PyTorch BERT inference performance  
**Tools:** Run gpu-bench-bert-transformers-inference.py via collect_bert_infer.py

Reference results measured by the maintainer on the system shown in each section (generator TEMPLATE_00_139 · recorded 2026-11-13). Your own runs write `results/RESULTS_ACTUAL.md` in the same format.

> Smoke runs use deliberately small sizes. They check that the workload installs and runs end to end; their numbers are not performance results. Baseline and extended are.

<!-- profile:smoke -->
## smoke

- **System:** 1× NVIDIA H100 PCIe (81559 MiB) · Intel(R) Xeon(R) Platinum 8352Y CPU @ 2.20GHz · Ubuntu 24.04.5 LTS · kernel 6.8.0-138-generic · driver 595.91.07
- **Run:** 2026-11-13T14:35:58Z · status **PASS** (exit 0)
- **Time (mm:ss):** setup 02:33 · benchmark 00:16 · whole run 03:04
- **Source:** run 223_20261113_143558
- **Command:** `bash run_benchmark.sh --smoke --model-name bert-base-uncased --dtype f16_r --sequence-len 32 --batch-size 1 --warmup-iters 2 --num-iterations 5 --prompt-source synthetic`

| # | Metric | Result |
|---|---|---|
| 1 | Inference throughput (sequences_per_sec) | 163.82583666666667 |
| 2 | Inference latency, mean step time, ms (mean_latency_ms) | 6.117846666666667 |
| 3 | Token throughput (tokens_per_sec) | 5242.426771333333 |
| 4 | Peak GPU memory (peak_gpu_memory_gb) | 0.260582 |
<!-- /profile:smoke -->
