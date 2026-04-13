# 노트북 목록

| 파일 | 상태 | 목적 | 경로 메모 |
| --- | --- | --- | --- |
| `preprocess_all.ipynb` | 정상 JSON | 데이터 불러오기와 정제 | 원본은 로컬 절대 경로를 사용했습니다. 정리본은 상대 경로를 사용합니다. |
| `brazil_home_decor_strategy.ipynb` | 정상 JSON | 전략 서술과 카테고리 순위 분석 | 원본은 로컬 절대 경로를 사용했습니다. 정리본은 상대 경로를 사용합니다. |
| `olist_home_living_eda.ipynb` | 원본 JSON 파싱 문제 | EDA, 카테고리 시각화, 전처리 로직 | 원본은 그대로 두고 별도 요약 노트북을 만들었습니다. |
| `olist_home_living_eda copy.ipynb` | 원본 JSON 파싱 문제 | EDA 노트북 복사본 | 원본은 그대로 둡니다. |
| `olist_home_living_project.ipynb` | 원본 JSON 파싱 문제 | 최종 홈앤리빙 보고서 | 원본은 그대로 두고 별도 요약 노트북을 만들었습니다. |
| `olist_home_living_project2.ipynb` | 원본 JSON 파싱 문제 | 보고서 노트북 복사본 | 원본은 그대로 둡니다. |

## 추천 실행 순서

1. `notebooks/01_preprocess_all.ipynb`
2. `notebooks/02_home_living_analysis_summary.ipynb`
3. `notebooks/03_growth_strategy_summary.ipynb`

## 상대 경로 규칙

정리된 노트북은 아래 구조를 기준으로 합니다.

```text
house_of_brazil/
|-- data/
`-- notebooks/
```

아래와 같은 데이터 로더 패턴을 사용합니다.

```python
from pathlib import Path
import pandas as pd

BASE_DIR = Path("..")
DATA_DIR = BASE_DIR / "data"

def load_csv(filename: str) -> pd.DataFrame:
    return pd.read_csv(DATA_DIR / filename)
```

