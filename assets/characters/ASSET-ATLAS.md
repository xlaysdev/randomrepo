# Character PNG visual atlas

Visual inspection of every PNG currently stored in `assets/characters/` on the main branch. Paths below are exact and case-sensitive. This file is the filename-to-visual-role reference for the renderer. These assets are not interchangeable: some are full sprites, some are body halves, some are heads/faces, and some are special effects.

## Monika

- `1l.png`, `1r.png`: left and right halves of the standard school-uniform torso/body pose; combine as layers, not standalone sprites.
- `2l.png`, `2r.png`: alternate standard-uniform body halves with the arm/hand pose; combine as layers.
- `3a.png`, `3b.png`: complete leaning-forward school-uniform poses; same pose, different mouth/expression.
- `a.png`–`r.png`: head-only expression sprites (head/hair/face; transparent lower canvas). Use over a compatible body, not as full characters. Observed variants include neutral/smile, open-mouth speech, frown, closed-eye smile, sleepy/closed eyes, and concerned expressions.
- `g1.png`: full-body glitch/corruption sprite (visible face and body with block artifacts).
- `g2.png`, `g3.png`, `g4.png`: heavily fragmented/glitched image tiles; special-effect assets, not normal poses.
- `MonikaSpritesheet.png`: horizontal sprite strip containing small face/pose thumbnails; not a normal full-size character sprite.

## Natsuki

- `0.png`: head/hair base with blank/washed-out facial features.
- `1t.png`: head-only base with normal eyes and a small smile.
- `1l.png`, `1r.png`: left/right halves of the standard school-uniform body.
- `1bl.png`, `1br.png`: left/right halves of the casual white-shirt and pink-skirt body.
- `2l.png`, `2r.png`: standard school-uniform body halves with the hand-on-hip pose.
- `2bl.png`, `2br.png`: casual-shirt body halves with the hand-on-hip pose.
- `2bt.png`, `2bta.png`–`2bti.png`: head-only alternate side-looking expression set (eyes/mouth/blush vary). These are heads, not full-body sprites.
- `3.png`: school-uniform torso/body with crossed arms; head is absent.
- `3b.png`: casual white-shirt/pink-skirt torso/body with crossed arms; head is absent.
- `a.png`–`z.png`: head-only expression sprites. They share the pink-haired head framing but vary eyes and mouth (smiling, talking, frowning, embarrassed, eyes shut, shouting, etc.).
- `blackeyes.png`: tiny dark eye/eyebrow overlay detail.
- `eye.png`: single eye graphic/overlay.
- `mouth.png`: mouth/teeth overlay.
- `ghost1.png`: full-body ghost variant with blank face.
- `ghost2.png`: full-body ghost variant with an exaggerated grin.
- `ghost3.png`: full-body ghost variant with the head tilted sideways.
- `ghost_blood.png`: isolated blood effect pieces.
- `glitch1.png`: full-body inverted/cyan-green glitch variant.
- `scream.png`: head/expression sprite with wide eyes and open screaming mouth.
- `vomit.png`: full-body special scene sprite with vomiting effect.

## Sayori

- `1l.png`, `1r.png`: left/right halves of the standard school-uniform body.
- `1bl.png`, `1br.png`: left/right halves of the casual pink-shirt/shorts body.
- `2l.png`, `2r.png`: standard-uniform body halves with raised/curled hand pose.
- `2bl.png`, `2br.png`: casual-shirt body halves with raised/curled hand pose.
- `3a.png`–`3d.png`: complete leaning-forward school-uniform poses; facial expression changes across the four files.
- `a.png`–`y.png`: head-only expression sprites (red bow, pink hair, face); use on a compatible body. Variants cover neutral, smiling, talking, surprised, eyes-shut, and distressed expressions.
- `glitch1.png`: full-body Monika-like/corrupted sprite with horizontal glitch bands.
- `glitch2.png`: full-body corrupted Yuri-like sprite with horizontal glitch bands.
- `end-glitch1.png`, `end-glitch2.png`: heavily fragmented tile/glitch images for the ending sequence.
- `noface1.png`, `noface1b.png`: corrupted/washed-out face-and-hair overlays.
- `noface2.png`: isolated corrupted facial fragments and a cyan hand/shape; special effect, not a normal face.

## Yuri

- `0a.png`: full-body standard school-uniform sprite with blank/covered face.
- `0b.png`: same full-body pose with a glitch/corrupted face overlay.
- `1l.png`, `1r.png`: left/right pieces of the standard-uniform body.
- `2l.png`, `2r.png`: standard-uniform body pieces with a hand/arm raised toward the chest.
- `1bl.png`, `1br.png`: left/right pieces of the casual cream sweater and dark pants body.
- `2bl.png`, `2br.png`: casual-sweater body pieces with an alternate arm/hand pose.
- `3.png`: standard-uniform torso/body holding a lock of hair; head is absent.
- `3b.png`: casual-sweater torso/body holding a lock of hair; head is absent.
- `a.png`–`w.png`: head-only expression sprites (front-facing); eyes and mouth vary, including neutral, smiling, talking, worried, embarrassed, and closed-eye expressions.
- `a2.png`, `b2.png`, `c2.png`, `d2.png`, `e2.png`: side-profile head/expression variants.
- `k-old.png`, `l-old.png`, `m-old.png`, `w-old.png`: older versions of the corresponding head expressions; keep distinct from the current `k.png`, `l.png`, `m.png`, and `w.png`.
- `cuts.png`: full-body distressed scene sprite with bandaged/cut forearm detail.
- `eyes1.png`: large face/upper-body image with altered pale eyes.
- `eyes2.png`: isolated pair of eyes.
- `eyesfull.png`: full-body standard-uniform sprite with altered/pale eyes.
- `oneeye.png`: full head with one eye closed/winking.
- `oneeye2.png`: isolated single-eye overlay.
- `hisui.png`: smiling/closed-eye head expression.
- `glitch1.png`–`glitch5.png`: full-body corrupted/glitch variants with different colored horizontal bands and distortions.
- `dragon1.png`, `dragon2.png`: high-contrast red/black special corrupted full-body variants.
- `za.png`–`zd.png`: close-up head/face glitch sequence with a corrupted block over the right side of the face.

## Renderer rules

1. Never decide sprite role from a numeric filename alone. Inspect the actual PNG role listed above.
2. For split bodies, load the matching left/right pair at the same scale and alignment. Keep the transparent canvas dimensions/anchors intact.
3. For face sprites, layer the head above the selected body; do not render a head PNG as the whole character.
4. Keep special/glitch/scene sprites separate from ordinary dialogue expression selection.
5. Preserve the exact filenames and case. Do not rename or flatten the source assets.
