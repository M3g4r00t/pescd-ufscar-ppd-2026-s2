# Programação Paralela e Distribuída — CUDA e LLMs
## UFSCar · PESCD 2026/S2

Material didático da parte CUDA/LLMs do curso de Programação Paralela e Distribuída (PPD) da UFSCar,
semestre 2026/S2.

## Conteúdo publicado

### Slides

| Arquivo | Descrição |
|---------|-----------|
| `content/aula_00_ppd_ufscar.pptx` | Aula 0 — Motivação: GPU, paralelismo, Transformer e LLM |

### Notebooks (Google Colab · GPU T4)

| Arquivo | Descrição |
|---------|-----------|
| `content/1.AC_CUDA_C-com_exemplos_incluidos_v2.ipynb` | Fundamentos de CUDA C com exemplos |
| `content/2.Unified Memory v2.ipynb` | Unified Memory: modelo e benchmarks |
| `content/3.Streaming and Visual Profiling v2.ipynb` | Streams CUDA e profiling visual |
| `content/0.Accelerating GPT-2 with GPUs_ A Deep Dive v2.ipynb` | Aceleração do GPT-2 com CUDA — análise aprofundada |

### Papers de referência

| Arquivo | Descrição |
|---------|-----------|
| `content/paper- All Attention is You Need - 1706.03762v7.pdf` | Vaswani et al. (2017) — Attention Is All You Need |
| `content/paper - Deepseek V3 - 2412.19437v2.pdf` | DeepSeek-V3 Technical Report (2024) |

## Como usar os notebooks

1. Abra o notebook no **Google Colab**.
2. Selecione `Runtime > Change runtime type > T4 GPU`.
3. Valide o ambiente antes de executar:
   ```
   !nvidia-smi
   !nvcc --version
   ```
4. Execute as células em ordem; benchmarks incluem warm-up e múltiplas medições.
