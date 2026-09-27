# Curso de Programação Paralela e Distribuída — CUDA
## UFSCar · Material didático

Projeto para atualizar criticamente o trabalho de David Münch (2009),
*Parallel programming with CUDA: Architecture, Analysis, Application*,
produzindo material atualizado para a parte CUDA do curso de PPD.

## Objetivos

- Ensinar o modelo de programação CUDA desde os fundamentos até a otimização.
- Contrastar CUDA 2.x e arquiteturas históricas com o CUDA moderno.
- Manter o fio pedagógico do material original: arquitetura → modelo → algoritmos → desempenho → limitações.
- Incorporar práticas reproduzíveis, medição rigorosa e laboratórios em GPU.

## Estado

- Fonte original incorporada em `source/`.
- Cada módulo distingue: conteúdo histórico, conceito vigente, material obsoleto e atualização didática.

## Sequência de aulas

| # | Tema | Arquivo |
|---|------|---------|
| 0 | Motivação: GPU, paralelismo, Transformer e LLM | `classes/00_motivacion_gpu_transformer_llm.md` |
| 1 | Processamento e memória CUDA | `classes/01_processamento_memoria_cuda_t4.md` |
| 2 | Multi-GPU e escalabilidade | `classes/02_multigpu_colab_t4.md` |
| 3 | Profiling CUDA | `profiling/GUIA_PROFILING_CUDA_COLAB_T4.md` |
| 4 | Matrizes, convolução e aplicações | — |
| 5 | Projeto integrador | — |

## Estrutura do repositório

```
classes/
  00_motivacion_gpu_transformer_llm.md   # Aula 0 — motivação e contexto histórico
  01_processamento_memoria_cuda_t4.md    # Aula 1 — processamento e memória CUDA (PT)
  02_multigpu_colab_t4.md                # Aula 2 — multi-GPU e escalabilidade (PT)
  aula-00/                               # Plano, roteiro e referências da Aula 0
    CLASS_PLAN.md
    SLIDES_OUTLINE.md
    REFERENCES.md
  drafts/                                # Rascunhos históricos (espanhol — não usar em aula)
    01_procesamiento_memoria_cuda_t4.md

notebooks/
  00_primera_aula_llmc_t4.py             # Aula 0: GPU, CUDA, Transformer, llm.c — Colab T4
  11_procesamiento_memoria_t4.py         # Aula 1: timing, memória, benchmark
  12_multigpu_semantics_t4.py            # Aula 2: semântica multi-GPU (simulado em 1 GPU)
  13_profiling_t4.py                     # Aula 3: profiling com PyTorch e CUDA events

presentation/
  create_aula_00_carbon.py               # Gerador do PPTX da Aula 0 (python-pptx)
  aula_00_do_pixel_ao_token_carbon_light.pptx
  primera_aula_cuda_transformer.pptx

profiling/
  GUIA_PROFILING_CUDA_COLAB_T4.md       # Guia transversal de profiling

source/
  parallel-programming-with-cuda-2009.pdf  # Fonte original de 2009
  parallel-programming-with-cuda-2009.txt  # Extração textual
```

## Notas de execução

- Os notebooks rodam no **Google Colab** com `Runtime > Change runtime type > T4 GPU`.
- Antes de executar: valide `nvidia-smi`, `nvcc --version` e memória disponível.
- `notebooks/00_primera_aula_llmc_t4.py` clona o repositório externo `llm.c` — fixe o commit antes da aula.
- `notebooks/12_multigpu_semantics_t4.py` simula particionamento em **uma única GPU**; o output é rotulado `SIMULATED`.
- Benchmarks devem incluir warm-up, sincronização explícita e múltiplas medições.
