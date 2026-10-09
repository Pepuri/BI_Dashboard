# BI Dashboard Skills

업무 질문에서 출발해 운영 BI의 설계, 적재 구조, 편집 방식, 리뷰 기준을 연결하는 공개 스킬입니다. Power BI와 Microsoft Fabric을 중심으로 작성했으며, 설계는 별도 도구 없이 제공된 자료와 스키마로 수행합니다.

**흐름:** 업무·필수 정보 → 데이터 계약 → 적재 선택 → 대표 화면 → 편집·검증 → 필수 수락 검사 → 품질 리뷰.

## 포함된 내용

- `dashboard-draft-guide`: 대시보드 초안, 기존 설계 재개, 설계 리뷰.
- 원천·행 단위·키·분모·시간·누락 상태를 연결하는 데이터 계약.
- 원본 보존 / 가공·제공 테이블 / 모델 적재 / 화면 조회를 구분하는 구조 선택.
- 조사표의 대상 식별과 요약·조사·상세의 역할 설계.
- 지표의 실무 가치, 편집 계층·스킬, 배치 편집·검증 계획.
- 필수 요구를 먼저 검사하고 초안과 실제 구현 평점을 구분하는 리뷰.
- 요청·인수인계 양식과 [합성 예제](examples/device-operations.synthetic.json).

보고서 편집 도구, 커넥터, 라이선스, 계정 권한은 포함하지 않습니다. 실제 PBIR·모델·파이프라인 편집은 해당 도구가 설치되고 현재 작업 범위에 포함된 경우 수행합니다.

## 설치

### GitHub에서 설치

Codex에 다음과 같이 요청합니다.

```text
$skill-installer
https://github.com/Pepuri/BI_Dashboard/tree/main/skills/dashboard-draft-guide
이 스킬을 설치해주세요.
```

같은 이름이 이미 설치돼 있다면 기존 개인 설정을 먼저 보존하고 설치 위치나 이름을 결정합니다. 설치 도구는 기존 폴더를 자동 덮어쓰지 않습니다.

### ZIP으로 프로젝트에 설치

저장소 ZIP을 다운로드해 압축을 풀고 `skills/dashboard-draft-guide` **폴더 전체**를 사용할 프로젝트의 `.agents/skills/dashboard-draft-guide`에 복사합니다. `references/`도 함께 있어야 합니다.

새 대화에서 확인하고 표시되지 않으면 앱을 다시 시작합니다. 현재 탐색 위치와 설치 방식은 [공식 스킬 문서](https://learn.chatgpt.com/docs/build-skills)를 참고합니다.

### 플러그인 구조

루트 `plugin.json`과 Codex 호환 `.codex-plugin/plugin.json`도 제공합니다. 공식 플러그인 가져오기·제출 흐름에 사용할 파일 구조이며, 플러그인 디렉터리에 등록되거나 심사를 완료한 패키지는 아닙니다. [공식 패키징 안내](https://developers.openai.com/plugins/build/plugins)를 따릅니다.

## 사용

```text
$dashboard-draft-guide
조직별로 동기화가 오래된 장치와 사용자를 찾는 운영 BI 초안을 만들어주세요.
첨부 스키마와 기존 일일 Import 구조를 먼저 확인해주세요.
사용자 이름·계정·장치·상태·자료 기준일은 조사표의 기본 열입니다.
목적, 원천, 지표 채택 이유, 적재 구조, 대표 화면,
편집 스킬과 방식, 검증과 리뷰 기준을 정리해주세요.
이번에는 설계만 작성해주세요.
```

구현까지 원하면 실행 범위와 대상 자료를 추가합니다. 게시·예약·실제 데이터 변경은 현재 사용자가 지정한 범위에 따라 수행합니다.

ChatGPT·Claude 등의 일반 대화에서는 `SKILL.md`와 필요한 `references/` 문서를 함께 첨부하고 해당 지침으로 설계하도록 요청할 수 있습니다. 이는 해당 환경의 자동 설치나 로컬 파일 접근을 의미하지 않습니다.

## 사용자별 방향성

[가상 사용자 프로필](examples/user-profile.example.md)을 자신의 프로젝트에 복사하고 언어·시간대·해상도·필수 열·동선·수락 조건을 맞춥니다. 다음 요청부터 프로필을 함께 참조합니다.

수정은 `문제 → 이유 → 설계 원칙 → 적용 범위 → 확인 방법`으로 프로젝트에 기록합니다. 공통 선호, 프로젝트 설정, 현재 적용 상태를 구분합니다. 개인 프로필과 고객 데이터는 이 공개 저장소에 추가하지 않습니다.

기술 버전 필드가 있다는 이유로 변경 건수를 핵심 KPI로 만들지 않습니다. 어떤 업무 판단을 돕는지 설명해야 합니다. 대상을 알아보는 필수 정보가 빠지면 다른 점수가 높아도 수락하지 않습니다.

## 선택 구현 도구

| 계층 | 설치돼 있을 때 사용할 예 |
|---|---|
| 보고서·PBIR | `powerbi-report-cli` |
| 관계·DAX·모델 | `semantic-model-authoring` |
| 필요한 변환 | `spark-cli` |
| SQL 확인 | `sqldw-cli` 또는 승인된 SQL 도구 |
| 운영 화면 리뷰 | 운영 보고서 품질 스킬과 보고서 도구 |
| 브라우저 계정 작업 | Power BI 브라우저 도구 |

별도 도구의 권한·실행·실패 규칙을 따릅니다. 미설치 상태에서도 설계와 편집 계획은 완성할 수 있습니다.

## 공개 범위

실제 고객사·사용자·계정·테넌트 ID, 비공개 대화 링크, 개인 로컬 경로, 원본 작업 이력, 실제 보고서·로그·스크린샷은 포함하지 않습니다. 예제의 이름·주소·식별자·데이터는 합성값입니다. 실제 원천과 설정은 각 사용자의 비공개 작업 공간에 둡니다. 기여할 때도 합성 예제를 사용합니다.

## English overview

An instruction-only skill connecting operational tasks, required fields, data contracts, loading choices, editing ownership, and evidence-based review. Install `skills/dashboard-draft-guide`, then invoke `$dashboard-draft-guide` with your schema and optional private profile. Authoring tools are optional and not bundled. Examples are synthetic; private history is excluded.

## License

MIT. See [LICENSE](LICENSE).
