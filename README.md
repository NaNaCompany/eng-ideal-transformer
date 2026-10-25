# 이상 변압기 전압 계산기

권선비로 이상적인 교류 변압기의 2차 전압 계산

- Plan ID: E082
- App: https://nanalab.kr/eng-ideal-transformer/
- Repository: https://github.com/NaNaCompany/eng-ideal-transformer
- Formula: `V₂ = V₁N₂/N₁`
- Output: 2차 실효전압 V₂

## Model

V₁≥0, N₁,N₂는 양의 정수. 이상 결합·교류 정상상태 모델이다. 직류 입력·코어 손실·누설·부하 전압강하·정격 출력은 제외한다.

Inputs are normalized to SI. Only one scalar is returned. Model conditions, finite numbers, physical boundaries, overflow and underflow are checked. External solver APIs and property databases are not used.

## Verification

Run `node --test tests/*.test.mjs` with Node.js 22 or later. Independent 70-digit Decimal example result: `20`. Source and license notices are in [SOURCES.md](SOURCES.md) and [LICENSE](LICENSE).

## Hosting

GitHub Pages uses `main` and `/`, with the NaNaCompany domain inherited. Google GTM, GA4, AdSense, Cloudflare analytics and the gray More Apps link are included. All code, descriptions and graphics are original.

## Static languages

Korean (existing root), English (`en/`), Spanish (`es/`), Simplified Chinese (`zh/`), Japanese (`ja/`) and German (`de/`). Each page has its own canonical URL, reciprocal hreflang, localized metadata, interface, validation messages and preview image. The language links work without JavaScript. Calculation code is shared and no runtime translation API is used.

Edit `localization/*.json` for text, `src/template.html` for the shared page, and run `python scripts/build-locales.py`. Run `python scripts/build-locales.py --check` and `npm test` before publishing. Decimal commas are accepted in Spanish and German; thousands separators are not supported.
