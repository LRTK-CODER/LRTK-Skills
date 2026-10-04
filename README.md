# LRTK-Skills

개인 Claude Code 스킬을 주제별 플러그인으로 묶은 마켓플레이스입니다.

## 설치

Claude Code 세션에서 실행합니다.

```
/plugin marketplace add LRTK-CODER/LRTK-Skills
/plugin install lrtk-writing@lrtk-skills
```

## 업데이트

플러그인에 `version`을 적지 않아서 main에 병합된 커밋마다 새 버전으로 인식됩니다. 자동 업데이트는 기본으로 꺼져 있으니 직접 받습니다.

```
/plugin marketplace update lrtk-skills
```

`/plugin`의 **Marketplaces** 탭에서 `lrtk-skills`를 골라 **Enable auto-update**를 켜면 자동으로 받습니다.

## 플러그인과 스킬

| 플러그인 | 스킬 | 호출 | 하는 일 |
|---|---|---|---|
| `lrtk-writing` | `clay-ai-write` | `/lrtk-writing:clay-ai-write` | 남에게 보여 줄 글을 쓰거나 다듬을 때 사용자의 생각만 담는다. Clay의 AI Writing Policy를 따른다 |

## 개발

```
plugins/<플러그인>/
  .claude-plugin/plugin.json
  skills/<스킬>/SKILL.md
```

- 스킬 `name`은 폴더 이름과 같게 짓습니다(소문자, 숫자, `-`).
- 새 플러그인은 `.claude-plugin/marketplace.json`의 `plugins`에 추가합니다.
- 로컬에서 시험할 때는 `claude --plugin-dir plugins/<플러그인>`으로 띄우고, 고친 뒤 `/reload-plugins`로 다시 읽습니다.
- 커밋 전에 `claude plugin validate .`로 확인합니다.
- 저장소 루트의 `.claude/`는 이 저장소 개발용 설정이며 배포되지 않습니다.
