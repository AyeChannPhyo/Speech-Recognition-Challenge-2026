# Speech Recognition Challenge 2026

학생은 `submission/` 폴더에 **HTML 파일 1개만** 추가한 뒤 Pull Request(PR)로 제출합니다.

## 제출 파일

파일명은 아래 형식을 사용합니다.

```text
submission/Team_<팀대표이름>_<학번>.html
```

## HTML 필수 구성

제출 HTML에는 아래 항목을 순서대로 작성합니다.

1. Challenge 제목 및 팀 구성원
2. Challenge Description
3. 입력 → 모델 → 출력 흐름
4. Baseline & Method
5. Dataset
6. Evaluation Setup
7. Leaderboard
8. References

다음 제출 조건을 지켜야 합니다.

- 팀별 주제, 방법, Dataset과 실험 결과를 직접 작성합니다.
- 사용한 모델, 논문, Dataset과 본인 코드의 링크를 연결합니다.
- Dataset의 학습용·평가용 구분과 평가 지표를 명시합니다.
- Baseline과 제안 방법을 같은 Evaluation Setup으로 비교합니다.
- 스타일은 HTML 내부의 `<style>`에 작성합니다.
- 별도 CSS, JavaScript, 이미지 또는 제출용 하위 폴더는 추가하지 않습니다.

## 제출 방법

### 1. Fork 및 Clone

GitHub에서 이 저장소를 자신의 계정으로 Fork한 뒤 Clone합니다.

```bash
git clone https://github.com/GITHUB_ID/Speech-Recognition-Challenge-2026.git
cd Speech-Recognition-Challenge-2026
git remote add upstream https://github.com/LSH-Ajou/Speech-Recognition-Challenge-2026.git
```

### 2. Branch 및 HTML 파일 생성

팀 대표 이름과 학번을 사용해 Branch와 제출 파일을 만듭니다.

```bash
git switch -c submission/team-name-studentid
```

`submission/Team_NAME_STUDENTID.html` 파일을 새로 만들고 Challenge 내용을 작성합니다.

### 3. Commit 및 Push

```bash
git add submission/Team_NAME_STUDENTID.html
git commit -m "submission: add Team_NAME_STUDENTID"
git push -u origin submission/team-name-studentid
```

`NAME`과 `STUDENTID`는 팀 대표의 실제 정보로 바꿉니다. 자신의 제출 HTML 이외의 파일은 수정하지 않습니다.

### 4. Pull Request 제출

GitHub에서 **Compare & pull request**를 선택하고 아래 대상으로 PR을 만듭니다.

```text
base repository: LSH-Ajou/Speech-Recognition-Challenge-2026
base branch: main
head repository: GITHUB_ID/Speech-Recognition-Challenge-2026
compare branch: submission/team-name-studentid
```

PR 제목:

```text
[Submission] Team_NAME_STUDENTID
```

수정 요청을 받으면 같은 Branch에서 수정한 뒤 다시 Commit하고 Push합니다. 기존 PR에 자동으로 반영됩니다.
