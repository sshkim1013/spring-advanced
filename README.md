# SPRING ADVANCED

내일배움캠프 Spring_5기 트랙의 [ 스프링 입문 주차 - 일정 관리 앱 Develop ] 과제에 대한 README.md 문서입니다.

-----

## 레벨 별 수정 사항

### Lv 1. 코드 개선

**1-1) 코드 개선 퀴즈 - Early Return**

<img width="800" alt="스크린샷 2025-02-27 오전 11 19 10" src="https://github.com/user-attachments/assets/93caa095-0c98-4241-897c-e9cd0104a15d" />

- 코드를 최상단으로 옮겨 `passwordEncoder`의 `encode()` 동작이 불필요하게 일어나지 않게 리팩토링.

<br>

**1-2) 리팩토링 퀴즈 - 불필요한 if-else 피하기**

<img width="800" alt="스크린샷 2025-02-27 오전 11 19 10" src="https://github.com/user-attachments/assets/45ecc2b6-8572-4839-b961-e54e22dd5747" />

- if문을 분리하여 순서 재배치.

<br>

**1-3) 코드 개선 퀴즈 - Validation**

<img width="631" alt="스크린샷 2025-02-27 오전 11 22 25" src="https://github.com/user-attachments/assets/087480f4-b723-4d50-b47a-0742e9e811cc" />

- 기존의 검증 코드 제거.

<img width="473" alt="스크린샷 2025-02-27 오전 11 22 52" src="https://github.com/user-attachments/assets/639cc508-a7d3-4e5d-97e9-47a2baa5ef60" />

- 관련된 dto에서 Validation 어노테이션을 통해 검증할 수 있도록 수정.

---

### Lv 2. N+1 문제

<img width="603" alt="스크린샷 2025-02-27 오전 11 25 40" src="https://github.com/user-attachments/assets/89afb05c-084d-4e66-905d-671768bad4a3" />

- `@EntityGraph` 어노테이션을 사용하여 기존의 쿼리(`fetch join` 사용)와 동일한 동작을 하는 코드로 리팩토링.
- 하단의 코드는 `findById()` 로 메서드 명을 수정해면 `@EntityGraph`를 적용 가능하지만, 요구사항만 충족시키기 위해서 건드리지 않았습니다.

---

### Lv 3. 테스트 코드 연습

**1번 케이스**

<img width="509" alt="스크린샷 2025-02-27 오전 11 29 45" src="https://github.com/user-attachments/assets/2d4ab705-0099-4cab-be13-b1759fdb04c6" />

<img width="437" alt="스크린샷 2025-02-27 오전 11 29 58" src="https://github.com/user-attachments/assets/ea2c98b0-fe89-4997-902f-47c826c014cb" />

- 두 인자의 위치를 수정하면 테스트 성공.

<br>

**2번 케이스**

<img width="743" alt="스크린샷 2025-02-27 오전 11 35 37" src="https://github.com/user-attachments/assets/aba11671-8c52-4196-85cf-f6107891c20c" />

<img width="602" alt="스크린샷 2025-02-27 오전 11 35 48" src="https://github.com/user-attachments/assets/de4444d7-9413-491b-aa58-be84cb35f105" />

- `ServerException`이 아닌 `InvalidRequestException`으로 수정

<br>

**3번 케이스**

<img width="758" alt="스크린샷 2025-02-27 오전 11 39 33" src="https://github.com/user-attachments/assets/ef388ad9-e835-4428-8431-55930b51437d" />

- ManagerService 클래스에 `todo.getUser()`가 `null`인지 검증하는 로직을 추가.

<br>
<br>

---

# 💻 리팩토링 기간

Level 1 - 2025.02.24 ~ 2025.02.24 (1일 미만)

Level 2 - 2025.02.25 ~ 2025.02.25 (1일 미만)

Level 3 - 2025.02.25 ~ 2025.02.25 (1일 미만)

application.properties 파일 추가 및 실행 확인 - 2025.02.26 ~ 2025.02.26 (1일 미만)

<img width="355" alt="스크린샷 2025-02-27 오전 11 47 15" src="https://github.com/user-attachments/assets/7d69f5ad-1514-4f2d-9b6d-52ee53c4a84d" />



