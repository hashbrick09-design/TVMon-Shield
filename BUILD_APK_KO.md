# TVMon APK 자동 빌드 안내 (설정 최소화)

이 프로젝트는 GitHub Actions를 이용해 APK를 자동으로 빌드합니다. PC에 Android Studio나 Android SDK를 설치할 필요가 없습니다.


## 1. GitHub 저장소 만들기 (한 번만)
1. https://github.com 에 로그인합니다.
2. 오른쪽 위 `+` → `New repository`를 누릅니다.
3. Repository name에 `TVMon-Shield` 입력, `Public` 또는 `Private` 선택 후 `Create repository`.
4. 저장소 화면에서 `Add file` → `Upload files`를 선택합니다.
5. 이 ZIP을 PC에서 먼저 압축 해제한 후, 안의 `SimpleBrowser` 폴더와 `BUILD_APK_KO.md` 파일을 저장소 루트에 업로드합니다. (숨김 폴더 `.github`도 반드시 포함되도록 업로드; 숨김 폴더 업로드가 불편하면 아래 방법 사용)


## 2. 자동 빌드 실행
- 저장소의 `Actions` 탭 → `Build TVMon APK` workflow 선택
- `Run workflow` 버튼 → `Run workflow` 눌러 시작
- 진행 중인 작업이 초록 체크(성공)로 바뀌면 실행을 클릭합니다.

## 3. APK 내려받기
- 성공한 실행 화면 아래 `Artifacts`에서 `TVMon-APK` 클릭
- 다운로드한 ZIP 압축을 풀면 `app-debug.apk`가 있습니다.

## 4. SHIELD TV 설치
- `app-debug.apk`를 USB에 복사해 TV에 연결하고 APK 설치 앱(파일 관리자)으로 열어 설치합니다.
- Android에서 출처를 알 수 없는 앱 설치 허용을 요청할 수 있습니다. TV 설정에서 APK를 여는 파일 관리자에 설치 권한을 허용하세요.


## 참고
- APK는 GitHub Actions에서 매번 새로 생성됩니다. 빌드 성공 전 APK가 만들어졌다고 보장하지 않습니다.
- 이 workflow는 debug APK를 만듭니다. 개인 테스트 설치용이며 Play Store 배포 서명 APK가 아닙니다.
