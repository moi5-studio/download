# 제3자 오픈소스 고지 (Third-Party Notices)

moi5 Studio 는 아래 오픈소스 구성요소를 사용합니다. 각 구성요소의 저작권은
원 저작자에게 있으며, 해당 라이선스 조건에 따라 사용·배포됩니다.

최종 갱신: 2026-11-11

---

## 1. 함께 배포되는 구성요소 (bundled)

앱 설치본에 **파일로 포함**되어 배포되므로, 아래 라이선스 원문을 **반드시 함께
배포**해야 합니다.

### llama.cpp — 로컬 LLM 추론 엔진

| 항목 | 내용 |
|---|---|
| 빌드 | `b10777` (win-cpu-x64, ggml-org 공식 릴리스) |
| 출처 | https://github.com/ggml-org/llama.cpp/releases/tag/b10777 |
| 라이선스 | MIT |
| 저작권 | Copyright (c) 2023-2026 The ggml authors |
| 원문 위치 | `engine/LICENSE-llama.cpp` |

포함 파일: `engine/llama-server.exe`, `engine/ggml*.dll`, `engine/llama.dll` 등

> MIT 는 **저작권 표시와 허가 표시를 소프트웨어의 모든 복사본 또는 중요한
> 부분에 포함**할 것을 요구합니다. `engine/` 폴더를 재배포할 때
> `LICENSE-llama.cpp` 를 반드시 함께 배포하십시오.

### LLVM OpenMP 런타임 (llama.cpp 에 vendored)

| 항목 | 내용 |
|---|---|
| 라이선스 | Apache License 2.0 with LLVM Exception |
| 원문 위치 | `engine/LICENSE-LLVM-OpenMP` |

> Apache-2.0 은 라이선스 사본 제공과 **NOTICE 파일 유지**를 요구합니다.

### pypdf — PDF 본문 추출

| 항목 | 내용 |
|---|---|
| 버전 | 6.19.0 |
| 출처 | https://pypi.org/project/pypdf/ |
| 라이선스 | BSD-3-Clause |
| 저작권 | Copyright (c) 2006-2008, Mathieu Fenniak (외 기여자 — 원문 참고) |
| 원문 위치 | `licenses/LICENSE-pypdf.txt` |

지식 넣기(드롭존 · 폴더 학습 · 새 자료 정리)의 PDF 글자 추출에 쓴다(2026-09-30 추가).

> BSD-3-Clause 는 **바이너리로 재배포할 때 저작권 표시·조건·면책 문구를 문서에
> 함께 넣을 것**을 요구합니다. `licenses/LICENSE-pypdf.txt` 를 함께 배포하십시오.

### 파이썬 런타임과 함께 들어가는 파이썬 구성요소 (2026-11-11 보완)

설치본(PyInstaller)에 아래가 함께 들어갑니다. 원문은 모두 `licenses/` 에 있습니다.
목록은 실제 빌드 목록에서 뽑았고, 원문은 빌드에 쓴 설치 정보에서 그대로 복사했습니다(`tools/python_licenses.py`).

| 구성요소 | 버전 | 라이선스 | 원문 |
|---|---|---|---|
| Python 런타임 (bzip2 · libffi · OpenSSL · Tcl/Tk 포함) | 3.12.0 | PSF-2.0 · OpenSSL 은 Apache-2.0 | `LICENSE-python-runtime.txt` |
| Pillow | 11.3.0 | MIT-CMU (함께 든 이미지 라이브러리 조건 포함) | `LICENSE-python-pillow.txt` |
| numpy (OpenBLAS · LAPACK · GCC 런타임 포함) | 2.5.4 | BSD-3-Clause 외 · GCC 런타임은 GPL-3.0 + 런타임 예외 | `LICENSE-python-numpy.txt` |
| onnxruntime | 1.31.0 | MIT (제3자 고지 포함) | `LICENSE-python-onnxruntime.txt` |
| tokenizers (Hugging Face) | 0.23.3 | Apache-2.0 | `LICENSE-python-tokenizers.txt` |
| lxml (libxml2 · libxslt 포함) | 6.1.3 | BSD-3-Clause | `LICENSE-python-lxml.txt` |
| python-docx | 1.2.0 | MIT | `LICENSE-python-python-docx.txt` |
| requests | 2.32.5 | Apache-2.0 | `LICENSE-python-requests.txt` |
| urllib3 | 2.8.0 | MIT | `LICENSE-python-urllib3.txt` |
| certifi | 2026.7.22 | MPL-2.0 (원본: pypi.org/project/certifi) | `LICENSE-python-certifi.txt` |
| charset-normalizer | 3.5.1 | MIT | `LICENSE-python-charset-normalizer.txt` |
| idna | 3.20 | BSD-3-Clause | `LICENSE-python-idna.txt` |
| defusedxml | 0.7.1 | PSF-2.0 | `LICENSE-python-defusedxml.txt` |
| typing_extensions | 4.16.0 | PSF-2.0 | `LICENSE-python-typing_extensions.txt` |
| PyYAML | 6.0.3 | MIT | `LICENSE-python-PyYAML.txt` |
| youtube-transcript-api | 1.2.4 | MIT | `LICENSE-python-youtube-transcript-api.txt` |
| pypdf | 6.19.0 | BSD-3-Clause | `LICENSE-pypdf.txt` (위 항목) |

- 파이썬 런타임에 함께 든 expat · mpdecimal · zlib · SQLite · xz 등의 조건은 Python 공식 고지에 있습니다:
  https://docs.python.org/3.12/license.html#licenses-and-acknowledgements-for-incorporated-software
- Microsoft Visual C++ 런타임(`vcruntime140.dll` 등)은 Microsoft 재배포 허용 파일입니다.
- 실행 파일의 시작 부분(PyInstaller 부트로더)은 GPL-2.0 + 예외 조항으로, 프로그램을 어떤 조건으로든 배포할 수 있게 허용합니다.
- **PyMuPDF(AGPL-3.0)는 설치본에 들어 있지 않습니다**(2026-11-11 빌드 목록 확인). 예전 이 절의 경고는 지웠습니다.
- 빌드에 꾸러미가 새로 들어가면 `py -3.12 tools/python_licenses.py --check` 와 배포 점검이 실패합니다. 원문을 모으고 이 표에 한 줄 더하십시오.

### 판정 모델 2종 — bge-m3 · mDeBERTa (2026-11-09 추가)

| 모델 | 쓰임 | 라이선스 | 저작권 |
|---|---|---|---|
| BAAI bge-m3 (`ggml-org/bge-m3-Q8_0-GGUF`) | 지식 검색 · moi5-System1 판정 | MIT | Copyright (c) 2022 staoxiao |
| mDeBERTa-v3-base-xnli-multilingual-nli-2mil7 (ONNX) | 인용 대조(근거에 없는 문장 표시) | MIT | Moritz Laurer · 바탕 모델 Microsoft mDeBERTa-v3-base(MIT) |

원문 위치: `licenses/LICENSE-judge-models.txt` · 설치 위치: `.data/embedding/` · `.data/nli-mdeberta/`

> 설치본이 이 두 모델 파일을 **직접 담아** 배포하므로 MIT 원문과 저작권 표시를 함께 배포합니다.
> 그 밖의 모델(답을 쓰는 모델 · 판정 엔진 등)은 아래 3절대로 사용자가 직접 내려받습니다.

---

## 2. 함께 배포되는 화면 구성요소 (bundled · frontend/vendor/)

**2026-09-22 변경: CDN 로드 → 로컬 번들.** 아래 항목은 이제 `frontend/vendor/`
에 **포함되어 배포**됩니다. 따라서 **재배포에 해당**하며, 각 라이선스 원문을
`frontend/vendor/licenses/` 에 동봉합니다.

왜 바꿨나 — 예전에는 아이콘·글꼴·마크다운 렌더러를 외부 CDN 에서 받아왔습니다.
그래서 **인터넷이 없으면 화면이 깨졌고**(아이콘 317곳), 앱을 켤 때마다 사용자
IP 가 4개 CDN 사업자에게 전달됐습니다. "로컬 AI" 를 표방하는 앱으로서 맞지
않아 전부 내려받아 함께 배포합니다.

| 구성요소 | 버전 | 라이선스 | 원문 | 용도 |
|---|---|---|---|---|
| [Font Awesome Free](https://fontawesome.com) | 6.4.0 | 아이콘 CC BY 4.0 · 코드 MIT · 폰트 SIL OFL 1.1 | `LICENSE-fontawesome.txt` | UI 아이콘 |
| [highlight.js](https://highlightjs.org) | 11.7.0 | BSD-3-Clause | `LICENSE-highlightjs.txt` | 코드 구문 강조 |
| [marked](https://marked.js.org) | **12.0.2** | MIT | `LICENSE-marked.txt` | 마크다운 렌더링 |
| [SheetJS (xlsx)](https://sheetjs.com) | 0.18.5 | Apache-2.0 | `LICENSE-sheetjs.txt` | 엑셀(.xlsx) 내보내기 |
| [vis-network](https://visjs.org) | **9.1.9** | Apache-2.0 또는 MIT | `LICENSE-vis-network.txt` | 지식 별자리 그래프 |
| Inter / Montserrat / JetBrains Mono | Google Fonts | SIL OFL 1.1 | `LICENSE-inter-OFL.txt` 외 2종 | 본문·제목·모노 서체 |
| [Pretendard](https://github.com/orioncactus/pretendard) | 1.3.9 (가변) | SIL OFL 1.1 | `LICENSE-pretendard-OFL.txt` | 한글 본문 서체 |

> **Pretendard 관련 기록** — 예전에는 Google Fonts 에 Pretendard 를 요청했으나
> **Google Fonts 는 Pretendard 를 제공하지 않습니다.** 요청은 나갔지만 글꼴은
> 오지 않았고, 한글은 시스템 대체 글꼴로 표시되고 있었습니다. 이제 배포처에서
> 가변폰트를 직접 가져와 번들하므로 의도한 서체가 실제로 적용됩니다.

> **앞으로 라이브러리를 추가할 때** — CDN 링크를 그대로 넣지 마십시오.
> `frontend/vendor/` 에 내려받아 넣고, 라이선스 원문을 `vendor/licenses/` 에
> 함께 두고, 위 표에 한 줄 추가하십시오.

---

## 3. 사용자가 직접 내려받는 AI 모델 (user-obtained)

모델 가중치(GGUF)는 앱이 재배포하지 않습니다. 사용자가 Hugging Face 등에서
**직접 내려받아** 자신의 PC 에 저장합니다. 따라서 모델 라이선스는
**사용자와 모델 제작사 사이**의 조건이 적용됩니다.

앱은 각 모델의 라이선스와 **상업적 이용 가부를 화면에 표시**합니다
(구현: `backend/modules/models/criteria.py`).

| 모델 계열 | 라이선스 | 상업적 이용 |
|---|---|---|
| LG EXAONE | EXAONE License | **불가** (경고 배지 표시) |
| NAVER HyperCLOVA X SEED | HyperCLOVAX SEED License | 조건 확인 필요 |
| Gemma · Mistral · Granite 등 | Apache-2.0 등 | 대체로 가능 (개별 확인) |
| BAAI bge-m3 — 지식 검색 모델 (`ggml-org/bge-m3-Q8_0-GGUF`, 설치본에 함께 들어 있음 · 1절) | MIT | 가능 |

> 모델을 업무에 사용하기 전 해당 모델 저장소의 라이선스를 직접 확인하십시오.
>
> 알리바바 **Qwen 계열 모델은 이 앱이 추천 · 검색 · 내려받기 · 실행에서 제외합니다.**

---

## 4. moi5 Studio 자체

moi5 Studio 애플리케이션 코드와 디자인 자산(로고·아이콘 포함)의 저작권은
아래에 있습니다.

```
Copyright (c) 2026 moi5. All rights reserved.
```

본 고지는 **제3자 구성요소**에 대한 것입니다.
moi5 Studio 자체의 이용 조건은 함께 배포되는 **`LICENSE.md`**(최종 사용자
이용약관)를 따르며, 외부 통신 범위는 **`PRIVACY.md`** 에 명시되어 있습니다.

---

## 갱신 방법

구성요소를 추가·교체·버전 변경할 때 이 문서를 함께 갱신하십시오.

- **번들 엔진 교체 시**: `engine/` 의 라이선스 파일과 `engine/BUNDLE_INFO.txt`
  의 빌드 번호를 새 릴리스의 원문으로 교체하고, 위 1절의 빌드·저작권 연도를 갱신
- **화면 라이브러리 추가 시**: `frontend/vendor/` 에 파일을, `vendor/licenses/`
  에 라이선스 원문을 넣고 2절 표에 한 줄 추가 (CDN 링크를 그대로 쓰지 말 것)
- **버전 올릴 때**: 파일 교체와 함께 2절 표의 버전 숫자도 갱신
