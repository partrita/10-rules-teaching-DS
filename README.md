# 데이터 과학 교육을 위한 10가지 간단한 규칙

> Timbers, T. A., & Çetinkaya-Rundel, M. (2026). Ten simple rules for teaching data science (arXiv:2602.02874). arXiv. https://doi.org/10.48550/arXiv.2602.02874

이 저장소는 "데이터 과학 교육을 위한 10가지 간단한 규칙" 논문을 바탕으로 한 Quarto 책 프로젝트입니다. [Pixi](https://prefix.dev/)를 사용하여 의존성을 관리하며, GitHub Pages를 통해 배포됩니다.

## 프로젝트 구조

- `mybook/`: Quarto 책 소스 파일(`.qmd`)이 포함되어 있습니다. `index.qmd`에 주요 내용이 담겨 있습니다.
- `pixi.toml`: Quarto 및 필요한 라이브러리 의존성을 관리합니다.
- `.github/workflows/publish.yml`: 책을 자동으로 빌드하고 배포하는 GitHub Action 설정 파일입니다.

## 사용법 (Usage)

### 사전 준비

- 기기에 [Pixi](https://prefix.dev/)가 설치되어 있어야 합니다.

### 로컬 개발 및 미리보기

1.  **저장소 복제:**

    ```bash
    git clone https://github.com/partrita/10-rules-teaching-DS.git
    cd 10-rules-teaching-DS
    ```

2.  **책 미리보기:**

    다음 명령어를 실행하면 필요한 도구를 설치하고 라이브 서버를 시작합니다.

    ```bash
    pixi run quarto preview mybook
    ```

    책을 렌더링하려면 다음 명령어를 사용하세요:

    ```bash
    pixi run quarto render mybook
    ```

### 의존성 관리

이 프로젝트는 `pixi`를 사용하여 의존성을 관리합니다.

Python 또는 R 패키지를 추가하려면:

```bash
pixi add python pandas  # Python 패키지 예시
# 또는
pixi add r-base r-tidyverse  # R 패키지 예시
```

## 배포 (Deployment)

GitHub Actions를 통해 GitHub Pages에 자동으로 배포되도록 설정되어 있습니다. `main` 브랜치에 푸시하면 빌드 및 배포 워크플로우가 트리거됩니다.

최종 배포 사이트: https://partrita.github.io/10-rules-teaching-DS/