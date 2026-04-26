# Yogibo Product Shape Reference

> 정본: `~/Yogibo/knowledge/PRODUCT_REFERENCE.md`. 수정은 항상 knowledge 쪽에서 하고 `cp ~/Yogibo/knowledge/PRODUCT_REFERENCE.md ~/Yogibo/keyring/PRODUCT_REFERENCE.md`로 키링 사본 동기화. (이 배너는 양쪽 파일 모두에 동일하게 들어가 있어 cp로 덮어써도 유지됨.)

A 3D-shape reference for the Yogibo keyring printing project. Goal: given any product photo from the US, JP, or KR sites, identify the **shape family** and decide whether the photo shows the unloaded silhouette (good for Meshy single-image reconstruction) or a deformed-by-user state (bad for reconstruction).

---

## 1. About Yogibo and bean-bag mechanics

Yogibo is a US-origin lifestyle brand selling micro-bead bean-bag furniture. The product is a fabric outer shell + inner liner + EPS micro-beads. Because the beads flow freely, **the shape under load is dramatically different from the shape at rest.** A "Max" lying on the floor with no one on it is a ~170 cm pill/log; the same Max with a person sitting on it folds into a chair-like form. Almost all marketing photos and review photos show the loaded form, which makes them poor input for single-image 3D reconstruction. For Meshy, we always want **unloaded studio photos**, ideally on a plain background, and ideally a 3/4 view that shows volume and the seam pattern.

Variants (Standard / Premium / Premium Plus / Zoola outdoor / Luxe / Mix / Rainbow / Kakao Friends / Pride Edition) change cover material, print, or fabric — **not the inner shape**. A Premium Plus Drop has the same silhouette as a Standard Drop. Treat shape lines as one shape per row in this document.

---

## 2. Sofa line — shape families

All measurements are approximate, taken from yogibo.jp product pages (most reliable canonical data).

### Max

- **EN / JP / KR**: Yogibo Max / ヨギボー マックス / 요기보 맥스
- **JP handle**: `max`
- **Shape category**: long pill / elongated cylinder with rounded ends, like a giant body pillow
- **Proportions (H × W × D)**: ~170 × 65 × 55 cm. Roughly 2.6 : 1 : 0.85 when standing; flat horizontal log when lying.
- **Distinctive silhouette**: a single seam runs around the perimeter (top and bottom edges) creating a stitched piping line down each long side. No handle, no protrusions. Symmetric end-to-end.
- **Behavior under load**: extreme — folds into a chair, recliner, or bed depending on how the user sits. Almost no review photo shows it as a pill.
- **Best photo for unloaded form**: studio shot of it lying flat on the floor, 3/4 view, end visible. Both the JP `max` and KR 요기보 맥스 product pages have a clean lying-flat hero image.
- **Size class**: huge sofa.

### Mini

- **EN / JP / KR**: Yogibo Mini / ヨギボー ミニ / 요기보 미니
- **JP handle**: `min`
- **Shape category**: short pill — same silhouette as Max but shrunk lengthwise.
- **Proportions**: ~95 × 65 × 55 cm. Closer to 1.5 : 1 : 0.85 — nearly cubic when stood up.
- **Distinctive silhouette**: small log; same single seam as Max but dimensions feel almost square from the side.
- **Behavior under load**: deforms into a single-seat chair; less travel than Max because there's less length to fold.
- **Best photo**: studio standing-upright 3/4, or floor-lying 3/4.
- **Size class**: chair.

### Midi

- **EN / JP / KR**: Yogibo Midi / ヨギボー ミディ / 요기보 미디
- **JP handle**: `mid` (currently clearance)
- **Shape category**: pill — between Mini and Max length.
- **Proportions**: ~135 × 65 × 55 cm. Similar to Lite (see below).
- **Distinctive silhouette**: identical seam pattern to Max, just shorter.
- **Note**: Midi and Lite have nearly identical external dimensions (~135 cm tall). The internal density / firmness differs but the **outline is essentially the same**. From a single photo, Midi vs Lite is often visually indistinguishable; rely on color/SKU labels.
- **Best photo**: lying-flat 3/4. **Hard to disambiguate from Lite from a photo alone.**
- **Size class**: chair / love-seat.

### Lite (= Slim in KR, = Short in older US)

- **EN / JP / KR**: Yogibo Lite / ヨギボー ライト / 요기보 슬림 (KR uses "Slim", older US listings called it "Short")
- **JP handle**: `sht`
- **Shape category**: pill — slim, mid-length.
- **Proportions**: ~135 × 60 × 55 cm. Slightly slimmer width than Midi.
- **Distinctive silhouette**: same construction as Max/Midi, slimmer cross-section.
- **Best photo**: studio standing or lying 3/4.
- **Size class**: chair.

> The Max / Mini / Midi / Lite line is **one shape family** (rounded-end pill / cylinder) at four lengths. They are not visually distinct enough to identify from a single hero photo without size context.

### Drop (= Pod X in US)

- **EN / JP / KR**: Yogibo **Pod X** (US) / ヨギボー ドロップ (JP) / 요기보 드롭 (KR)
- **JP handle**: `drp` / **US slug**: `yogibo-pod-x`
- **⚠️ Cross-region naming alert**: The product KR/JP call "Drop" is sold in the US as **"Pod X"** — same product, different name. yogibo.com does NOT have a product called "Drop". Do not confuse Pod X with Pod.
- **Shape category**: vertical teardrop / onion. JP brand description: "水滴のようなカタチ" (shaped like a water drop).
- **Proportions**: 
  - JP/KR Drop: ~75 × 85 × 85 cm (H × W × D)
  - US Pod X: 32 × 32 × 32 inches (~81 × 81 × 81 cm) — listed as a cube but actual silhouette is teardrop
- **Distinctive silhouette**: rounded balloon base tapering to a small top with **a prominent fabric handle / drawstring loop on top** (US Pod X marketing calls this an "integrated ergonomic handle"). Multiple vertical seams divide it into pumpkin-segment panels.
- **Behavior under load**: holds form better than Max-family because of the segmented panel construction; the rounded base keeps shape even when sat on. The top handle stays visible.
- **Best photo**: 3/4 view, slightly above eye level so handle and base curve are both visible. The KR Drop INTRO image (blue + pink Drops) is ideal.
- **Size class**: chair (single seater).

### Pod (JP / KR only — no US product)

- **EN / JP / KR**: (no US equivalent) / ヨギボー ポッド / 요기보 팟
- **JP handle**: `pod` (currently clearance JP-side; still standard on KR)
- **⚠️ Cross-region naming alert**: yogibo.com does NOT carry Pod. The US "Pod X" is the **Drop**, not this product. **Pod has no US equivalent at all.**
- **Shape category**: rounded sphere / squat egg. Brand copy also says "water-drop-shaped" but visually the photos show a **flatter, ball-like form** sitting on the floor — more like a slightly squashed sphere than a teardrop.
- **Proportions**: ~85 × 95 × 95 cm. Almost spherical, distinctly squatter and rounder than Drop.
- **Distinctive silhouette**: ball-like body on the ground with **a small drawstring loop on top** (visible but inconspicuous, much smaller than Drop's prominent handle). Same vertical pumpkin-panel seams as Drop.
- **Pod vs Drop — what actually distinguishes them**:
  - **Both have a handle on top.** It is *not* true that Pod is handle-less.
  - **Drop**: taller teardrop body, **large prominent ergonomic handle** for carrying.
  - **Pod**: squatter sphere body, **small drawstring loop** that's barely a handle.
  - The body proportion (taller-teardrop vs squatter-ball) is the most reliable visual cue.
- **Behavior under load**: squashes flatter; the ball form bulges outward.
- **Best photo**: side-on view at floor level, full circular silhouette visible. KR Pod 015 image (two Pods in styled room — brown and wine) clearly shows the small top loop on the wine Pod.
- **Size class**: floor cushion / chair.

### Pyramid

- **EN / JP / KR**: Yogibo Pyramid / ヨギボー ピラミッド / 요기보 피라미드
- **JP handle**: `prm`
- **Shape category**: rounded three-sided pyramid (tetrahedron with rounded edges and softened apex).
- **Proportions**: ~65 × 75 × 75 cm. Triangular footprint, broad base tapering to soft peak.
- **Distinctive silhouette**: three triangular fabric panels meeting at a soft point on top. Squat, stable, low. From the product photo (purple Pyramid with child), the unloaded shape reads as a soft Toblerone-like wedge but with three faces, not two.
- **Behavior under load**: the peak collapses into a backrest; the user nestles into the V between two faces. **Heavy deformation** in most lifestyle photos.
- **Best photo**: studio 3/4 from above so all three faces are visible. The KR Pyramid product gallery has a clean overhead-3/4.
- **Size class**: floor cushion / kid chair.

### Lounger

- **EN / JP / KR**: Yogibo Lounger / ヨギボー ラウンジャー / 요기보 라운저
- **JP handle**: `lgr`
- **Shape category**: organic curved lounger / fin-shape. Brand calls it "独特の有機的な曲線" (distinctive organic curves).
- **Proportions**: ~80 × 75 × 85 cm (tall back / wider footprint). 
- **Distinctive silhouette**: looks like a **shark fin** or **comma**. Tall curved back swooping down to a wide flat seat. Has piping running around the perimeter (a sewn rim that **maintains the curved form even unloaded** — unique among Yogibo products). Very recognizable from the side.
- **Behavior under load**: holds form best of all Yogibo sofas because the piping resists collapse. The user sits in the curve and the back stays standing.
- **Best photo**: pure side view (silhouette photo). The KR Lounger INTRO (gray Lounger by a window) is essentially this. **This is the easiest Yogibo product to reconstruct from a photo** because of the firm piping.
- **Size class**: chair / personal recliner.

### Bubble (clearance / discontinued)

- **EN / JP / KR**: Yogibo Bubble / ヨギボー バブル / (limited KR availability)
- **JP handle**: `bbl`
- **Shape category**: short cylinder (drum). Despite the name, **it is NOT spherical** — JP description: "ツートンカラーの円柱型" (two-tone cylindrical shape).
- **Proportions**: ~75 × 70 × 70 cm. Almost as tall as wide. Squat drum.
- **Distinctive silhouette**: vertical cylinder with flat top and bottom, two-tone (top half + bottom half different colors). Looks like a layer cake or stool.
- **Best photo**: side-on, both color zones visible.
- **Size class**: floor stool / kid seat.
- **Surprising finding**: the "Bubble" name implies sphere; the actual shape is a flat-topped cylinder. Don't trust the name.

### Mega Max (JP-only naming)

- **EN / JP / KR**: Yogibo Mega Max / ヨギボー メガ マックス / (no direct KR equivalent)
- **JP handle**: `db-sht`
- **Shape category**: wide twin-Lite — two Lite inners side by side inside one cover.
- **Proportions**: ~135 × 120 × 55 cm. Wider than Max-Mini family because two cylinders are joined laterally.
- **Distinctive silhouette**: a fat double-pill, like two sausages stuck along their length. There may be a faint center valley between the two inner cylinders.
- **Behavior under load**: collapses into a 2-person sofa or one wide bed.
- **Best photo**: lying flat, 3/4 from above to see the joined-pill outline.
- **Size class**: huge sofa.

### Giga Max (= Yogibo Double in KR)

- **EN / JP / KR**: Yogibo Giga Max / ヨギボー ギガ マックス / 요기보 더블 맥스
- **JP handle**: `dbl`
- **Shape category**: double Max — two full Max inners stacked or side-by-side inside one outer cover.
- **Proportions**: ~170 × 140 × 55 cm. Same height as Max but double the width.
- **Distinctive silhouette**: enormous pill, twice as wide as Max. KR-side product photos labeled "Yogibo Double" show a wide loveseat/2-person sofa form when sat on.
- **Best photo**: lying-flat top-down or 3/4 to compare width to a Max.
- **Size class**: huge sofa / double bed.
- **Naming pitfall**: KR calls this "더블 맥스 (Double Max)". Don't confuse with JP "Mega Max", which is the **wide Lite**, not the wide Max.

### Hugibo

- **EN / JP / KR**: Hugibo / ハギボー / 허기보
- **JP handle**: `hgb`
- **Shape category**: humanoid character — the only Yogibo sofa with a defined character silhouette.
- **Proportions**: ~115 × 60 × 50 cm.
- **Distinctive silhouette**: vertically standing peanut/snowman body with **a smaller round head on top, two short arms protruding from the sides, and a printed face** (eyes + smiling mouth). Total: roughly a wobbly bowling pin shape with appendages. The face print is on the front panel only.
- **Behavior under load**: the body deforms when hugged, but the head and arms keep their identity because they are separately stuffed sections.
- **Best photo**: front view, full body, arms visible. The KR 허기보 SIGNATURE photo showing a child hugging the blue Hugibo is the canonical view. **For Meshy reconstruction the front-on photo will work better than 3/4 because the face needs to be square to camera.**
- **Size class**: standing character / kid hug-friend.

### Lux Ottoman (Luxe Ottoman)

- **EN / JP / KR**: Luxe Ottoman / ラックス オットマン / 럭스 오토만
- **JP handle**: `lux-omn` (also non-Luxe `omn` exists in JP buddy collection)
- **Shape category**: short cylinder / squarish footstool / cube cushion.
- **Proportions**: roughly 35 × 55 × 55 cm — wide and low.
- **Distinctive silhouette**: a soft cube/cylinder footstool. Top and bottom are flat, side panel forms a low drum. The Luxe variant has a vertical-ribbed fabric texture distinct from the smooth Standard cover.
- **Best photo**: 3/4 from slightly above so the flat top, side, and bottom edges are all visible.
- **Size class**: footrest / pillow.

### Prime (KR-only)

- **EN / JP / KR**: — / — / 요기보 프라임
- **Shape category**: giant horizontal log / rolled futon.
- **Proportions**: long horizontal cylinder, much longer than tall, no defined head/foot. From the KR PRIME INTRO image (green log next to a guitar), it looks like a rolled-up duvet or a giant draft excluder.
- **Distinctive silhouette**: low, very long, smooth cylinder. No segmentation, no handle. Lies on the floor as a horizontal bolster.
- **Behavior under load**: people lean against it like a backrest at floor seating; it deforms into a curve.
- **Best photo**: pure side view, lying on floor. KR Prime INTRO is canonical.
- **Size class**: huge floor sofa (Korea-only).
- **Note**: KR-only product. No JP / US equivalent. SKU code FUBST102.

### Variant cover lines (no shape change)

The following do **not** change the underlying inflatable shape:
- **Zoola** (`z*` JP handles, e.g. zmx, zdrp, zpm) — outdoor-fabric variant. Same shape as the base product.
- **Luxe / Lux** (`lux-*`) — premium velvet/ribbed fabric. Same shape.
- **Rainbow** (`r*`) — rainbow-printed cover. Same shape.
- **Pride Edition** (`*-pe`) — rainbow Pride print. Same shape.
- **Kakao Friends** (KR only) — character-printed cover. Same shape as base product (Drop, Slim, Pyramid).
- **Mix** (KR) — multi-color panel pattern. Same shape.
- **Premium / Premium Plus** — different inner-bead density, **same outer shape and dimensions**.

---

## 3. Body pillow / Buddy line — shape families

### Support

- **EN / JP / KR**: Yogibo Support / ヨギボー サポート / 요기보 서포트
- **JP handle**: `sup`
- **Shape category**: U-shape / horseshoe / boomerang. The product is **U-shaped in plan view**, designed to drape behind the user as a backrest with two side wings forming armrests.
- **Proportions**: ~90 × 70 × 30 cm.
- **Distinctive silhouette**: viewed from above, like a wide letter U or a thick horseshoe. From the front, looks like a short wall with two wings curving forward.
- **Behavior under load**: minor deformation; the U opening hugs the user's body, but the U-shape itself is largely preserved.
- **Best photo**: top-down or high 3/4 to show the U opening clearly.
- **Size class**: backrest / pillow accessory.

### Roll Max

- **EN / JP / KR**: Yogibo Roll Max / ヨギボー ロール マックス / 요기보 롤 맥스
- **JP handle**: `rol`
- **Shape category**: long cylinder / body-pillow tube.
- **Proportions**: ~165 cm long × 25 cm diameter. Length-to-diameter ratio ~6.6 : 1.
- **Distinctive silhouette**: smooth uniform-diameter tube with flat circular end caps. No segmentation. Like a giant rolling pin.
- **Behavior under load**: bends in the middle when used as a body pillow; otherwise holds shape.
- **Best photo**: lying on floor, 3/4 view, with one end facing camera.

### Roll Midi

- **EN / JP / KR**: Yogibo Roll Midi / ヨギボー ロール ミディ / 요기보 롤 미디
- **Shape category**: same cylinder as Roll Max, shorter (~120 cm).
- **Distinctive silhouette**: medium tube, same proportions per length.

### Roll Mini

- **EN / JP / KR**: Yogibo Roll Mini / ヨギボー ロール ミニ / 요기보 롤 미니
- **Shape category**: short stubby cylinder / lumbar bolster.
- **Proportions**: ~50 × 25 cm — stubby, almost a thick disc.
- **Distinctive silhouette**: short tube with rounded ends. From the KR Roll Mini INTRO image, the orange Roll Mini sits on top of a yellow square cushion, clearly showing a fat-sausage profile.
- **Best photo**: side-on at floor level.

> Roll Max / Midi / Mini are **one cylinder family** at three lengths. Diameter is roughly constant; length scales.

### Caterpillar Roll (Long / Max / Midi)

- **EN / JP / KR**: Yogibo Caterpillar Roll / ヨギボー キャタピラー ロール / 카터필러 롤
- **JP handle**: `ctp`
- **Shape category**: extra-long flexible cylinder, **visibly segmented** by colored ring panels along its length, like a caterpillar or a striped sock. Despite JP description not emphasizing segments, the KR product photo clearly shows alternating-color rings (e.g. dark blue / brown / cream stripes).
- **Proportions**: ~240 cm long × 20 cm diameter — much longer and thinner than Roll Max.
- **Distinctive silhouette**: long, can be **draped in an S-curve** over the back of a sofa as a body-length backrest pillow. The KR Caterpillar Roll Max INTRO photo shows it curving in an S-shape over a Yogibo Lite/Max-like base sofa.
- **Behavior under load**: very flexible; almost always photographed in a curved configuration. Straight unloaded photo is rare.
- **Best photo**: laid out straight on the floor, full length visible, to see segment colors. **This is hard to find** because most marketing photos use the curved-over-sofa configuration.
- **Size class**: long body pillow / accent.

### Roll Mate (Dog / Fox / Unicorn / Panda / Alligator / Axolotl 우파루파)

- **EN / KR**: Yogibo Roll Mate / 도그 롤 메이트, 팍스 롤 메이트, 유니콘 롤 메이트, 판다 롤 메이트, 앨리게이터 롤 메이트, 우파루파 롤 메이트
- **Shape category**: animal-shaped long body pillow. **A Roll Mini-style cylinder body with a 3D plush animal head, ears, tiny limbs, and (where applicable) a tail attached.**
- **Proportions**: tube body roughly Roll Midi-sized (~100 cm long); appendages are small and stylized.
- **Distinctive silhouettes per animal**:
  - **Dog (도그)**: brown-and-cream patched cylinder; small dog head with floppy ears, tiny paws, short tail nub. Confirmed from the KR DOG_ROLL_MATE_INTRO photo.
  - **Fox (팍스)**: orange/white; pointed fox ears and a bushy tail.
  - **Unicorn (유니콘)**: pastel pink/purple; horn on top of head, mane, tail.
  - **Panda (판다)**: black-and-white; round panda ears, no tail.
  - **Alligator (앨리게이터)**: green; long crocodile snout (segmented teeth print), back ridges, tail.
  - **Axolotl (우파루파)**: pale blue/lavender; **frilly external gills** on the sides of the head (the most distinctive feature of any Roll Mate), small leg fins, flat tail. Confirmed from the KR Axolotl_Roll_Mate_01.png photo.
- **Behavior under load**: cylinder body deforms; head, ears, gills, tail keep their stuffing-firm form because they are separate sub-units.
- **Best photo**: side view, animal head facing camera-left or camera-right, full body horizontal. All KR Roll Mate INTRO photos use exactly this angle.
- **Size class**: kid body pillow / character.
- **Region**: KR-primary; some variants (Fox, Unicorn, Alligator, Dog) are also available on the US site as "Roll Mates"; Axolotl appears KR-exclusive.

### Ghost (JP-only)

- **EN / JP / KR**: Yogibo Ghost / ヨギボー ゴースト / (not in KR catalog)
- **JP handle**: `psup`
- **Shape category**: tall back-support cushion. **Despite the name, NOT ghost-shaped.** It is a tall vertical wedge / backrest with a rounded top edge.
- **Proportions**: ~98 × 75 × 50 cm.
- **Distinctive silhouette**: tall flat-faced backrest with a rounded shoulder up top, narrow base. Profile is roughly a domed rectangle; from the front, a soft tombstone shape.
- **Best photo**: side view at chair-height to show the backward lean.
- **Size class**: backrest accessory.
- **Note**: customers might expect a cute ghost figure based on the name; the actual product is a piece of back-support furniture.

### Ottoman (Standard, JP)

- **EN / JP / KR**: Yogibo Ottoman / ヨギボー オットマン / (KR has Luxe variant only)
- **JP handle**: `omn`
- **Shape category**: same short-cylinder/cube as Luxe Ottoman in the sofa list above. Same shape; different fabric line.

---

## 4. Per-product photo strategy — best angle for unloaded silhouette

The goal for Meshy single-image reconstruction is a **clean, unloaded, 3/4 studio shot** wherever possible. Rules per shape:

| Shape line | Best angle | Why | Where to find |
| --- | --- | --- | --- |
| Max / Mini / Midi / Lite | Lying-flat 3/4 from one end | Shows the pill outline and the rounded end caps | KR `001_*_INTRO.jpg` per product folder |
| Drop | 3/4 slight-above eye level | Shows top handle + base curve in same frame | KR Drop INTRO (blue + pink Drops) is canonical |
| Pod | Side-on at floor level | Shows the squat sphere outline | KR Pod INTRO (purple ball) |
| Pyramid | High 3/4 from above | All three faces visible | KR Pyramid gallery photos |
| Lounger | Pure side view (silhouette) | The piping holds the curve, side reads the form | KR Lounger INTRO |
| Bubble | Side-on at eye level | Shows the cylinder + two-tone seam | JP `bbl` page |
| Mega Max / Giga Max (Double) | Lying-flat top-down or 3/4 | Shows the doubled width | KR Double SIGNATURE shots |
| Hugibo | Front view, full body | Face must be square to camera; arms visible | KR 허기보 SIGNATURE |
| Lux Ottoman | 3/4 from slightly above | Shows top, side, base of the cube/cylinder | KR Luxe Ottoman SIGNATURE |
| Prime | Pure side view | Just a horizontal log | KR Prime INTRO |
| Support | Top-down or high 3/4 | The U-shape opens upward and reads from above | JP/KR Support gallery |
| Roll Max / Midi / Mini | Side at floor level | Length is the main feature; show end-cap | KR Roll Mini INTRO |
| Caterpillar Roll | Lay-out-straight side view | Hard to find — most photos are S-curved | KR Caterpillar Roll Max INTRO is curved; need to seek studio straight shot from JP |
| Roll Mate (animals) | Side view, head left or right | Animal silhouette + body length both visible | KR `LIBST*_ROLL_MATE_INTRO.jpg` per animal |
| Ghost | Side view at chair height | Shows the rounded backrest profile | JP `psup` gallery |

**General fallback**: if no clean studio image exists, prefer photos with a plain wall background, no person, soft single-source lighting, and the product clearly off-the-floor (not buried in cushions).

**Avoid for Meshy input**:
- Any photo with a person sitting / lying on the bag (deformation).
- Top-down photos for vertical-asymmetric items like Drop, Lounger, Hugibo (loses height).
- Cluttered lifestyle shots where the bag overlaps furniture.
- GIFs and motion blur frames (the `_BEADS_*.gif` files in product folders are unsuitable for Meshy).

---

## 5. Cross-region naming map

Where shape is identical, the row groups EN ↔ JP ↔ KR. Highlight notes call out renames or region-only items.

### Sofa line

| English (yogibo.com) | Japanese (yogibo.jp title) | JP handle | Korean (yogibo.kr) | Notes |
| --- | --- | --- | --- | --- |
| Max | Yogibo Max ヨギボー マックス | `max` | 요기보 맥스 | All three regions, same shape |
| Mini | Yogibo Mini ヨギボー ミニ | `min` | 요기보 미니 | All three |
| (no US) | Yogibo Midi ヨギボー ミディ | `mid` | 요기보 미디 | JP currently clearance; **no US equivalent** |
| **Short** | Yogibo **Lite** ヨギボー ライト | `sht` | 요기보 **슬림** | Same shape, three different names: US "Short" / JP "Lite" / KR "Slim" |
| **Pod X** | Yogibo **Drop** ヨギボー ドロップ | `drp` | 요기보 **드롭** | ⚠️ **US calls this "Pod X"** — same teardrop with prominent handle. yogibo.com has no product named "Drop" |
| (no US) | Yogibo Pod ヨギボー ポッド | `pod` | 요기보 팟 | ⚠️ **US has no equivalent.** Pod is JP/KR only — squatter sphere with small drawstring loop. Do not confuse with US Pod X |
| (no US) | Yogibo Pyramid ヨギボー ピラミッド | `prm` | 요기보 피라미드 | JP/KR only; **no US equivalent**. KR has Kakao variant |
| Lounger | Yogibo Lounger ヨギボー ラウンジャー | `lgr` | 요기보 라운저 | All three |
| (no US) | Yogibo Bubble ヨギボー バブル | `bbl` | (limited) | JP clearance only; **cylinder, not sphere** |
| (no US) | Yogibo Mega Max ヨギボー メガ マックス | `db-sht` | (no KR) | **JP-only**. Wide-Lite (two Lite inners joined) |
| **Double Max** | Yogibo Giga Max ヨギボー ギガ マックス | `dbl` | 요기보 **더블 맥스** | Same product, three names: US "Double Max" / JP "Giga Max" / KR "Double Max". **Two Max inners joined**. JP's old name was "Double" before being renamed to "Giga Max" |
| (no US) | Hugibo ハギボー | `hgb` | 허기보 | JP/KR only; humanoid character. **No US equivalent** |
| (Wiggle Bear Hugger) | wiggle wiggle Collection | `ww-hgb` | — | JP collab; bear-shaped Hugibo variant |
| Luxe Max / Lite / Drop / Lounger | ラックス + base name | `lux-*` | 럭스 + base name | Premium-fabric covers, same shapes |
| Zoola Max / Lite / Drop / Lounger / Pyramid / Mini / Pod / Midi | ヨギボー ズーラ + base | `z*` | 줄라 + base | Outdoor-fabric, same shapes |
| Rainbow Max / Lite / Drop / Lounger | ヨギボー + base + レインボー | `r*` | (limited KR rainbow variants) | Same shapes |
| Premium / Premium Plus | プレミアム / プレミアム プラス | `pro-*` (Premium only) | 프리미엄 / 프리미엄 플러스 | Inner-bead density change, same shape |
| Kakao Friends Drop / Slim / Pyramid | — | — | 요기보 카카오프렌즈 + base | KR-exclusive licensed prints |
| Mix Drop / Lounger / Max / Slim | — | — | 믹스 + base | KR-exclusive multi-panel pattern |
| Prime | — | — | 요기보 프라임 | **KR-only**; long horizontal log shape |

### Body pillow / Buddy line

| English | Japanese (yogibo.jp) | JP handle | Korean | Notes |
| --- | --- | --- | --- | --- |
| Support | Yogibo Support ヨギボー サポート | `sup` | 요기보 서포트 | All three; U-shape backrest |
| Roll Max | Yogibo Roll Max ヨギボー ロール マックス | `rol` | 요기보 롤 맥스 | All three; long cylinder |
| Roll Midi | Yogibo Roll Midi | (KR only / accessory line) | 요기보 롤 미디 | KR-prominent; medium cylinder |
| Roll Mini | Yogibo Roll Mini | (KR only / accessory line) | 요기보 롤 미니 | KR-prominent; short cylinder |
| Caterpillar Roll Long | ヨギボー キャタピラー ロール ロング | `ctp` | 카터필러 롤 맥스 / 미디 | All three; segmented long cylinder |
| Roll Mate Fox / Dog / Unicorn / Panda / Alligator | (US) Roll Mates | (not in JP main buddy collection) | 팍스/도그/유니콘/판다/앨리게이터 롤 메이트 | KR-primary, US has subset |
| Roll Mate Axolotl | — | — | 우파루파 롤 메이트 | **KR-exclusive** |
| Ghost | Yogibo Ghost ヨギボー ゴースト | `psup` | (not in KR catalog) | JP-prominent; tall backrest |
| Ottoman | Yogibo Ottoman ヨギボー オットマン | `omn` | (KR has Luxe Ottoman only) | Short cylinder/cube footrest |
| Luxe Ottoman | ラックス オットマン | `lux-omn` | 럭스 오토만 | All three; ribbed-fabric ottoman |
| Zoola Support / Ottoman | ズーラ + base | `zsp` / `zomn` | 줄라 + base | Outdoor-fabric variants |
| Rainbow Support / Roll Max | + レインボー | `rsp` / `rrol` | (limited) | Rainbow-printed |

---

## 6. Quick-identify cheat sheet

If a single product photo shows...

- **A long horizontal pillow/log on the floor, no person** → Max, Lite/Slim, Midi, or (if very long & low) Prime. Distinguish by length.
- **A teardrop / onion taller than wide with a *prominent* fabric handle on top** → **Drop** (JP/KR) = **Pod X** (US). Same product, different name.
- **A squatter ball / sphere shorter than wide with only a *small* drawstring loop on top** → **Pod**. JP/KR only — has no US equivalent. (Don't confuse with US Pod X.)
- **A three-sided pyramidal cushion with a soft peak** → Pyramid.
- **A side-profile shark fin / comma-shaped chair with a piped rim** → Lounger.
- **A two-tone short cylinder/drum** → Bubble.
- **A wide loveseat-form sofa with two visible "seats"** → Giga Max / Double Max (KR).
- **A blue/colored character with a face, arms, and head** → Hugibo.
- **A small round footstool/cube** → Ottoman / Luxe Ottoman.
- **A horizontal log clearly twice as long as Max in scale** → Prime (KR-only).
- **A U-shaped / horseshoe cushion** → Support.
- **A long thin cylinder, plain color, ~6× longer than thick** → Roll Max / Midi / Mini (by length).
- **A long thin cylinder with colored stripe rings** → Caterpillar Roll.
- **A long pillow with a plush animal head, ears, and tiny limbs** → Roll Mate (identify by animal: dog ears, fox tail, unicorn horn, panda ears, alligator snout, **frilly axolotl gills**).
- **A tall flat-faced backrest with a rounded top edge, no character** → Ghost.

---

## 7. Confidence notes / uncertainty

Items I could **not** confidently characterize from text alone and where the doc relies on photo evidence:
- **Pyramid**: JP description says "三角形のユニークなフォルム" (triangular unique form) without specifying tetra vs triangular-prism. The product photo clearly shows three faces meeting at a soft top — i.e. a pyramid/tetrahedron, not a Toblerone prism.
- **Pod vs Drop**: JP marketing copy uses near-identical "water-drop shape" language for both, AND **both products have a handle** on top. The actual visual difference: Drop is taller-teardrop with a *prominent ergonomic handle*; Pod is squatter-ball with a *small drawstring loop*. **Body proportion is the most reliable discriminator** (Drop tall vs Pod squat). Handle size is secondary. (Note: an earlier draft of this document incorrectly said Pod has no handle — that was wrong; the small loop is just inconspicuous.)
- **Bubble**: name suggests sphere, actual shape is short cylinder. Confirmed via JP product copy "円柱型".
- **Ghost**: name suggests cute ghost figure, actual shape is a tall backrest. No ghost silhouette.

## 8. US (yogibo.com) lineup is significantly reduced

A quick reference for which products exist on yogibo.com vs JP/KR. The US site sells far fewer SKUs:

**On yogibo.com**:
- Yogibo Max / Mini / Lounger / Short / **Pod X** (= JP/KR Drop) / Double Max (= JP Giga Max) / Sleepybo Pillow / Support Pro

**NOT on yogibo.com (JP/KR only)**:
- Drop (sold as Pod X instead — same product, different name)
- Pod (no US equivalent at all)
- Pyramid
- Midi
- Bubble
- Mega Max (JP-only)
- Hugibo
- Ghost
- All Roll Mate animals
- Prime (KR-only)
- 우파루파 (Axolotl) Roll Mate (KR-only)

**Implication for the keyring project**: when looking for product images, the yogibo.com gallery is mostly useful only for Max/Mini/Lounger/Short/Pod X/Double Max. For Drop, Pod, Pyramid, Hugibo, etc., rely on JP and KR sites only. The Pod X URL on yogibo.com is the canonical US source for Drop reference photos.
- **Mega Max vs Giga Max naming**: KR site collapses both into a single "Double Max" SKU which actually maps to JP Giga Max. JP-side Mega Max has no direct KR counterpart.
- **Caterpillar Roll segmentation**: JP text doesn't mention segments, but KR product photos clearly show alternating-color ring panels. This is a real shape feature, not just a print pattern.

Items I could **not** verify and would flag:
- **Prime** dimensions: KR product detail page returned only generic catalog content via WebFetch; dimensions inferred from product hero image and blog/Musinsa references. The shape is clearly a long horizontal log, but exact length is not pinned.
- **Roll Mate exact lengths** per animal: KR product detail pages did not return spec text via WebFetch (the spec is in image-only graphics); shapes confirmed from hero photos but exact length per variant not extracted.
