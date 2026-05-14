# Sermon Skills 자동 제안 및 자연어 호출 규칙

> 이 프로젝트 디렉토리에서 작업할 때 아래 규칙을 반드시 따른다.

## 1. 스킬 제안 (자동 사용 X, 먼저 물어보기)

사용자가 설교·성경·신학 관련 요청을 하면, **바로 스킬을 실행하지 말고** 아래 형식으로 먼저 제안한다:

```
이 작업에 적합한 스킬이 있습니다:
- **[스킬 한글명]** — 한 줄 설명
사용할까요?
```

- 여러 스킬이 해당되면 2~3개까지 제안하고 선택하게 한다.
- 사용자가 "응/좋아/해줘/사용하자" 등 동의하면 그때 Skill 도구로 실행한다.
- 사용자가 스킬 없이 해달라고 하면 일반 응답으로 진행한다.

## 2. 자연어 호출 (슬래시 명령 없이 스킬 사용)

사용자가 아래와 같이 **자연어로 스킬을 지정**하면, 제안 없이 바로 해당 스킬을 Skill 도구로 실행한다:

예시:
- "칼빈 스타일로 해줘" → `sermon-calvin-style-insight`
- "바빙크 코칭 해줘" → `sermon-bavinck-coaching`
- "회중 피드백 받아보자" → `sermon-audience-feedback-persona`
- "본문비평 해줘" → `sermon-textual-criticism`
- "루터 관점으로 봐줘" → `sermon-luther-coaching`

## 3. 스킬 매핑 테이블 (21개)

| 스킬 ID | 한글명 | 트리거 키워드 |
|---------|--------|-------------|
| `sermon-audience-feedback-persona` | 회중 페르소나 피드백 | 회중 반응, 회중 입장, 성도 시각, 청중 피드백, 워킹맘/청년/새신자 시각, 솔직한 반응, 회중 속마음 |
| `sermon-augustine-coaching` | 어거스틴 설교 코치 | 어거스틴, Augustine, 고백록, 하나님의 도성, 교부 설교, 사랑의 질서 |
| `sermon-bavinck-coaching` | 바빙크 신학 코칭 | 바빙크, Bavinck, 개혁교의학, 은혜와 자연, 유기적 모티프, 네덜란드 개혁주의 |
| `sermon-bible-dictionary` | 성경사전 | 성경 단어 뜻, 원어 분석, 헬라어/히브리어 뜻, 성경 인물, 성경 지명, 어원, 용례 |
| `sermon-bible-history-matcher` | 성경-세계사 매칭 | 성경 인물 세계사, 역사적 증거, 고고학 증거, 성경과 역사 교차점 |
| `sermon-calvin-institutes` | 칼빈 기독교 강요 | 기독교 강요, Institutes, 칼빈 신학, TULIP, 예정론, 그리스도 연합, 칼빈 조직신학 |
| `sermon-calvin-style-insight` | 칼빈식 설교 인사이트 | 칼빈식 설교, 칼빈처럼, 개혁주의 설교, 강해 설교, lectio continua, 칼빈 스타일 |
| `sermon-christian-history-interpreter` | 기독교 관점 역사 해석 | 기독교 관점 역사, 교회사, 종교개혁사, 역사 속 섭리, 기독교 역사 |
| `sermon-doctrinal-planner` | 교리설교 기획 | 교리설교, 교리 강론, 교리문답 설교, 사도신경 설교, 신학적 설교 |
| `sermon-emotive-writing-coach` | 감동 설교문 글쓰기 코치 | 감동적 설교문, 설교 글쓰기, 설교문 다듬기, 설교 문체, 설교 표현 강화, 설교문 피드백 |
| `sermon-greek-grammar-machen` | 메이첸 헬라어 문법 | 메이첸, 헬라어 문법, 헬라어 배우기, 코이네 헬라어, 아오리스트, 분사, 가정법 |
| `sermon-history-culture-geo-context` | 성경 역사-문화-지리 배경 | 성경 배경, 역사적 배경, 당시 상황, 고대 근동, 유대 풍습, 성경 지리 |
| `sermon-lloyd-jones-coaching` | 로이드 존스 설교 코칭 | Lloyd-Jones, MLJ, 로이드 존스, 설교와 설교자, Logic on Fire, 부흥 설교 |
| `sermon-luther-coaching` | 루터 신학-설교 코칭 | 루터, Luther, 이신칭의, 십자가 신학, 법과 복음, 종교개혁 설교 |
| `sermon-multi-bible-version-compare` | 성경 다중 번역 비교 | 번역본 비교, 여러 번역, NIV는 어떻게, Vulgata, 코란에는, 탈무드에서는 |
| `sermon-planner-52week` | 52주 설교 계획 | 52주 설교, 연간 설교, 설교 시리즈, 절기 설교, 연간 계획 |
| `sermon-qt-original-text-based` | 원문 기반 큐티(QT) | 큐티, QT, 말씀 묵상, 생명의 삶, 매일성경, 짧은 설교, 묵상 |
| `sermon-text-analysis-multimethod` | 본문 다각도 통합 분석 | 본문 분석, 다각도 분석, 구조 분석, 키아스무스, 평행 본문, 해석 검증 |
| `sermon-textual-criticism` | 성경 본문비평 | 사본 비교, 본문비평, 사해사본, 시내 사본, 이독, NA28, BHS |
| `sermon-topic-message-coach` | 설교 주제-메시지 코치 | 설교 주제 못 정하겠다, 어떻게 시작, 설교 막혔다, 설교 코칭, 메시지 정립, 설교 방향 |
| `sermon-topic-research-multidisciplinary` | 설교 주제 다학제 조사 | 설교 자료 조사, 다학제 자료, 사회적 분석, 배경 자료, 통계와 데이터 |

## 4. 복합 워크플로우 제안

설교 준비의 단계에 따라 여러 스킬을 순차적으로 제안할 수 있다:

1. **주제 못 정했을 때** → `sermon-topic-message-coach` 먼저 제안
2. **본문이 정해졌을 때** → `sermon-text-analysis-multimethod` 또는 `sermon-bible-dictionary` 제안
3. **설교문 초안 작성** → `sermon-emotive-writing-coach` 또는 신학자 코칭 스킬 제안
4. **설교문 검증** → `sermon-audience-feedback-persona` 제안

단, 한 번에 하나씩만 제안하고, 사용자가 원하면 다음 단계를 안내한다.
