# 🚀 Galpi Release Artifacts

이 저장소는 [갈피(Galpi)](https://github.com/wisgraph/galpi-app) 애플리케이션의 정식 빌드 바이너리와 자동 업데이트 명세서를 보관하는 배포 전용 저장소입니다.

## 📦 배포 파일 구조

*   **`galpi_{version}_{arch}.dmg`**: macOS용 신규 설치 패키지입니다.
*   **`galpi.app.tar.gz`**: 기존 사용자를 위한 자동 업데이트용 패키지입니다. (디지털 서명 포함)
*   **`latest.json`**: 최신 버전 정보와 업데이트 경로가 담긴 명세서입니다.

## 🛠️ 개발자 배포 가이드

새로운 버전을 배포할 때는 다음 순서를 권장합니다.

1.  **빌드**: 메인 프로젝트 루트에서 `./release.sh`를 실행하여 결과물을 생성합니다.
2.  **푸시**: `release/` 폴더 내의 변경사항을 이 저장소로 푸시합니다.
3.  **Release 생성**:
    *   GitHub 웹사이트에서 **Create a new release**를 클릭합니다.
    *   태그는 `v1.0.0` 형식을 사용하고, **Set as the latest release**를 체크합니다.
    *   `release/v{version}/` 폴더 안에 생성된 3개 파일을 모두 업로드합니다.

## 🔗 업데이트 주소
Tauri 앱은 아래 경로를 통해 최신 업데이트를 확인하도록 설정되어 있습니다.
`https://github.com/wisgraph/galpi-release/releases/latest/download/latest.json`

---
Copyright © 2026 wisgraph. All rights reserved.
