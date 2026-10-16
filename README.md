# hanjamaster-kaiti-strokes

Modified Kaiti (해서체) stroke data used by the Android app **한자마스터 (HanjaMaster)** by RedMoon Lab.
Published to satisfy Section 2(b) of the [Arphic Public License](ARPHICPL.TXT): the modifications are
made freely available, as a whole, to all third parties under the same license.

## Origin

- Source: `graphics.txt` of [Make Me a Hanzi](https://github.com/skishore/makemeahanzi)
- Its glyphs are derived from the fonts **AR PL KaitiM GB** and **AR PL UKai** by Arphic Technology Co., Ltd.,
  distributed under the Arphic Public License.

## What was changed (2026-10-16, RedMoon Lab)

- **Format**: each character from `graphics.txt` was converted to its own JSON file named by its code point
  (e.g. `5BB6.json` = 家), with the fields `strokes` (SVG path per stroke), `medians` (centre line per stroke)
  and `notice`.
- **Stroke order**: in some files the strokes were reordered to follow the Korean stroke order.
  Stroke shapes and medians were not changed; each stroke is kept exactly as in the source, only its position in
  the list may differ. Stroke drawing directions were kept as in the source.
- **Code point**: a few characters are stored under the Korean standard code point while the source entry uses a
  different code point for the same glyph (e.g. 爲 ← 為, 敎 ← 教).
- Every file has a `notice` field stating exactly what was done to that file, including its source entry when it
  differs.

## Contents

| Folder | Meaning |
|---|---|
| `data/kaiti/` | Glyph form matches the Korean standard form. Strokes ordered as in Korean stroke order. |
| `data/kaiti_alt/` | Glyph form differs from the Korean standard form (shown only as an alternative). Stroke order unchanged from the source. |

`_index.json` in each folder lists the included code points. This repository contains only the files distributed
in the app; it will be updated when the app ships more characters.

## License

Arphic Public License — see [ARPHICPL.TXT](ARPHICPL.TXT) (included unaltered). The data is provided without
warranty.

---

## 한국어 안내

RedMoon Lab의 안드로이드 앱 **한자마스터**가 쓰는 '해서체' 획순 데이터의 수정본입니다.
Arphic Public License 2조 b항(수정본을 누구나 같은 조건으로 자유롭게 받을 수 있게 할 것)에 따라 공개합니다.

- 출처: Make Me a Hanzi `graphics.txt` (Arphic AR PL KaitiM GB / AR PL UKai 글꼴 파생)
- 바꾼 것(2026-10-16): 글자별 JSON으로 변환, 일부 글자는 획 **순서**를 한국 필순에 맞게 재배열
  (획 모양·중심선·쓰는 방향은 원본 그대로), 일부 글자는 한국 표준 코드포인트로 저장
- `data/kaiti/`: 한국 자형과 같은 글씨 / `data/kaiti_alt/`: 한국 자형과 다른 글씨(순서도 원본 그대로)
- 파일마다 `notice` 필드에 그 파일에 한 변경을 적어 두었습니다.
