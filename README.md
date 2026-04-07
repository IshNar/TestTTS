# 孫子兵法 The Art of War — 영한 병렬 학습 + AI 음성

손자병법 13편 전문을 영어-한국어 병렬로 읽으며, AI 음성(Kokoro TTS)으로 듣고, 어휘를 학습할 수 있는 웹 애플리케이션입니다.

## 주요 기능

- **영한 병렬 텍스트**: 손자병법 13편 전문, 영어 원문(Lionel Giles 번역)과 한국어 번역 동시 표시
- **AI 음성 재생**: Kokoro AI TTS 기반 17개 음성(미국/영국 남녀) 지원, 즉시 재생
- **속도 조절**: 0.6x ~ 1.2x 재생 속도 선택
- **반복 재생**: 구절별 반복 듣기 기능
- **단어 학습**: 밑줄 친 영어 어휘 터치 시 한국어 뜻 팝업
- **한국어 표시 토글**: 한국어 번역 표시/숨기기

## 데모

[https://ishnar.github.io/TestTTS/](https://ishnar.github.io/TestTTS/)

## 프로젝트 구조

```
TestTTS/
├── index.html              # 메인 학습 페이지
├── generate_audio.html     # TTS 음성 일괄 생성기 (관리용)
├── convert_mp3.html        # WAV → MP3 변환기 (관리용)
├── audio/                  # 미리 생성된 MP3 음성 파일 (1,105개)
│   ├── af_heart/           # Heart (미국 여성)
│   ├── af_sky/             # Sky (미국 여성)
│   ├── af_bella/           # Bella (미국 여성)
│   ├── af_nicole/          # Nicole (미국 여성)
│   ├── af_sarah/           # Sarah (미국 여성)
│   ├── af_nova/            # Nova (미국 여성)
│   ├── af_alloy/           # Alloy (미국 여성)
│   ├── af_jessica/         # Jessica (미국 여성)
│   ├── af_river/           # River (미국 여성)
│   ├── af_aoede/           # Aoede (미국 여성)
│   ├── af_kore/            # Kore (미국 여성)
│   ├── am_adam/            # Adam (미국 남성)
│   ├── am_michael/         # Michael (미국 남성)
│   ├── bf_emma/            # Emma (영국 여성)
│   ├── bf_isabella/        # Isabella (영국 여성)
│   ├── bm_george/          # George (영국 남성)
│   └── bm_lewis/           # Lewis (영국 남성)
└── README.md
```

## 기술 스택

- **프론트엔드**: HTML, CSS, JavaScript (프레임워크 없음, 단일 파일)
- **TTS 엔진**: [Kokoro TTS](https://tts.rocks/) (WebAssembly 기반, 브라우저 내 로컬 실행)
- **음성 파일**: MP3 128kbps, 17개 음성 × 65개 구절 = 1,105개 파일
- **호스팅**: GitHub Pages

## 완성 현황

| 항목 | 상태 |
|---|---|
| 손자병법 13편 전문 텍스트 (영/한) | ✅ 완료 |
| 17개 AI 음성 MP3 파일 생성 | ✅ 완료 (1,105개) |
| MP3 파일 즉시 재생 | ✅ 완료 |
| 실시간 Kokoro TTS 폴백 | ✅ 완료 (MP3 없을 시) |
| 속도 조절 (playbackRate) | ✅ 완료 |
| 반복 재생 | ✅ 완료 |
| 어휘 팝업 (터치/클릭) | ✅ 완료 |
| 한국어 표시/숨기기 | ✅ 완료 |
| 기기 내장 음성 (Web Speech API) | ✅ 완료 |
| 모바일 반응형 UI | ✅ 완료 |
| TTS 음성 일괄 생성기 | ✅ 완료 |
| WAV → MP3 변환기 | ✅ 완료 |

## 사용법

1. [데모 페이지](https://ishnar.github.io/TestTTS/)에 접속
2. 상단에서 음성과 속도를 선택
3. **▶ Listen** 버튼으로 AI 음성 재생
4. **🔁 Repeat** 버튼으로 반복 듣기
5. **밑줄 친 단어**를 터치하면 한국어 뜻 표시

## 권장 환경

- **Google Chrome** 권장 (실시간 TTS 폴백 시)
- MP3 재생은 모든 브라우저에서 정상 동작
- 카카오톡 인앱 브라우저에서는 외부 브라우저로 열기 권장

## 라이선스

- 영문 텍스트: Lionel Giles (1910, Public Domain)
- 한국어 번역: Claude AI
- 음성: Kokoro AI TTS
