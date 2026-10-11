# Film-ing 개인정보 안내

Film-ing 은 **내 PC 안에서만 동작하는 프로그램**입니다. 이 문서는 Film-ing 이 인터넷으로 무엇을 보내는지, 보내지 않는지를 빠짐없이 적은 것입니다.

> **English summary:** Film-ing never uploads your photos or your library records. It only goes online for three things:
> (1) an optional daily update check against GitHub (sends nothing but a normal web request with "Film-ing/<version>"), and
> (2) feedback you choose to send (your message, optional reply email, and — if you leave it on — app/Windows version,
> screen size and photo/roll counts), and (3) "Show on map", which opens OpenStreetMap in your browser with that
> photo's coordinates — only when you click it. No accounts, ads, analytics or tracking.

## 한눈에

| | 보내는 곳 | 언제 | 무엇을 |
|---|---|---|---|
| 사진·정리 기록 | **어디로도 보내지 않음** | — | — |
| 업데이트 확인 | GitHub (`api.github.com`, `github.com`) | “알림 받기”를 골랐을 때 하루 한 번, 또는 “지금 확인”을 누를 때 | 일반 인터넷 요청뿐 (프로그램 이름·버전) |
| 업데이트 받기 | GitHub | 새 버전을 “받기”로 직접 고를 때 | 일반 인터넷 요청뿐 |
| 의견 보내기 | 개발자의 구글 앱스 스크립트 → 개발자 메일 | 직접 “보내기”를 누를 때 | 적은 내용 + 고른 항목 (아래) |
| 지도에서 보기 | OpenStreetMap (기본 브라우저로 열림) | 사진 정보 패널의 “지도에서 보기”를 직접 누를 때 | 그 사진의 위치 좌표 (지도 주소에 들어감) |

계정·로그인·광고·사용 통계·위치 추적이 없습니다. 인터넷이 없어도 모든 기능을 쓸 수 있습니다.

## 사진과 정리 기록

- 사진 파일은 원래 있던 폴더에 그대로 있고, **어디로도 올리거나 보내지 않습니다.**
- 롤·별점·보정값·미리보기·백업·기록(로그) 같은 정리 기록은 내 PC 의 `%LOCALAPPDATA%\Film-ing` 에 있습니다
  (**설정 → 정리 기록 위치…** 에서 다른 폴더로 옮겼다면 그 폴더). 이 기록도 밖으로 보내지 않습니다.
- 되돌리기 기록(`Ctrl+Z`), 다시 켤 때 보던 곳으로 돌아가기 위한 화면 상태, 내 내보내기 프리셋도 모두 내 PC 안(프로그램 창의 저장소와 정리 기록)에만 둡니다.
- 사진 파일에 촬영 정보를 적는 기능은 내 PC 의 파일에만 적용됩니다. 위치(GPS)도 파일에 적을 수 있는데, 내보낼 때
  **위치 정보(GPS 좌표) 빼기**를 켜면 내보낸 파일에서 위치를 지웁니다(인스타그램·필름 프레임·웹 용도는 기본으로 켜짐).

## 업데이트 확인 때 GitHub 로 가는 것

처음 켤 때 “업데이트 알림”(새 버전이 나오면 알려 드릴까요?)을 받을지 묻습니다. “나중에”를 고르면 **설정 → 업데이트…** 의 “지금 확인”을 누를 때만 확인합니다.

- 받는 것: 배포 저장소의 최신 릴리스 정보, 그 릴리스의 `manifest.json`(새 버전 정보)과 `manifest.json.sig`(공식 서명). 새 버전을 “받기”로 고르면 업데이트 파일(zip).
- 보내는 것: 위 파일을 달라는 **일반 인터넷 요청**뿐입니다. 요청 머리글에 `Film-ing/<버전>` 이 들어갑니다.
  사진, 정리 기록, 파일 위치, 사용자 이름, 기기 번호는 보내지 않습니다.
- 인터넷 요청의 성격상 GitHub 는 요청한 **IP 주소와 시각**을 알 수 있습니다. GitHub 가 이를 어떻게 다루는지는
  [GitHub 개인정보 처리방침](https://docs.github.com/site-policy/privacy-policies/github-general-privacy-statement)을 따릅니다.
- 확인한 시각과 동의 여부는 정리 기록 폴더의 `update.json` 에만 적습니다.

## 의견 보내기로 가는 것

도움말(`?`)이나 설정 창의 **의견 보내기…** 에서 직접 “보내기”를 누를 때만 보냅니다. **보낼 내용 보기**로 나갈 내용을 미리 그대로 볼 수 있습니다.

| 항목 | 기본 | 내용 |
|---|---|---|
| 종류 · 내용 | 늘 | 문제 신고 / 기능 제안 / 기타, 직접 쓴 글(5~4000자) |
| 답장 받을 메일 | 선택 (비워 둠) | 적으면 그 주소로 답장합니다 |
| 환경 정보 | 켜짐 (끌 수 있음) | 앱 버전, 윈도우 버전, 화면 크기, 사진 수, 롤 수 — **숫자만**. 파일 위치·사진 이름·정리 기록 내용은 넣지 않음 |
| 최근 오류 기록 | 꺼짐 | `logs/app.log` 의 오류 부분만. 사용자 이름·폴더 경로·파일 이름·메일 주소를 가린 뒤 화면에 그대로 보여 주고, **이대로 보내기**를 눌러야만 보냄 |
| 그 밖에 | 늘 | 앱 버전, 자동 입력(스팸) 판단용 값(창을 연 뒤 보내기까지 걸린 초, 사람에게는 보이지 않는 빈 칸), 보내는 쪽별 하루 한도를 세는 **임의 번호**(무작위로 만든 값 — 사람이나 컴퓨터를 알아볼 수 없음) |

- 받는 곳: 개발자가 만든 구글 앱스 스크립트 웹앱이 받아 개발자 메일로 전달합니다. 이 과정에서 구글 서버를 거치므로 구글은 요청한 **IP 주소와 시각**을 알 수 있습니다.
- 받은 의견은 프로그램을 고치고 답장하는 데만 씁니다. 지워 달라고 메일(filmingapp.official@gmail.com)로 알려 주시면 지웁니다.
- 인터넷이 끊겼거나 보내지 못하면 내 PC 의 정리 기록 폴더 `outbox` 에 보관했다가 다시 보냅니다(최대 14일·12번). 보관함은 의견 창에서 지울 수 있습니다.
- 하루 10건까지, 같은 내용은 하루 안에 다시 보내지 않습니다.

## 프로그램 창(Microsoft Edge)

Film-ing 의 화면은 내 PC 안의 작은 서버(`127.0.0.1`, 바깥에서는 접속할 수 없음)를 Microsoft Edge 의 앱 창으로 여는 방식입니다.
이 창은 Film-ing 전용 설정 폴더를 쓰고, 계정 로그인·동기화·번역을 끈 채로 엽니다. 다만 Edge 프로그램 자체의 업데이트·보안 기능 같은
통신은 Microsoft 의 Edge 설정과 [Microsoft 개인정보처리방침](https://privacy.microsoft.com/)을 따릅니다. Film-ing 이 Edge 를 통해 사진이나 정리 기록을 보내는 일은 없습니다.

## 프로그램을 지울 때

제거하면 프로그램 파일은 지우고, 사진 파일은 건드리지 않습니다. 정리 기록은 기본으로 남기고 지울지 한 번 묻습니다.
나중에 직접 지우려면 `%LOCALAPPDATA%\Film-ing` 폴더를 지우면 됩니다.

## 문의

filmingapp.official@gmail.com
