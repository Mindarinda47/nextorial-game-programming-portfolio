# 2026 넥슨 넥토리얼 Game Programming 포트폴리오

게임 네트워크, Unity 게임플레이 시스템, C 시스템 프로그래밍 경험을 빠르게 확인할 수 있도록 구성한 포트폴리오 허브입니다. 각 저장소는 구현 코드, 담당 범위, 문제 해결 과정과 검증 근거를 중심으로 정리했습니다.

## 우선 검토 프로젝트

<table>
<tr>
<td width="50%" valign="top">
<h3>1. VR 재난 시뮬레이션</h3>
<p>PC 관제자와 VR 참가자를 연결하는 3인 팀 프로젝트입니다. 멀티플레이 연결·설정, 플레이어 생성과 소유권 이전, 위치 동기화, 관제 상호작용과 음성 기능 연동을 담당했습니다.</p>
<p><strong>Unity · C# · Netcode for GameObjects · XR · Vivox</strong></p>
<p><a href="https://github.com/Mindarinda47/vr-disaster-networking-portfolio"><strong>저장소 바로 보기 →</strong></a></p>
<p><a href="https://www.youtube.com/watch?v=iOX_i1il5Sw">시연 영상</a> · <a href="https://github.com/Mindarinda47/vr-disaster-networking-portfolio/blob/main/docs/contribution.md">담당 범위</a> · <a href="https://github.com/Mindarinda47/vr-disaster-networking-portfolio/tree/main/src/networking">대표 코드</a></p>
</td>
<td width="50%" valign="top">
<h3>2. Unity 2D RPG Gameplay Systems</h3>
<p>탐색, 전투, NPC 대화, 퀘스트, 인벤토리와 저장 기능을 하나의 플레이 흐름으로 연결한 개인 프로젝트입니다. 상태 전이와 시스템 간 데이터·UI 동기화에 중점을 두었습니다.</p>
<p><strong>Unity 6 · C# · ScriptableObject · JSON · 2D Physics</strong></p>
<p><a href="https://github.com/Mindarinda47/unity-2d-rpg-gameplay-systems"><strong>저장소 바로 보기 →</strong></a></p>
<p><a href="https://github.com/Mindarinda47/unity-2d-rpg-gameplay-systems/blob/main/Docs/ARCHITECTURE.md">설계</a> · <a href="https://github.com/Mindarinda47/unity-2d-rpg-gameplay-systems/blob/main/Docs/PROBLEM_SOLVING.md">문제 해결</a> · <a href="https://github.com/Mindarinda47/unity-2d-rpg-gameplay-systems/tree/main/Assets/Scripts">대표 코드</a></p>
</td>
</tr>
</table>

## 5분 검토 경로

1. **VR 재난 시뮬레이션**의 시연 영상으로 프로젝트 전체 흐름을 확인합니다.
2. VR 저장소의 `NetworkConnect`, `NetworkPlayer`, `minimapClickHandler`에서 담당 네트워크 구현을 확인합니다.
3. **Unity 2D RPG**의 `QuestManager`, `PlayerInventory`, `SaveManager`에서 게임플레이 시스템 연결을 확인합니다.
4. 관심 분야에 따라 웹 게임 또는 [전공 기술 사례](docs/TECHNICAL_CASES.md)를 추가로 확인합니다.

## 프로젝트 지도

| 우선순위 | 프로젝트 | 형태·역할 | 핵심 역량 | 바로 보기 |
|---:|---|---|---|---|
| 1 | VR 재난 시뮬레이션 | 3인 팀 · 네트워크 담당 | Unity 멀티플레이, 소유권·동기화, 비동기 생성 순서, 협업 | [Repository](https://github.com/Mindarinda47/vr-disaster-networking-portfolio) |
| 2 | Unity 2D RPG Gameplay Systems | 개인 프로젝트 · 게임플레이 구현 | 퀘스트, 대화, 인벤토리, 전투, 저장, 이벤트 기반 UI | [Repository](https://github.com/Mindarinda47/unity-2d-rpg-gameplay-systems) |
| 3 | 웹 방탈출 게임 | 1인 프로젝트 · 전체 구현 | 퍼즐 상태 관리, 게임 밸런스, 반복 플레이 검증 | [Repository](https://github.com/Mindarinda47/website-escape-game-portfolio) |
| 4 | 붐비 혼잡 예보 | 1인 프로젝트 · 전체 구현 | 요구사항 구조화, 혼잡도 규칙, 데이터와 서비스 설계 | [Repository](https://github.com/Mindarinda47/boombi-ai-crowd-forecast) |
| 기술 사례 | C 다중 클라이언트 채팅 | 개인 재구현 | TCP framing, `select`, 연결·방 상태, 통합 테스트 | [Repository](https://github.com/Mindarinda47/c-network-room-chat) |
| 기술 사례 | xv6 Kernel Extensions | 학부 과제·재검증 | 시스템 콜, 우선순위 스케줄링, lazy allocation | [Repository](https://github.com/Mindarinda47/xv6-kernel-extensions) |
| 기술 사례 | STM32 Halli Galli | 4인 팀 · 센서·통합 기여 | 임베디드 통합, 하드웨어 디버깅, 협업 | [Repository](https://github.com/Mindarinda47/stm32-halli-galli-system) |

전공 사례의 구현 범위와 증거 수준은 [Technical Cases](docs/TECHNICAL_CASES.md)에 비교 정리했습니다.

## 역량 요약

### Unity 게임플레이 프로그래밍

- 퀘스트 상태 전이와 NPC 대화 분기 연결
- 수량 기반 인벤토리와 ID 기반 저장·복원
- 플레이어·적 전투, 피격, 넉백과 사망 상태 처리
- 상태 변경 이벤트를 이용한 UI 동기화

### 게임 네트워크

- Host/Client 연결과 서버 주도 NetworkObject 생성
- 플레이어 소유권 이전과 Client-authoritative Transform 적용
- RPC 기반 관제 상호작용과 비동기 생성 순서 처리
- PC와 VR 역할에 따른 UI·카메라·입력 분리

### 시스템 기반

- C 소켓의 stream framing과 다중 클라이언트 상태 관리
- xv6 시스템 콜, 스케줄러와 가상 메모리 경로 분석
- STM32 센서·LCD·Bluetooth·게임 상태 통합 경험

## 공개 및 기여 기준

- 팀 프로젝트는 확인 가능한 담당 범위만 설명합니다.
- 실행 결과, 코드, 테스트 또는 당시 기록으로 확인 가능한 내용만 주장합니다.
- 학부 당시 결과와 이후 재구현·보강 사항을 구분합니다.
- 교수 제공 자료, 과제 명세 원문, 팀원 코드와 개인정보는 공개하지 않습니다.
- 권리를 확인하지 않은 외부 아트·폰트 리소스는 코드 포트폴리오에서 제외합니다.
