# Design Tokens & Architecture Extraction

Replicated from reference site: `https://www.aswinpanengal.me/` for **Yashwanth Ponnam**.

## 1. Color Palette

| Token | Dark Mode (Default) | Light Mode | Purpose |
|---|---|---|---|
| `--sc-canvas` | `#11151c` / `#0c0e12` | `#f7f4f0` / `#ffffff` | Page root background |
| `--sc-surface` | `#181b24` / `#141720` | `#eeede9` / `#f1f0ec` | Cards, folders, modals |
| `--sc-surface-hover` | `#232734` | `#e4e3df` | Hover card states |
| `--sc-ink` | `#f5f4f0` / `#ffffff` | `#141414` / `#0a0a0a` | Primary text and headings |
| `--sc-ink-soft` | `#9ca3af` / `#a1a1aa` | `#5b5a57` / `#6b7280` | Subtitles, labels, descriptions |
| `--sc-line` | `rgba(255, 255, 255, 0.08)` | `rgba(0, 0, 0, 0.09)` | Dividers, folder borders |
| `--sc-accent` | `#ffd700` / `#facc15` | `#eab308` | Signature yellow accent (sneakers, glasses, focal points) |
| `--sc-accent-lime` | `#d8ff3e` | `#65a30d` | Code badges & tag highlights |
| `--sc-shadow` | `0 10px 30px rgba(0, 0, 0, 0.5)` | `0 10px 30px rgba(0, 0, 0, 0.08)` | Floating header pill, dialogs |

## 2. Typography

| Role | Font Family | Weight | Size / Line-height |
|---|---|---|---|
| Display / Hero | `'Space Grotesk', -apple-system, sans-serif` | 800 | `min(12.1vw, 24svh, 174px)`, line-height: `0.9` |
| Section Headings | `'Space Grotesk', -apple-system, sans-serif` | 700 / 800 | `clamp(2rem, 5vw, 4.2rem)`, line-height: `1.05` |
| Sub-statements | `'Space Grotesk', -apple-system, sans-serif` | 500 / 600 | `clamp(1.1rem, 2vw, 1.5rem)`, line-height: `1.3` |
| Body Text | `'Space Grotesk', system-ui, sans-serif` | 400 / 500 | `clamp(0.95rem, 0.9rem + 0.25vw, 1.1rem)`, line-height: `1.65` |
| Code & Metadata | `'JetBrains Mono', 'Geist Mono', monospace` | 500 / 600 | `clamp(0.75rem, 0.72rem + 0.15vw, 0.85rem)`, letter-spacing: `0.02em` |

## 3. Layout & Geometry

- Max container width: `82rem` (`1312px`) with responsive fluid gutter: `clamp(1.25rem, 5vw, 5.5rem)`.
- Section vertical rhythm: `clamp(4.5rem, 9vw, 10rem)`.
- Pill Header: width `350px`, height `60px`, border-radius `20px`, fixed `top: 30px`, centered.
- Safe Area Insets: `env(safe-area-inset-top)`, `env(safe-area-inset-bottom)` for notch coverage.

## 4. Keyframe Animations

1. `career-road-draw`: SVG road path progressive dashoffset animation (`1.8s cubic-bezier(0.22, 1, 0.36, 1)`).
2. `career-pin-arrive`: Milestone pin arrival scale bounce (`0.6s cubic-bezier(0.34, 1.56, 0.64, 1)`).
3. `terminal-blink`: Monospace blinking cursor (`1s steps(2, start) infinite`).
4. `wave-text-roll`: Text roll hover transform where stacked duplicate words slide up (`0.3s cubic-bezier(0.16, 1, 0.3, 1)`).
5. `crowd-walk-cycle`: HTML5 Canvas pedestrian animation loop modulated by frame delta and layer depth.
