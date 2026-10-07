# Technical Architecture — TIMEFLUX

**Upstream:** [https://github.com/nicedoc/timeflux](https://github.com/nicedoc/timeflux)
**License:** MIT
**Category:** BRAIN_COMPUTER_INTERFACE
**Anticloud Integration:** PAX L5 Narrow L2 General 27B + AIOSS + Offline-First

## Upstream Description

Real-time BCI signal processing

## Anticloud Architectural Changes

1. PAX L5 Narrow L2 General 27B local neural signal decoding — air-gapped clinical device
2. AIOSS tamper-evident neural recording chain (FDA De Novo/510k audit-ready)
3. AES-256 encryption for all neural signal data (most sensitive PII category)
4. Single-binary BCI runtime deployable on embedded clinical hardware
5. Zero-cloud: all decoding, classification, and feedback run on-device
6. GPU/CPU equalizer: real-time decoding on embedded GPU, logging on CPU
7. Open BrainFlow/LSL integration replacing proprietary BCI SDK interfaces
8. Offline stimulation parameter optimizer replacing cloud neuromodulation APIs

## Integration Points

- **PAX Inference Socket:** Local HTTP endpoint at `127.0.0.1:11434/v1/chat` — same OpenAI-compatible API, zero cloud
- **AIOSS Hook:** Every write operation calls `aioss_append(event, payload)` before commit
- **Encryption Layer:** All file I/O routed through `anticloud_crypto.encrypt_at_rest()`
- **Single Binary Build:** `pyinstaller anticloud_timeflux.spec` or `go build -o timeflux`

## Deployment Modes

| Mode | Hardware | Notes |
| --- | --- | --- |
| Edge CPU | Raspberry Pi 4 / Intel NUC | Full feature set, PAX on CPU |
| Desktop GPU | RTX 3060 / A10 | PAX GPU inference, <1s latency |
| Server | 2× A100 | Full batch throughput |
| Air-gapped | Any x86/ARM | Zero network dependency |