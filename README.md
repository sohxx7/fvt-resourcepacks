# FvT Minecraft 26.3 Resource Packs

Restore real scene-depth processing and the original world-before-hands render placement while keeping all 51 FvT effect handlers enabled.

Changes:
- Sample the actual main-target depth attachment; the fixed `0.994` approximation is removed.
- Convert 26.3 reverse-Z to the finite forward-depth convention used by the original 1.21.8 formulas (near 0.05; legacy default cloud range 128). A small existing particle-marker region carries the legacy render-distance far plane.
- Run world effects in the vanilla outline render graph before first-person hands/HUD. Existing Gamerule `1.0-fvt263.3` maintains a private subpixel render cue only during effects, with cleanup after effects, disconnect and plugin shutdown. No client-side helper mod is required.
- Keep a late-pass fallback so effects remain enabled with an older server JAR until the updated server is started.
- Preserve ordinary vanilla entity outlines, original effect bodies, textures and sounds. The supplemental ZIPs are unchanged.

Requires the updated local Gamerule JAR supplied with the server port for the pre-HUD path; this release contains resource packs only.

Validation: isolated Paper/client 1.21.8 reference and 26.3 comparison at view-axis distances 2.5 / 11.5 / 31.5 blocks; eight effect modes captured, real resource reload twice, automatic cue creation/cleanup, 1,517 external API references checked, 26 SPIR-V variants and 208 Shaderc configurations passed. The existing full mod combination was tested separately without changing the user's client installation.

This restores the depth and render-order behavior. It does not claim every possible overlapping translucent/particle scene is pixel-identical: 26.3 uses composited OIT color rather than exposing all six legacy color attachments to the late post-processing chain. Nondefault legacy cloud-distance settings and every cinematic sequence have not been exhaustively compared.

Apply order: `base.zip`, `Touhou_Holy_Grail_War_sub_1.zip`, `Touhou_Holy_Grail_War_sub_2.zip`. Checksums: `manifest.json`.

Original project and asset credits: https://github.com/heIp12/fate-vs-touhou-Server/releases/tag/v1.0.0

## Public downloads

- [base.zip](https://github.com/sohxx7/fvt-resourcepacks/releases/download/v2026.10.26-mc26.3.7-depth/base.zip)
- [Touhou_Holy_Grail_War_sub_1.zip](https://github.com/sohxx7/fvt-resourcepacks/releases/download/v2026.10.26-mc26.3.7-depth/Touhou_Holy_Grail_War_sub_1.zip)
- [Touhou_Holy_Grail_War_sub_2.zip](https://github.com/sohxx7/fvt-resourcepacks/releases/download/v2026.10.26-mc26.3.7-depth/Touhou_Holy_Grail_War_sub_2.zip)

[Checksums](https://github.com/sohxx7/fvt-resourcepacks/releases/download/v2026.10.26-mc26.3.7-depth/manifest.json)
