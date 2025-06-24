# linux-script
리눅스 명령어 정리

# 리눅스 명령어 조사 (top, ps, jobs, kill)

**과제 제출일:** 2025년 6월 25일

이 문서는 리눅스의 프로세스 관리 및 작업 제어와 관련된 주요 명령어인 `top`, `ps`, `jobs`, `kill`에 대해 조사하고 정리한 내용입니다.

---

## 1. top 명령어

`top` 명령어는 시스템의 현재 실행 중인 프로세스와 리소스 사용량(CPU, 메모리 등)을 실시간으로 보여주는 도구입니다.

### 주요 기능 및 특징
* 실시간 시스템 모니터링
* 프로세스별 CPU, 메모리 사용량 확인
* 정렬, 필터링 등 다양한 상호작용 기능 제공

### 주요 출력 내용
* **프로세스 정보:** PID, USER, PR, NI, VIRT, RES, SHR, S, %CPU, %MEM, TIME+, COMMAND 등
* **시스템 요약:** Load Average, Task Summary, CPU Stats, Memory Stats, Swap Stats

### 주요 옵션
* `-d [초]`: 업데이트 간격 설정 (예: `top -d 1`)
* `-p [PID]`: 특정 PID만 모니터링 (예: `top -p 1234`)
* `-u [USER]`: 특정 사용자 프로세스만 모니터링 (예: `top -u root`)

### 사용 예시

```bash
# 기본 top 명령어 실행
top

# 3초 간격으로 업데이트
top -d 3

# 특정 PID (예: 1234)만 모니터링
top -p 1234
