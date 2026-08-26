# 2026 넥슨 넥토리얼 Game Programming 포트폴리오

게임 네트워크, 게임플레이 시스템 설계와 시스템 프로그래밍 경험을 한곳에서 확인할 수
있도록 정리한 포트폴리오 허브입니다. 팀 프로젝트는 직접 담당한 범위만, 재구현 사례는
당시 결과와 2026년 결과를 구분해 설명합니다.

> **현재 단계:** 비공개 제출 검토본입니다. 완성도와 실행 증거가 확인된 항목부터
> 공개하고, 준비 중인 항목은 제출 링크에서 제외합니다.

## 처음 방문했다면

현재 권장 확인 순서는 다음과 같습니다.

1. [**VR 재난 시뮬레이션**](https://github.com/Mindarinda47/vr-disaster-networking-portfolio) — Unity 멀티플레이에서 직접 담당한 네트워크 구현과 팀 협업
2. [**웹 방탈출 게임**](https://github.com/Mindarinda47/website-escape-game-portfolio) — 짧은 일정 안에 완성한 1인 게임의 상태 관리와 검증
3. [**C 다중 클라이언트 채팅**](https://github.com/Mindarinda47/c-network-room-chat) — TCP stream 경계 문제를 재현하고 독립 테스트로 해결한 사례

First_game은 추가 개발과 검증이 끝난 뒤 위 순서에 포함합니다. 전체 전공 사례의 역할과
검증 수준은 [전공 기술 사례 안내](docs/TECHNICAL_CASES.md)에서 비교할 수 있습니다.

## 프로젝트 구성

| 구분 | 프로젝트 | 증명하는 역량 | 상태 |
|---|---|---|---|
| 핵심 | VR 재난 시뮬레이션 | Unity 멀티플레이, 동기화, 팀 협업 | 선별본 완료 |
| 핵심 | 웹 방탈출 게임 | 게임 로직, 상태 관리, 테스트, AI 활용 | 선별본 완료 |
| 핵심 | First_game | 퀘스트, 대화, 인벤토리 | 추가 개발 후 반영 |
| 보조 | 붐비 AI 혼잡 예보 | AI 구조화, 규칙 엔진, 데이터와 제품 설계 | 선별본 완료 |
| 기술 기반 | C 다중 클라이언트 채팅 | TCP, `select`, framing, 독립 테스트 | 검증 완료 |
| 기술 기반 | xv6 Kernel Extensions | 시스템 콜, 스케줄러, lazy allocation | 당시 실행 기록 포함 |
| 기술 기반 | STM32 Halli Galli | 하드웨어 통합, 디버깅, 협업 | 협업 사례 정리 완료 |

## 핵심 역량

### 게임 네트워크

Unity Netcode를 이용한 Host/Client 연결, NetworkObject 생성, RPC, 플레이어 생성과 Transform 동기화 경험이 있습니다.

### 게임플레이 시스템

퀘스트·대화·인벤토리 시스템과 Canvas 기반 전투·퍼즐·저장 시스템을 구현했습니다.

### AI를 활용한 개발

AI에 요구사항과 제약을 제공하고, 생성 결과를 실행·테스트·코드 검토로 검증하는 방식으로 사용했습니다.

## 저장소

- [VR 재난 시뮬레이션 — 네트워크 담당 선별본](https://github.com/Mindarinda47/vr-disaster-networking-portfolio)
- [웹 방탈출 게임 — 1인 게임 개발 선별본](https://github.com/Mindarinda47/website-escape-game-portfolio)
- [붐비 — AI 혼잡 예보 선별본](https://github.com/Mindarinda47/boombi-ai-crowd-forecast)
- [C 다중 클라이언트 채팅 — 전공 기술 사례](https://github.com/Mindarinda47/c-network-room-chat)
- [xv6 Kernel Extensions — 전공 기술 사례](https://github.com/Mindarinda47/xv6-kernel-extensions)
- [STM32 Halli Galli — 협업·통합 사례](https://github.com/Mindarinda47/stm32-halli-galli-system)

## 증거 기준

| 표시 | 의미 |
|---|---|
| 검증 완료 | 소스, 설명과 재현 가능한 독립 테스트를 확인할 수 있음 |
| 당시 실행 기록 포함 | 보존된 실행 결과와 현재 구현 코드를 함께 확인할 수 있음 |
| 협업 사례 정리 완료 | 팀 결과와 확인된 개인 기여를 구분해 설명함 |
| 추가 개발 후 반영 | 현재 상태로는 대표 프로젝트로 제출하지 않음 |

## 작성 원칙

- 팀 프로젝트는 직접 담당한 부분만 명시합니다.
- AI가 보조한 부분과 직접 판단·구현한 부분을 구분합니다.
- 실제 개발 기간과 포트폴리오 정리 기간을 구분합니다.
- 실행·코드·테스트·영상으로 확인할 수 있는 내용만 주장합니다.
- 강의 자료, 과제 명세, 팀원 코드와 개인정보는 공개 저장소에 포함하지 않습니다.
- 2026년 재구현·수정 사항은 당시 제출 결과와 분리해 표시합니다.
