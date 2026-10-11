# Speech Recognition Challenge 2026

학생은 `submission/` 폴더에 **HTML 파일 1개만** 추가한 뒤 Pull Request(PR)로 제출합니다.

## 제출 파일

파일명은 아래 형식을 사용합니다.

```text
submission/Team_<팀대표이름>_<학번>.html
```

### 2. 과제 제출 내용

#### 과제는 HTML 페이지 형태로 구성하며, 아래 항목은 반드시 포함해야 합니다.

<ol>
  <li><strong>메인화면</strong>: <code>index.html</code></li>
  <li><strong>Challenge 설명</strong>: Challenge 개요 및 프로젝트 내용</li>
  <li><strong>Leaderboard</strong>: 벤치마크 결과 및 성능 비교</li>
  <li>개인 GitHub 링크: 아래 항목을 포함한 Repository
    <ol type="a">
      <li>Baseline 코드</li>
      <li>Dataset(Evaluation용 데이터셋 필수 포함)</li>
      <li>Evaluation: 모델 평가 방법 및 관련 코드</li>
    </ol>
  </li>
</ol>

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
