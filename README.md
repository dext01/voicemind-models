# VoiceMind — зеркало моделей

Файлы моделей, которые скачивает приложение [VoiceMind](https://voice-mind.ru)
(офлайн-расшифровка и ИИ-анализ записей на телефоне). Зеркало нужно, чтобы
приложение продолжало работать, даже если исходный файл удалят или переименуют.
Приложение качает отсюда в первую очередь, исходный источник остаётся запасным.

Файлы лежат в релизе [`models-v1`](../../releases/tag/models-v1) и побайтно
совпадают с исходными. После загрузки приложение проверяет SHA-256.

| Файл | Что это | Источник |
|---|---|---|
| `ggml-whisper-podlodka-turbo-q4_0.bin` | Распознавание речи: Whisper large-v3-turbo, дообученный на русском (bond005/whisper-podlodka-turbo), GGML q4_0 | [JoaoZaokk/whisper-podlodka-turbo-ggml](https://huggingface.co/JoaoZaokk/whisper-podlodka-turbo-ggml) |
| `ggml-small-q5_1.bin` | Распознавание, режим «Быстрее»: Whisper small | [ggerganov/whisper.cpp](https://huggingface.co/ggerganov/whisper.cpp) |
| `gemma-2-2b-it-Q4_K_M.gguf` | ИИ-анализ: Gemma 2 2B instruct | [bartowski/gemma-2-2b-it-GGUF](https://huggingface.co/bartowski/gemma-2-2b-it-GGUF) |
| `qwen3-0.6b-v2-Q4_K_M.gguf` | ИИ-анализ: Qwen3-0.6B, дообученная командой VoiceMind на «Выделить главное» | VoiceMind |
| `wespeaker-voxceleb-resnet34-LM.onnx` | Разделение по голосам: эмбеддинги говорящих | [onnx-community/wespeaker-voxceleb-resnet34-LM](https://huggingface.co/onnx-community/wespeaker-voxceleb-resnet34-LM) |
| `pyannote-segmentation-3.0.onnx` | Разделение по голосам: сегментация | [onnx-community/pyannote-segmentation-3.0](https://huggingface.co/onnx-community/pyannote-segmentation-3.0) |
| `silero_vad.onnx` | Детектор речи | [snakers4/silero-vad](https://github.com/snakers4/silero-vad) |

Контрольные суммы — в `SHA256SUMS` (и в ассетах релиза).

## Лицензии

Каждая модель распространяется на условиях своего исходного репозитория
(ссылки в таблице).

**Gemma.** Gemma is provided under and subject to the Gemma Terms of Use found at
[ai.google.dev/gemma/terms](https://ai.google.dev/gemma/terms). Использование
Gemma также подчиняется [Gemma Prohibited Use Policy](https://ai.google.dev/gemma/prohibited_use_policy).

**VoiceMind Qwen 0.6B** — производная от [Qwen/Qwen3-0.6B](https://huggingface.co/Qwen/Qwen3-0.6B)
(Apache License 2.0).
