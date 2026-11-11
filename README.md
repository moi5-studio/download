# moi5 Studio

**내 PC 안에서 돌아가는 로컬 AI 스튜디오**입니다. AI 모델을 내 컴퓨터에 내려받아
대화하고, 내 문서를 넣어 그 문서를 근거로 답을 받습니다. 대화와 문서는 기본적으로
이 PC 밖으로 나가지 않습니다.

> 이 저장소는 **설치 파일과 안내 문서만** 올리는 배포용입니다. 소스 코드는 공개하지 않습니다.

## 내려받기

| 항목 | 내용 |
|---|---|
| 최신 버전 | **34.3** |
| 설치 파일 | [`moi5Studio_Setup_v34.3.exe`](https://github.com/moi5-studio/download/releases/download/v34.3/moi5Studio_Setup_v34.3.exe) (926 MB) |
| 대상 | Windows 10 / 11 (64비트) |
| 사용 조건 | 무료 · 개인/업무 사용 가능 ([이용약관](LICENSE.md)) |

내려받은 뒤 **받은 파일이 진짜인지** 꼭 확인해 주십시오. 이 설치 파일에는 코드 서명이 없습니다.

### 받은 파일 확인 (SHA-256)

공식 값:

```
4798007815d44356c02a0d1c2c8726aef93d5ea813703cb859d0ded6fdafcba7
```

PowerShell 에서 아래 명령을 실행해 나온 `Hash` 가 위 값과 **한 글자도 다르지 않아야** 합니다.

```powershell
Get-FileHash "$env:USERPROFILE\Downloads\moi5Studio_Setup_v34.3.exe" -Algorithm SHA256
```

값이 다르면 설치하지 말고 파일을 지운 뒤, 이 페이지에서 다시 받으십시오.

### 설치할 때 Windows 경고가 뜨면

「Windows의 PC 보호」 창이 뜨면 **[추가 정보] → [실행]** 을 누르십시오. 코드 서명이 없어서
게시자가 「알 수 없는 게시자」로 나오는 것이며, 위 SHA-256 이 같다면 정상 파일입니다.
자세한 안내는 [INSTALL.md](INSTALL.md) 를 보십시오.

## 문서

- [설치 안내](INSTALL.md)
- [자주 묻는 질문](FAQ.md)
- [개인정보처리방침](PRIVACY.md)
- [이용약관](LICENSE.md)
- [오픈소스 라이선스 고지](THIRD-PARTY-NOTICES.md) · 원문은 [licenses](licenses/) 폴더

## 문의 · 버그 신고

https://moi5.com/contact.html

---

공식 배포처는 이 저장소의 Releases 와 moi5.com 입니다. 다른 곳에서 받은 설치 파일은 쓰지 마십시오.
