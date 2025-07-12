# Triton-ML-Runner

**Triton-ML-Runner** is a lightweight, multi-level execution engine for [Triton](https://github.com/triton-lang/triton), designed to support IR/PTX/cubin launches in complex pass pipelines.

This project is built specifically for **Triton v3.3.1** and is not guaranteed to work with other versions.

## Example

> **Note:** The following example requires an NVIDIA GPU with compute capability `sm90`, `sm86`, or `sm75`. Please make sure to install the package before running the example.

### sm90 (H20)
```bash
python examples/ttir_runner/matmul.py

python examples/ttgir_runner/sm90/matmul.py

python examples/llir_runner/sm90/matmul.py

python examples/ptx_runner/sm90/matmul.py

python examples/cubin_runner/sm90/matmul.py
```

### sm86 (A10)
```bash
python examples/ttir_runner/matmul.py

python examples/ttgir_runner/sm86/matmul.py

python examples/llir_runner/sm86/matmul.py

python examples/ptx_runner/sm86/matmul.py

python examples/cubin_runner/sm86/matmul.py
```

### sm75 (Tesla T4)
```bash
python examples/ttir_runner/matmul.py

python examples/ttgir_runner/sm75/matmul.py

python examples/llir_runner/sm75/matmul.py

python examples/ptx_runner/sm75/matmul.py

python examples/cubin_runner/sm75/matmul.py
```

## Installation

install the package as a standard Python package

```bash
git clone https://github.com/OpenMLIR/triton-ml-runner
cd triton-ml-runner
pip install .
```

### Development Installation (Editable Mode)

If you are actively developing or modifying the source code, install the package in editable mode. This allows changes in the source files to take effect immediately without reinstalling:

```bash
pip install -e .
```

## ⚠️ Version Compatibility

This runner is built against **Triton v3.3.1**.
Compatibility with other versions of Triton is **not guaranteed** and may lead to unexpected behavior or build failures.

## 📄 License

This project is licensed under the **MIT License**.
See the [LICENSE](./LICENSE) file for more details.
