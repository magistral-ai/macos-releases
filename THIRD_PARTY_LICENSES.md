# Licences et attributions tierces — WebhookForge

WebhookForge intègre les composants tiers suivants pour la transcription vocale locale.

---

## Modèle de reconnaissance vocale : NVIDIA Parakeet TDT 0.6B v3

- **Auteur** : NVIDIA Corporation
- **Licence** : Creative Commons Attribution 4.0 International (CC-BY-4.0)
  — https://creativecommons.org/licenses/by/4.0/
- **Source d'origine** : https://huggingface.co/nvidia/parakeet-tdt-0.6b-v3
- **Modifications** : quantification int8 et conversion au format ONNX par le projet
  k2-fsa/sherpa-onnx (https://huggingface.co/csukuangfj/sherpa-onnx-nemo-parakeet-tdt-0.6b-v3-int8).
- Le modèle n'est pas distribué avec l'application : il est téléchargé par l'utilisateur
  au premier usage (Réglages → Général → Transcription des vocaux).

---

## Moteur d'inférence : sherpa-onnx

- **Auteurs** : Xiaomi Corporation et contributeurs du projet k2-fsa
- **Licence** : Apache License 2.0 — http://www.apache.org/licenses/LICENSE-2.0
- **Source** : https://github.com/k2-fsa/sherpa-onnx
- Lié statiquement dans l'application (bibliothèque `libsherpa-onnx`), incluant le wrapper
  Swift officiel (`SherpaOnnx.swift`, Copyright (c) 2023 Xiaomi Corporation).

```
Copyright (c) 2022-2025 Xiaomi Corporation and k2-fsa contributors

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```

---

## ONNX Runtime

- **Auteur** : Microsoft Corporation
- **Licence** : MIT — https://github.com/microsoft/onnxruntime/blob/main/LICENSE
- **Source** : https://github.com/microsoft/onnxruntime
- Lié statiquement dans l'application (via la distribution sherpa-onnx).

```
MIT License

Copyright (c) Microsoft Corporation

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

## Outils optionnels détectés sur la machine (non distribués)

`whisper-cli` (whisper.cpp, MIT) et `ffmpeg` (LGPL/GPL) peuvent être utilisés comme moteur
de repli s'ils sont déjà installés par l'utilisateur. Ils ne sont ni inclus ni distribués
avec WebhookForge.
