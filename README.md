# assimalign branding — letterform system

One letter skeleton per name; the accent carries the signal (stem, nucleus, hub graph, point), with a soft glow in the mark's own hue behind each skeleton. Company mark is the moss-green `a`; the ograph mark is an asymmetric hub — center node, three uneven spokes.

## Palette

| Role | On dark | On light |
| --- | --- | --- |
| Ground | #161826 | #f3f5fe |
| Ink / skeleton | #e9e9ed | #292b31 |
| assimalign (company) | #85ad5a | #4e6f24 |
| cohesion | #5197db | #1d66a7 |
| ograph | #2baea1 | #007d71 |
| viu | #c472aa | #904379 |

Derivation: oklch — company moss `oklch(70% 0.12 130)` (light `oklch(50% 0.11 130)`); products share lightness/chroma with rotated hue: cohesion `oklch(66% 0.125 250)`, ograph `oklch(68% 0.11 185)`, viu `oklch(66% 0.125 340)`; on-light variants drop lightness to 50–52%. Opacities: stem halo 0.2, skeleton glow 0.55, graph edges 0.4.

## Variants

Every product mark ships twice, in both grounds:

- **per-product** (default) — the product's own accent hue: `cohesion.svg`, `ograph.svg`, `viu.svg`
- **mono** — company moss accent throughout, for contexts where one color must carry the family: `*-mono.svg`

The company mark has no mono variant (it is the accent).

## Files

- `svg/on-dark/`, `svg/on-light/` — transparent-background master marks, per-product + mono (source of truth)
- `svg/tiles/` — marks on rounded solid grounds (avatars, app tiles), dark + light × both variants
- `svg/lockups/` — mark + name; text is live Inter Medium (install Inter or convert to outlines before print use)
- `png/on-dark/`, `png/on-light/` — rasters at 16 / 32 / 64 / 128 / 256 / 512 for every variant
- `png/tiles/` — 512px tile rasters
- `nuget/` — package icons: centered glyph on a rounded tile, per-product + mono, dark + light, SVG + PNG 32/64/128/256. NuGet expects 128px (`<PackageIcon>`); dark per-product is the default. Map: Assimalign.Cohesion → `cohesion-nuget-*`, Assimalign.OGraph → `ograph-nuget-*`, Assimalign.Viu → `viu-nuget-*`.
- `theme/colors.css`, `theme/colors.json` — palette tokens

## Usage

- Wordmark: lowercase `assimalign`, Inter Medium (500), letter-spacing -0.015em; product names lowercase.
- Clear space: keep ≥ 25% of the mark's height on all sides (built into the 96px viewBox).
- Minimum sizes: mark 16px; lockups 24px tall. Below 16px prefer the tile variant; the ograph edges thin out at very small sizes.
- Use on-dark variants on grounds darker than ~40% luminance, on-light otherwise. Don't recolor; the accent sets above are the palette.
