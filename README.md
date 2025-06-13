# textminer-pro

textminer-pro는 불용어 제거, 핵심 키워드 추출, 텍스트 요약, 언어 감지 기능을 제공하는 고급 텍스트 분석 Python 패키지입니다.
간단한 API 호출만으로 자연어 텍스트를 전처리하고 요약할 수 있도록 설계되었습니다.

---

## 설치 방법

PyPI에 정식 등록된 패키지이므로 다음 명령어로 설치할 수 있습니다:

```
pip install textminer-pro
```

---

## 기능 요약

| 기능     | 설명                     | 함수 이름                    |
| ------ | ---------------------- | ------------------------ |
| 불용어 제거 | 영어 불용어(stopwords)를 제거  | `remove_stopwords(text)` |
| 키워드 추출 | TF-IDF 기반 상위 N개 키워드 추출 | `extract_keywords(text)` |
| 텍스트 요약 | Sumy 기반 문서 요약          | `summarize_text(text)`   |
| 언어 감지  | 텍스트의 언어 자동 감지          | `detect_language(text)`  |

---

## 예제 코드

```python
from textminer import (
    remove_stopwords,
    extract_keywords,
    summarize_text,
    detect_language
)

text = "Natural Language Processing is a subfield of Artificial Intelligence."

print(remove_stopwords(text))
print(extract_keywords(text))
print(summarize_text(text))
print(detect_language(text))
```

---

## 프로젝트 구조

```
textminer_pro/
├── textminer/                   # 텍스트 처리 기능 모듈
│   ├── __init__.py              # 패키지 초기화
│   ├── cleaner.py               # 불용어 제거, 키워드 추출
│   ├── summarizer.py            # 요약 기능
│   └── detector.py              # 언어 감지
│
├── tests/                       # 기능 테스트 파일
│   ├── test_cleaner.py
│   └── test_detector.py
│
├── docs/                        # mkdocs 문서 디렉토리
│   ├── index.md
│   └── usage/
│       ├── stopwords.md
│       ├── keywords.md
│       ├── summarize.md
│       └── detect.md
│
├── setup.py                     # 패키지 설정 및 배포 스크립트
├── mkdocs.yml                   # MkDocs 설정 파일
└── README.md                    # 프로젝트 설명 파일
```

