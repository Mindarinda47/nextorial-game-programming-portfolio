# 전공 기술 사례

게임 프로그래밍 프로젝트를 보완하는 운영체제, 네트워크와 임베디드 기술 사례입니다.
세 사례는 증명하는 역량과 남아 있는 증거가 다르므로 같은 완성도로 주장하지 않습니다.

## 권장 확인 순서

| 순서 | 사례 | 먼저 볼 내용 | 증명하는 역량 | 제출 상태 |
|---|---|---|---|---|
| 1 | C 다중 클라이언트 채팅 | TCP stream framing 문제와 독립 테스트 | C, socket, `select`, 상태 관리, 테스트 | 검증 완료 |
| 2 | xv6 Kernel Extensions | nice 스케줄러와 lazy page allocation | 커널 경로, 프로세스 상태, 가상 메모리 | 당시 실행 기록 포함 |
| 3 | STM32 Halli Galli | 제약에 따른 범위 조정과 통합 디버깅 | 임베디드 통합, 하드웨어 설계, 협업 | 협업 사례 정리 완료 |

## 01. C 다중 클라이언트 채팅

2023년 과제 경험을 바탕으로 2026년에 로비·채팅방 서버를 독립 구조로 다시 구현했습니다.
TCP가 응용 메시지 경계를 보존하지 않는 문제를 누적 버퍼와 newline framing으로 처리하고,
partial send, 방 격리, 연결 종료를 독립 테스트로 검증했습니다.

- **가장 먼저 볼 것:** README의 `문제 발견과 보완`, 독립 테스트 구성
- **코드 진입점:** protocol, server, integration test
- **현재 증거:** warning-free build, protocol test와 3-client integration test 통과
- **한계:** blocking slow client에 대한 output queue는 후속 확장 항목
- [상세 저장소 열기](https://github.com/Mindarinda47/c-network-room-chat)

## 02. xv6 Kernel Extensions

xv6-public을 기반으로 시스템 콜, nice 우선순위 스케줄러와 lazy page allocation을
구현한 학부 운영체제 사례입니다. 2026년에는 과제 명세와 코드를 다시 대조해 타이머
인터럽트 경로의 비선점 정책 불일치를 수정하고 독립 테스트를 구성했습니다.

- **가장 먼저 볼 것:** 15초 요약, 스케줄러 정책, lazy allocation 흐름
- **코드 진입점:** `proc.c`, `sysproc.c`, `trap.c`, `vm.c`, `portfolio_*_test.c`
- **현재 근거:** 과제 1·2 당시 실행 기록, 구현 코드와 독립 테스트 코드 5개
- **공개 경계:** MIT 기반 코드와 개인 변경 범위를 README·LICENSE·UPSTREAM에 명시

- [상세 저장소 열기](https://github.com/Mindarinda47/xv6-kernel-extensions)

## 03. STM32 Halli Galli

4인 팀이 STM32로 1인 대 컴퓨터 할리갈리 게임을 완성한 협업·통합 사례입니다. 포트와
안정성 제약에 따라 초기 범위를 조정하고, LCD·센서·Bluetooth·게임 상태를 통합하는
과정에서 인터페이스 설계, 하드웨어 배치, 디버깅과 반복 테스트를 담당했습니다.

- **가장 먼저 볼 것:** 개인 기여, 대표 문제해결, 협업 과정
- **현재 근거:** 당시 결과 문서, 역할 기록과 대표 센서 코드 2개
- **표현 기준:** 팀의 완성 결과와 개인 기여를 분리하고, 부분 코드를 전체 구현으로 주장하지 않음

- [상세 저장소 열기](https://github.com/Mindarinda47/stm32-halli-galli-system)

## 심사위원용 읽기 기준

- 각 저장소 첫 화면에서 **무엇을 만들었는지, 본인 기여, 해결한 문제, 검증 결과와 한계**를
  순서대로 확인할 수 있도록 구성합니다.
- 상세 회고보다 실행 가능한 코드와 증거를 먼저 연결합니다.
- 당시 과제와 2026년 재구현·보강을 날짜와 디렉터리로 구분합니다.
- 교수 제공 자료, 과제 명세 원문, 팀원 코드, 개인정보와 권리를 확인하지 않은 이미지는
  공개하지 않습니다.
