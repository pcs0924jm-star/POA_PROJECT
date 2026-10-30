# POA_PROJECT

## 실행
https://pcs0924jm-star.github.io/POA_PROJECT/ 에서 실행합니다. 로컬에서는 `index.html`을 웹 서버로 제공합니다. CSS와 JavaScript는 HTML 한 파일에 있으며, Supabase 라이브러리는 고정 버전 CDN으로 불러옵니다.

이메일·비밀번호로 가입하면 자동 로그인됩니다. 기존 가입자는 로그인 버튼을 사용합니다. 비밀번호를 잊었다면 이메일을 입력하고 비밀번호 재설정을 누른 뒤, 이메일의 링크에서 새 비밀번호를 입력합니다.

Supabase 프로젝트 `ttfgbupxowhpwcqruesy`에서 Confirm email 해제와 `mailer_autoconfirm=true`를 확인했습니다. 재설정 복귀 주소는 배포 앱의 `?recover=1`로 제한했습니다. 프런트엔드에는 공개용 publishable 키만 사용합니다.

## 검증 결과
- 실제 GitHub Pages 첫 화면 접속 및 JavaScript 문법 검사: 통과.
- DB RLS: 본인 메모 조회·추가·삭제 및 타인 조회·추가·삭제 차단 통과. 테스트 데이터는 롤백했습니다.
- 보안 Advisor: 지적 사항 없음.
- 비밀번호 재설정: 코드 문법 및 복귀 주소 설정 확인. 이메일 수신·비밀번호 변경은 사용자 진행 대기.
- 가입 직후 자동 로그인, 메모 저장·목록·삭제, 새로고침 후 유지, 로그아웃·재로그인: 실제 사이트 검증 미완료. 기존 계정 로그인에 실패하여 비밀번호 재설정 후 진행 예정.
