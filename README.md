# QR BOX — 여기 있어 QR코드

링크·텍스트·이미지·파일을 QR코드로 만들고, 카메라나 이미지로 QR코드를 인식하는 올인원 웹 앱입니다.  
별도 설치 없이 브라우저에서 바로 사용할 수 있습니다.

---

## 주요 기능

### QR 생성
| 타입 | 설명 |
|------|------|
| 링크 | URL을 입력해 QR코드 생성 |
| 텍스트 | 자유 텍스트를 QR코드로 변환 |
| 이미지 | 이미지를 클라우드에 업로드 후 링크형 QR 생성 |
| 파일 | 최대 20MB 파일을 [file.io](https://www.file.io)에 업로드해 다운로드 링크 QR 생성 |

- 생성된 QR코드 **클립보드 복사** 및 **PNG 다운로드** 지원

### QR 인식
- **카메라 스캔** — 후면 카메라로 실시간 인식
- **이미지 업로드** — 갤러리·파일에서 QR 이미지를 불러와 인식
- **클립보드 붙여넣기** — 복사한 이미지를 바로 분석 (Ctrl+V / Cmd+V)
- URL이 담긴 QR코드는 바로 열기 버튼 제공

---

## 사용 방법

정적 HTML 파일 하나로 구성되어 있습니다. 별도 빌드나 서버 설치 없이 사용할 수 있습니다.

```bash
# 저장소 클론
git clone https://github.com/chichiboo123/qrbox.git
cd qrbox

# index.html을 브라우저로 바로 열거나
open index.html

# 간단한 로컬 서버로 실행 (카메라 기능은 HTTPS 또는 localhost 필요)
python3 -m http.server 8080
```

---

## 기술 스택

- **HTML / Vanilla JS** — 프레임워크 없이 단일 파일로 구성
- **Tailwind CSS** (CDN) — 유틸리티 기반 스타일링
- **Pretendard GOV** — 본문 폰트
- **Google Material Icons** — 아이콘

---

## 참고한 오픈소스

이 프로젝트는 훌륭한 오픈소스 라이브러리들 덕분에 만들어질 수 있었습니다. 감사합니다.

| 라이브러리 | 역할 | 라이선스 |
|-----------|------|---------|
| [jsQR](https://github.com/cozmo/jsQR) | QR코드 디코딩 (주 엔진) | Apache 2.0 |
| [ZXing Browser](https://github.com/zxing-js/browser) | QR코드 디코딩 (폴백 엔진) | MIT |
| [goQR.me API](https://goqr.me/api/) | QR코드 이미지 생성 | 무료 공개 API |
| [file.io](https://www.file.io) | 파일 임시 업로드 | 무료 공개 API |
| [Tailwind CSS](https://github.com/tailwindlabs/tailwindcss) | UI 스타일링 | MIT |
| [Pretendard](https://github.com/orioncactus/pretendard) | 한국어 폰트 | OFL-1.1 |

> jsQR과 ZXing 두 엔진을 조합하고, 고대비 변환·이진화·업스케일 등 전처리를 추가해  
> 다양한 환경에서도 QR코드 인식률을 높였습니다.

---

## 제작

**교육뮤지컬 꿈꾸는 치수쌤**  
🔗 [litt.ly/chichiboo](https://litt.ly/chichiboo)

---

## 라이선스

MIT License
