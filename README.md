# lifos-starter

AI와 대화하며 나에게 맞는 가계관리 체계를 만드는 시작 양식입니다. 개발 지식이나 명령어 입력 없이 시작하도록 구성했습니다.

**GitHub에는 지침과 장기 기록을, Google Sheets에는 가계부와 계속 바뀌는 정보를 보관합니다.** 거래·잔액·분류표를 두 곳에서 따로 관리하지 않습니다.

버전: **0.3.2** · 통화 기본값: KRW · 시간대 기본값: Asia/Seoul. 개인 설정에서 바꿀 수 있습니다.

## 처음 시작하기

📷 처음이라면 **[화면 캡처와 함께 따라 하기](docs/setup.md)**를 먼저 여세요. Private 사본 생성부터 Google Sheets 준비·AI 연결·시작 요청까지 순서대로 안내합니다.

PC 브라우저와 AI 대화 화면을 함께 열고 순서대로 진행하세요. GitHub는 파일을 보관하는 공간이고, 저장소(repository)는 그 안의 프로젝트 폴더입니다.

1. [GitHub](https://github.com/signup) 계정을 만듭니다.
2. 이 공개 저장소 화면에서 **Use this template → Create a new repository**를 누릅니다.
3. Owner는 내 계정, 이름은 `lifos-personal`, 공개 범위는 **Private**로 선택합니다. `Include all branches`는 선택하지 않아도 됩니다.
4. **Create repository from template**을 누릅니다. 만들어진 저장소 이름 옆에 **Private** 표시가 있는지 확인합니다.
5. [Google 계정](https://accounts.google.com/signup)을 준비하고 [Google Sheets](https://sheets.google.com)에서 시작합니다. **기존 가계부가 있으면 그 주소를 준비하고**, 없으면 빈 스프레드시트 `내 가계부`를 만듭니다.
6. 시트의 **공유 → 일반 액세스**를 **제한됨**으로 유지합니다. AI 연결을 위해 전체 공개로 바꾸지 않습니다.
7. 사용하는 AI에서 GitHub와 Google Drive 연결을 설정합니다. Google Drive 연결로 Sheets를 다룹니다. [가입·연결 상세 안내](docs/setup.md)를 따라 읽기·쓰기 가능 여부를 확인하세요.
8. 아래 시작 요청의 두 URL을 내 주소로 바꾸고 AI에게 보냅니다. AI가 신규·기존 경로를 구분해 안내합니다.

이 공개 원본에는 개인 자료를 입력하지 마세요. `Fork`를 누르거나 원본 저장소의 공개 범위를 바꿀 필요가 없습니다. 템플릿 사본은 별도 저장소이며 나중에 원본 변경이 자동으로 들어오지 않습니다.

## AI에게 처음 보낼 요청

아래 두 URL은 사용자가 채우는 입력칸입니다. 개인 저장소 주소는 GitHub 브라우저 주소, 가계부 주소는 Sheets 브라우저 주소를 복사하세요.

```text
lifos-starter로 내 가계관리 체계를 설정해줘.

내 개인 Private GitHub 저장소 URL: [여기에 내 저장소 주소]
내 Google Sheets 가계부 URL: [여기에 내 시트 주소]

내 저장소의 AGENTS.md, README.md, prompts/start.md를 읽고 시작해줘.
지침·장기 기록은 GitHub, 가계부·계좌·분류·갱신 정보는 Google Sheets에 둬.
먼저 두 곳의 읽기·쓰기 가능 여부를 구분해서 확인해줘.
연결되지 않았다면 내가 화면에서 해야 할 일을 하나씩 알려줘.
먼저 기존에 쓰던 가계부가 있는지 물어봐줘.
신규라면 기본 계좌·계층 분류를 제안하고 필요한 것만 활성화해줘.
기존 시트라면 먼저 읽기 전용으로 진단하고 현재 구조에 맞는 운영지침을 제안해줘.
기존 탭·열·분류·수식을 기본 양식으로 교체하지 마.
실제 계좌나 금액은 추측하지 말고 한 번에 하나씩 질문해줘.
신규는 별도 연습 시트에서, 기존은 원본과 분리한 복사본에서 검증해줘.
기존 시트의 변경은 내가 선택한 범위만 반영해줘.
이미 만든 파일이나 시트가 있으면 확인하고 이어서 진행해줘.
로컬 수정·대화 속 표·GitHub 저장·시트 저장을 구분해서 결과를 알려줘.
주식 종목·매매·수익률 분석은 이번에 만들지 마.
```

## 내 상황에 맞게 시작하기

| 상황 | 진행 방법 |
|---|---|
| 처음 가계부를 만듦 | 아래 추천 양식을 사용하고 개인화 |
| 기존 Google Sheets 가계부가 있음 | [기존 시트 진단](docs/existing-sheet.md) 후 현재 구조에 맞는 지침 작성 |
| 기존 시트에 기능만 보완 | 부족한 기능과 최소 변경안을 검토하고 선택한 부분만 추가 |

기본 탭·열·양수 금액 방식·계층 분류는 **신규 사용자를 위한 제안**입니다. 기존 시트는 월별 탭, 음수 지출, 현재 분류와 집계 기준을 유지할 수 있습니다. 지원 가능한 기능과 제약은 진단 후 정합니다.

## 신규 사용자에게 제안하는 구성

| 구성 | 내용 | 개인화 방법 |
|---|---|---|
| 계좌 유형 6개 | 현금, 입출금 통장, 저축, 투자, 연금, 대출 | 실제 쓰는 것만 `계좌관리`에서 사용으로 변경 |
| 분류 | 수입·소비를 부모ID·Depth로 구성 | `설정`에서 하위 단계 추가·이름 변경·사용 중지 |
| 거래 원칙 | 카드 중복 방지, 이체 제외, 환불 연결, 미확인 유지 | 공통 원칙 안에서 개인 정책 추가 |
| 월간 점검 | 수입·순소비·미확인·자료 누락 확인 | `월간점검`에 결과 보관 |

기본 계좌는 보유 사실을 뜻하지 않는 후보입니다. 잔액은 비워두며 미확인을 0원으로 바꾸지 않습니다. 종목별 투자는 후속 확장 대상입니다.

## 설정 후 사용하는 요청

- [거래 기록](prompts/record.md): 거래를 추가하거나 자료를 다시 받아 확인할 때.
- [월간 점검](prompts/review-month.md): 한 달의 수입·소비와 빠진 자료를 확인할 때.
- [새 대화에서 이어가기](prompts/resume.md): AI가 이전 대화를 기억하지 못할 때.
- [계좌·분류 바꾸기](docs/customizing.md): 기본값을 내 생활에 맞출 때.

## 문서 지도

- [가입부터 설정까지](docs/setup.md)
- [신규 Google Sheets 추천 구성](docs/sheets-setup.md)
- [기존 시트 진단·적용 절차](docs/existing-sheet.md)
- [개인 시트 운영지침 양식](personal/finance-layout.example.md)
- [가계관리 공통 규칙](system/finance/rules.md)
- [개인정보와 저장 위치](docs/privacy.md)
- [거래 원문 안전 입력](docs/safe-input.md)
- [연결·저장 문제 해결](docs/troubleshooting.md)
- [가상 연습 예상 결과](examples/finance/expected-results.md)
- [업데이트와 확장](docs/updating.md)
- [배포자 안내](docs/publishing.md)

이 배포물은 지침·CSV 초기 양식·프롬프트입니다. 복제만으로 시트·수식·AI 연결이 자동 생성되지는 않습니다. 설정 단계에서 만들고 확인합니다. 실제 서비스 가입과 비개발자 사용 검증은 [파일럿 체크리스트](docs/pilot-checklist.md)로 별도 확인합니다.

## 복제 방식의 근거

공개 저장소의 fork는 공개입니다. 개인 자료를 보관하려면 템플릿에서 새 Private 저장소를 만드세요. [GitHub fork 공개 범위](https://docs.github.com/en/pull-requests/reference/forks), [템플릿으로 새 저장소 만들기](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-repository-from-a-template).
