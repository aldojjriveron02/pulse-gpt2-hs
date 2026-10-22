# pulse-gpt2-hs

Custom ONNX export of GPT-2 (124M, fp32, forward-only) for the PULSE live probe page.

- **Inputs:** `input_ids`, `attention_mask`
- **Outputs:** `logits` + `hidden_states.0` … `hidden_states.11` (per-layer, 768-dim)
- Exported with torch.onnx (opset 17/18), weights in `model.onnx.data`.
- Probe parameters (`probe_params.json`) live with the PULSE research files.

Part of Aldo Riveron's PULSE project — a checkup machine for AI.
