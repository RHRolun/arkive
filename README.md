# Arkive

A backup of the Red Hat OpenShift AI (RHOAI) **3.3** out-of-the-box workbench and pipeline runtime images, packaged as a Helm chart.

Install this on any RHOAI cluster to make the 3.3 images available alongside whatever version is currently running.

## What's included

**11 workbench images** (ImageStreams) — appear in the RHOAI dashboard under *Workbenches* prefixed with `[3.3]`:

| Image | Versions |
|-------|----------|
| Jupyter \| Minimal \| CPU \| Python 3.12 | 2025.2, 2025.1, 2024.2, 2024.1, 2023.2, 2023.1, 1.2 |
| Jupyter \| Data Science \| CPU \| Python 3.12 | 2025.2, 2025.1, 2024.2, 2024.1, 2023.2, 2023.1, 1.2 |
| Jupyter \| TrustyAI \| CPU \| Python 3.12 | 2025.2, 2025.1, 2024.2, 2024.1, 2023.2, 2023.1 |
| Code Server \| Data Science \| CPU \| Python 3.12 | 2025.2, 2025.1, 2024.2, 2024.1, 2023.2 |
| Jupyter \| Minimal \| CUDA \| Python 3.12 | 2025.2, 2025.1, 2024.2, 2024.1, 2023.2, 2023.1, 1.2 |
| Jupyter \| PyTorch \| CUDA \| Python 3.12 | 2025.2, 2025.1, 2024.2, 2024.1, 2023.2, 2023.1, 1.2 |
| Jupyter \| TensorFlow \| CUDA \| Python 3.12 | 2025.2, 2025.1, 2024.2, 2024.1, 2023.2, 2023.1, 1.2 |
| Jupyter \| PyTorch LLM Compressor \| CUDA \| Python 3.12 | 2025.2 |
| Jupyter \| Minimal \| ROCm \| Python 3.12 | 2025.2, 2025.1, 2024.2 |
| Jupyter \| PyTorch \| ROCm \| Python 3.12 | 2025.2, 2025.1, 2024.2 |
| Jupyter \| TensorFlow \| ROCm \| Python 3.12 | 2025.2, 2025.1, 2024.2 |

**7 pipeline runtime images** (ImageStreams) — available in the pipeline editor prefixed with `[3.3]`:

| Image | Versions |
|-------|----------|
| Runtime \| Minimal \| CPU \| Python 3.12 | minimal |
| Runtime \| Datascience \| CPU \| Python 3.12 | datascience |
| Runtime \| Pytorch \| CUDA \| Python 3.12 | pytorch |
| Runtime \| TensorFlow \| CUDA \| Python 3.12 | tensorflow |
| Runtime \| PyTorch LLM Compressor \| CUDA \| Python 3.12 | pytorch-llmcompressor |
| Runtime \| Pytorch \| ROCm \| Python 3.12 | rocm-pytorch |
| Runtime \| TensorFlow \| ROCm \| Python 3.12 | rocm-tensorflow |

> **Note:** Images tagged `2025.1` and later are pulled from `registry.redhat.io` and require a Red Hat pull secret configured on the cluster.

## Install

```bash
helm install arkive ./helm
```

## Upgrade / uninstall

```bash
helm upgrade arkive ./helm
helm uninstall arkive
```
