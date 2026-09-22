# Голоса «Сойки»

Готовые к работе модели распознавания речи для приложения «Сойка» (Android).
Здесь лежат только переупакованные файлы: исходные модели сделаны другими людьми,
ссылки и лицензии — ниже.

## Иврит, лёгкий — GigaAM-He CTC (ONNX, int8)

* Источник: [asfberlin/fast-hebrew-asr](https://huggingface.co/asfberlin/fast-hebrew-asr) — MIT
* Базовая модель: [salute-developers/GigaAM](https://github.com/salute-developers/GigaAM) — MIT
* Что сделано: экспорт в ONNX штатным `to_onnx()` пакета `gigaam`, метаданные
  для sherpa-onnx (`EncDecCTCModel`, `is_giga_am=1`, `subsampling_factor=4`),
  динамическая квантизация в QUInt8, словарь из 68 символов в `tokens.txt`.
* Файлы: `model.int8.onnx`, `tokens.txt`

Лицензия на сами файлы — MIT, как у источника.
