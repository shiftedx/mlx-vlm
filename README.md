# MLX-VLM — shiftedx fork

Development fork of [Blaizzy/mlx-vlm](https://github.com/Blaizzy/mlx-vlm) for
local vision, language, audio, and video model inference with MLX.

[Full reference](docs/REFERENCE.md) · [Usage](docs/usage.md) · [Agent skills](skills/) · [License](LICENSE)

## Use upstream

```bash
pip install -U mlx-vlm
mlx_vlm.generate --model mlx-community/Qwen2-VL-2B-Instruct-4bit \
  --max-tokens 100 --prompt 'Hello'
```

PyPI installs upstream releases. Model weights download separately; check the
model's license and memory requirements. The optional chat UI needs
`pip install -U 'mlx-vlm[ui]'`.

## Work on this fork

```bash
git clone https://github.com/shiftedx/mlx-vlm.git
cd mlx-vlm
python3 -m venv .venv
. .venv/bin/activate
python -m pip install -e .
```

Inspect the [upstream comparison](https://github.com/Blaizzy/mlx-vlm/compare/main...shiftedx:mlx-vlm:main)
for current fork changes. For inference on a Mac, use Apple Silicon and a Python
version supported by [pyproject.toml](pyproject.toml).

| Task | Reference |
| --- | --- |
| CLI, model support, speculative decoding | [Full reference](docs/REFERENCE.md) |
| Python API and batch generation | [Usage](docs/usage.md) |
| Server configuration | [Server section](docs/REFERENCE.md#server-fastapi) |
| Conversion, fine-tuning, distributed inference | [Full reference](docs/REFERENCE.md) |
| Agent workflow instructions | [Skills bundle](skills/) |
| Structured extraction | `python examples/structured_outputs.py --image /path/to/local-image.png` (requires Outlines 1.1.1) |

Keep credentials and local model paths out of commits. Upstream benchmarks and
release badges describe upstream builds; qualify fork changes on your own hardware.
