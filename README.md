# Speech Recognition Challenge 2026

학생은 `submission/` 폴더에 **HTML 파일 1개만** 추가한 뒤 Pull Request(PR)로 제출합니다.

[GitHub Pages에서 샘플 HTML 보기](https://lsh-ajou.github.io/Speech-Recognition-Challenge-2026/)

파일명은 아래 형식을 사용합니다.

```text
submission/Team_<팀대표이름>_<학번>.html
```

예: `submission/Team_hongildong_202612345.html`

## 제출 방법

### 1. Fork 및 Clone

GitHub에서 이 저장소를 자신의 계정으로 Fork한 뒤 Clone합니다.

```bash
git clone https://github.com/<GITHUB_ID>/Speech-Recognition-Challenge-2026.git
cd Speech-Recognition-Challenge-2026
git remote add upstream https://github.com/LSH-Ajou/Speech-Recognition-Challenge-2026.git
```

### 2. 샘플 복사 및 파일명 변경

macOS 또는 Linux:

```bash
cp submission/Team_sample_202624123.html submission/Team_hongildong_202612345.html
```

Windows PowerShell:

```powershell
Copy-Item submission/Team_sample_202624123.html submission/Team_hongildong_202612345.html
```

`hongildong` 부분은 팀 대표 이름으로, `202612345` 부분은 팀 대표의 학번으로 바꿉니다.

### 3. HTML 작성

복사한 [샘플 HTML](./submission/Team_sample_202624123.html)의 내용을 자신의 Challenge에 맞게 바꿉니다. 페이지는 아래 흐름을 따릅니다.

```text
Challenge 제목 · 팀 구성원
        ↓
Goal
        ↓
Method (번호별 단계와 관련 링크)
        ↓
Input → Processing → Output
        ↓
Dataset → Evaluation Setup → Leaderboard → References
```

#### 3-1. Challenge 제목 및 팀 구성원

- 페이지 맨 위에 Challenge의 핵심이 드러나는 짧은 제목을 작성합니다.
- 제목 아래에 모든 팀원의 이름과 학번을 한 줄로 작성합니다.

```text
Fine-Grained Emotional TTS Challenge
Team Members: student1 (202600001) · student2 (202600002) · student3 (202600003)
```

#### 3-2. Goal

해결하려는 문제와 최종 결과를 1~2문장으로 설명합니다.

```text
텍스트와 목표 감정을 입력받아 해당 감정이 표현된 음성을 생성합니다.
```

#### 3-3. Method

전체 방법을 실행 순서에 따라 번호로 나누어 작성합니다. 각 단계에는 사용한 모델이나 도구를 적고, 논문·공식 저장소·본인 GitHub 코드 링크를 연결합니다.

```text
1. Expresso 데이터 전처리 및 학습 준비
   → 본인 GitHub 전처리 코드 링크
2. Spark-TTS Fine-tuning과 추론으로 감정 음성 생성
   → https://github.com/SparkAudio/Spark-TTS
   → 본인 GitHub 학습·추론 코드 링크
3. emotion2vec-plus-large와 NISQA로 성능 평가
   → 본인 GitHub 평가 코드 링크
```

링크는 클릭할 수 있도록 작성합니다.

```html
<a href="https://github.com/SparkAudio/Spark-TTS">Spark-TTS</a>
```

#### 3-4. 입력 → 처리 → 출력 흐름도

입력, 핵심 처리 과정, 출력을 한눈에 볼 수 있는 흐름도를 넣습니다. 별도 이미지 파일을 추가하지 말고 샘플 HTML의 파이프라인 영역처럼 HTML과 CSS로 작성합니다.

```text
Text + Emotion → Spark-TTS → Generated Speech
```

#### 3-5. Dataset

Dataset 이름, Train/Evaluation 구분, 사용 목적과 전처리 코드 링크를 표로 작성합니다.

| Dataset | Split | Usage | Preprocessing Code |
| --- | --- | --- | --- |
| Expresso | Train | 감정 표현 학습 | 본인 GitHub 전처리 코드 링크 |
| ESD | Evaluation | 감정별 음성 평가 | 본인 GitHub 전처리 코드 링크 |

전처리 코드는 제출 HTML에 포함하지 않고 자신의 공개 GitHub 저장소로 연결합니다.

```html
<a href="https://github.com/<GITHUB_ID>/<REPOSITORY>/tree/main/preprocessing">본인 GitHub 전처리 코드 링크</a>
```

#### 3-6. Evaluation Setup

평가에 사용한 모델, 평가 지표, 평가 데이터의 클래스와 개수를 작성합니다.

```text
emotion2vec-plus-large로 Emotion Accuracy를 계산하고 NISQA로 음질을 평가했습니다.
happy, angry, sadness, surprise, fearful, neutral 데이터를 각 100개씩, 총 600개 사용했습니다.
```

#### 3-7. Leaderboard

Baseline과 제안 방법의 결과를 같은 평가 지표로 비교합니다. 높은 값이 좋은 지표는 `↑`, 낮은 값이 좋은 지표는 `↓`로 표시합니다.

| Rank | Model | Emotion Accuracy ↑ | NISQA ↑ |
| ---: | --- | ---: | ---: |
| 1 | Proposed Method | 0.88 | 4.11 |
| 2 | Baseline | 0.81 | 4.05 |

위 숫자는 형식을 보여주기 위한 예시이므로 실제 실험 결과로 교체합니다.

#### 3-8. References

참고한 논문, Dataset, 모델과 코드의 원문 링크를 작성합니다.

```text
EMORL-TTS paper
Expresso Dataset
ESD Dataset
Spark-TTS repository
```

제출물은 HTML 파일 하나이므로 스타일은 HTML 내부의 `<style>`에 작성합니다. 제출용 하위 폴더, 별도 CSS, 이미지 또는 JavaScript 파일은 추가하지 않습니다.

### 4. Branch, Commit 및 Push

```bash
git switch -c submission/team-hongildong-202612345
git add submission/Team_hongildong_202612345.html
git commit -m "submission: add Team_hongildong_202612345"
git push -u origin submission/team-hongildong-202612345
```

위 예시의 이름과 학번은 자신의 제출 정보로 바꾸어 사용합니다. 자신의 HTML 파일 외의 파일은 수정하지 않습니다.

### 5. Pull Request 제출

GitHub에서 **Compare & pull request**를 선택하고 아래 대상으로 PR을 만듭니다.

```text
base repository: LSH-Ajou/Speech-Recognition-Challenge-2026
base branch: main
head repository: <GITHUB_ID>/Speech-Recognition-Challenge-2026
compare branch: submission/team-hongildong-202612345
```

PR 제목:

```text
[Submission] Team_hongildong_202612345
```

수정 요청을 받으면 같은 Branch에서 수정한 뒤 다시 Commit하고 Push합니다. 기존 PR에 자동으로 반영됩니다.
