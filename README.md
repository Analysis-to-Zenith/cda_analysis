# 2026 빅콘테스트 — 기후 위기에 따른 취약 상권 영향 분석 (CDA·인과추론·문제 발굴)

제14회 2026 빅콘테스트 AI데이터 분석 분야. 이 저장소는 EDA·가설 설정 저장소([eda_analysis](https://github.com/Analysis-to-Zenith/eda_analysis))의 결과를 이어받아 **확증적 분석(CDA)과 인과추론**을 하고, 이를 바탕으로 **문제점을 발굴**한다.

## 진행 절차
| 단계 | 노트북 | 브랜치 | 상태 |
|---|---|---|---|
| 1. 가설 기반 인과추론 | `notebooks/01_causal_inference.ipynb` | `ana-causal` | 완료 |
| 2. 데이터 엔지니어링 | `notebooks/02_feature_engineering.ipynb` | `ana-engin` | 완료 |
| 3. 논문 근거 기후 피해 예측 | `notebooks/03_damage_prediction.ipynb` | `ana-pred` | 완료 |
| 4. 논문 근거 취약도 지수 | `notebooks/04_vulnerability_index.ipynb` | `ana-vuln` | 예정 |
| 5. 논문 근거 지원금 최적화 | `notebooks/05_support_optimization.ipynb` | `ana-opt` | 예정 |
| 6. 문제점 발굴 | `notebooks/06_problem_discovery.ipynb` | `ana-problem` | 예정 |

## 결론 방향
기후에 따른 매출 피해를 명확히 알지 못하면 지원이 불분명해져, 정말 필요한 곳에 지원하지 못할 수 있다.
→ **기후 피해 예측**이 필요하고, 이를 더 정확히 하려면 **취약도 지수**가 필요하며, 그 결과로 **지원금 최적화**를 해야 한다. 이 과정을 **대시보드**로 볼 수 있어야 한다 (서비스 구현은 이후).

## 폴더 구조
```
cda_analysis/
├─ data/                 # git 제외 (대회 데이터 외부 공유 금지)
│  └─ processed/         # eda_analysis 산출물 복사본 + 이 저장소 노트북 산출물
├─ references/           # 가설 판정표 등 집계 결과 (git 관리)
└─ notebooks/            # 단계별 분석 노트북 (커널: Python (bigcon))
```

## 환경·실행
```bash
conda activate bigcon
jupyter lab   # 또는 VS Code에서 커널 "Python (bigcon)" 선택
```
- `eda_analysis` 저장소가 같은 상위 폴더에 있고 그 노트북을 먼저 실행해 `eda_analysis/data/processed/`가 만들어져 있어야 한다. 01 노트북이 필요한 파일을 `data/processed/`로 복사한다.
- 노트북은 `notebooks/` 폴더에서 번호 순서대로 실행한다.
