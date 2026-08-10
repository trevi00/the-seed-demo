# 크레딧 (Credits) — 더 시드 (The Seed)

> 이 문서는 **실제로 빌드에 실린 것만** 적는다. 구매했으나 반입하지 않은 팩은 여기 없다
> (구매 전량 대장은 `ASSET-LEDGER.md` §A — 파일 단위 출처·크롭 좌표도 그쪽에 있다).
> 반입 실측: `game/assets/` 아래 PNG·OGG·TTF **64 파일**.

---

## 1. 자체 생성 픽셀아트 23종 — 구매 팩 아님

캐릭터·몹·보스 스프라이트의 **다수는 이 프로젝트가 직접 만든 것**이다. Codex(gpt-5.6-sol)가
저작한 **Python PIL 결정론 스크립트**가 출력하며, 같은 스크립트를 다시 돌리면 같은 PNG 가
나온다(스테이징 `assets-src/codex-gen*/gen_all.py`, gitignored). 라이선스 제약 없음(자체 저작).

| 발주 | 종수 | 파일 |
|---|---|---|
| 1차 (2026-08-04, RITE-33) | 8 | `bog_lurker` · `marsh_wisp` · `lich` · `lich_core` · `harwen` · `traveler_fallen` · `villager_cursed` · `mural` |
| 2차 (2026-08-05, 마을 주민) | 5 | `villager_smith` · `villager_baker` · `villager_youth` · `villager_elder` · `innkeeper` |
| 3차 (2026-08-06, 주민 확장 + 타락자) | 8 | `villager_launderer` · `villager_mason` · `villager_herbalist` · `villager_brewer` · `villager_fisher` · `villager_guard_recruit` · `villager_carpenter` · `defector` |
| 4차 (2026-08-06, F15 보스) | 2 | `guard_captain` · `giant_robot` |

즉 `art/npc/` 17종 중 **16종**, `art/monsters/` 8종 중 **6종**, `art/structures/` 의 `mural`
이 자체 생성물이다. 팔레트만 구매 팩(`swamp/tileset.png`)에서 **색상 참조**했고 원 데이터를
재배포하지 않는다.

## 2. 구매 아트 팩 (itch.io)

| 팩 | 작가 | 실제 반입분 | 라이선스 |
|---|---|---|---|
| STRANDED Blood Forest | **Penusbmic** | `art/blood/` — 타일셋 + 프롭 13 | 상업 사용 OK · 재배포 금지 |
| STRANDED Skull Swamp | **Penusbmic** | `art/swamp/` — 타일셋 + 프롭 6 | 동상 |
| STRANDED Town Tileset | **Penusbmic** | `art/town/` — 타일셋 + 프롭 7 | 상업/수정 OK · 재판매 금지 |
| STRANDED Townfolk Pack | **Penusbmic** | `art/npc/grave_watcher.png` (1종) | 상업/수정 OK |
| DARK Homes & Shelters | **Penusbmic** | `art/structures/hut1·hut2·hut3.png` | 상업/수정 OK |
| DARK Top Down Hero: Hunter | **Penusbmic** | `art/hero/hero_blue.png` (개조) | 상업/수정 OK |
| DARK Monster Pack 1 | **Penusbmic** | `art/monsters/monster2·monster3.png` | 상업/수정 OK |
| Ornate Fantasy Pixel UI | **zLizard** | `art/ui/dark_fantasy_ui.png` | 상업/수정 OK · 크레딧 불요(자율 표기) |

Penusbmic — https://penusbmic.itch.io/ · zLizard — https://zlizard.itch.io/

## 3. 오디오

| 곡 | 번들 | 작가 | 라이선스 |
|---|---|---|---|
| Serenity in the Shadows (IV) — `audio/bgm/bgm_serenity_shadows.ogg` | 610+ Tracks Mega Music Bundle (Echoes of Elders Ch.IV) | **alkakrab** | 상업 OK · 수정 OK · Content ID 안전 · No-AI 선언 |

alkakrab — https://alkakrab.itch.io/

> 후보곡 2곡(Ancient Glow · Darkmere Loop)은 저장소에 있으나 **빌드에서 제외**된다
> (`game/export_presets.cfg` exclude_filter — 미배선 12.8MB 페이로드 절감).

## 4. 폰트 · 엔진 · 오픈소스

| 이름 | 버전 | 작가 | 라이선스 |
|---|---|---|---|
| 네오둥근모 (neodgm) — `assets/fonts/neodgm.ttf` | — | Eunbin Jeong (Dalgona.) | **SIL Open Font License 1.1** — 원문 `assets/fonts/neodgm-LICENSE.txt` 동봉 |
| **Godot Engine** | 4.6 stable | Godot 재단 | MIT |
| **Dialogue Manager** | v3.10.4 | Nathan Hoad | MIT (`game/addons/dialogue_manager/LICENSE` 동봉) |

https://github.com/neodgm/neodgm

---

## 5. 표기 의무 이행 상태 (정직 표기)

- **의무 있음 → 현재 빌드엔 없다.** 크레딧이 *계약 의무*인 항목은 RPG Icon Pack v2.2
  (Franuka — 링크 의무) 하나인데, 구매만 했고 **아이콘을 반입하지 않았다**
  (`game/assets/` 아이콘 파일 0). 반입하는 순간 이 문서에 링크를 추가해야 한다.
- **권장/자율**: 위 Penusbmic · zLizard · alkakrab · neodgm 표기는 의무가 아니나 적었다.
- **OFL 재배포 조항 이행 (2026-08-07)**: SIL OFL 1.1 은 폰트를 재배포할 때 **라이선스
  사본 동봉**을 요구한다. 웹 빌드가 폰트를 pck 에 담아 배포하므로 실제로 적용된다.
  종전엔 저장소 어디에도 OFL 원문이 없었다 → 공식 저장소(github.com/neodgm/neodgm)의
  `LICENSE.txt` 를 `game/assets/fonts/neodgm-LICENSE.txt` 로 동봉했다.
- **잔여 확인 (`ASSET-LEDGER.md` §D — 미완)**: Penusbmic 무표기 2팩(Blood Forest ·
  Skull Swamp) 상업 사용 서면 확답 보관, alkakrab 번들 동봉 라이선스 PDF 원문 확인.
  둘 다 페이지·작가 코멘트 기준으로는 허용이나 **서면 증빙이 남아 있다**.
- **대장 미기록 21파일 [열림]**: `game/assets/` 64 파일 중 §A 반입 기록 표가 덮는 것은
  43 개다. 나머지 21 개(blood 14 · hero 1 · ui 1 · monster2·3 · grave_watcher · hut2 ·
  neodgm)는 초기 'D12 웨이브' 로 사후 언급될 뿐 전용 행이 없다 — D7 위생 규칙
  ("대장에 없는 에셋은 리포에 들어올 수 없다")과 어긋난 상태다. 출처 자체는 위 표로
  확정돼 있어 **크레딧 정확성에는 영향이 없고**, 대장 행 보강이 남은 일이다.
