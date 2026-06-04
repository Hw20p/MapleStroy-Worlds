<!-- >>> managed by mswai >>> -->
@AGENTS.md
<!-- <<< managed by mswai <<< -->

@AGENTS.md

# 프로젝트 개발 방향

## 스크립팅 방식

이 프로젝트는 **Maker Studio 블록 에디터** 방식을 사용합니다.

- 스크립트는 `.codeblock` 파일에 직접 저장됩니다 (`"Source": 0`)
- `.mlua` 파일을 별도로 만들지 않습니다
- 새 스크립트 로직을 추가할 때는 기존 `.codeblock` 파일을 수정하거나, 사용자가 Maker Studio 블록 에디터에서 직접 만든 `.codeblock`에 코드를 추가합니다
- AI가 `.mlua` 파일을 만들면 사용자가 편집할 수 없으므로, 반드시 `.codeblock` 수정 방식으로 작업합니다

## 확인된 MSW API

- 플레이어 닉네임: `player.PlayerComponent.Nickname`
- 플레이어 고유 ID: `player.PlayerComponent.UserId` (숫자)
- 로컬 플레이어: `_UserService.LocalPlayer`
- 맵 이동: `_TeleportService:TeleportToEntityPath(player, '/maps/맵이름')`
- UI 엔티티 접근: `_EntityService:GetEntityByPath("/ui/그룹명/엔티티명")`
