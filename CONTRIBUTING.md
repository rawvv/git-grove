# Contributing to grove

grove 프로젝트에 기여해주셔서 감사합니다.

## 개발 환경 설정

```bash
git clone --bare https://github.com/rawvv/grove.git .bare
echo "gitdir: ./.bare" > .git
git worktree add main main
cd main && npm install
```

## 변경사항 제출

1. 이슈를 먼저 생성하거나 기존 이슈를 확인하세요
2. 브랜치를 만들고 변경사항을 커밋합니다
3. **changeset 파일을 추가합니다** (빠뜨리면 배포에 포함되지 않습니다):
   ```bash
   npx changeset
   ```
4. Pull Request를 생성합니다

## Changeset 작성 가이드

| 타입 | 언제 |
|------|------|
| `patch` | 버그 수정, 내부 변경 |
| `minor` | 하위 호환 새 기능 |
| `major` | 하위 비호환 변경 |

## 코드 스타일

```bash
npm run lint        # 린트 검사
npm run lint:fix    # 자동 수정
```

## 커밋 메시지

`type: description` 형식을 따릅니다.

- `feat:` 새 기능
- `fix:` 버그 수정
- `chore:` 빌드/설정 변경
- `docs:` 문서 변경
