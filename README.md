# FvT Minecraft 26.3 Resource Packs

Fix the second resource-pack reload crash in modded Minecraft 26.3 clients.

The previous release replaced the shared `minecraft:core/blit_screen` shader. With the complete Fabulously Optimized mod combination, this reproduced a native `spirv-cross.dll` crash during resource reload even though standalone Shaderc compilation passed.

The screen effects now use the vanilla 26.3 `minecraft:end_of_frame` post chain and a dedicated `fvt:post/screen_effect` shader. The common screen blit remains vanilla. The 51 effect branches are retained; the previously documented fixed-depth and merged-layer limitations remain.

Particle markers reuse existing shader varyings, and the management-only font mapping document has moved from the font asset directory to `docs/font_mapping.json`.

Validation: reproduced the native crash in an isolated copy of the full mod combination; the repaired pack loaded all three ZIPs successfully and produced a native lobby/HUD framebuffer. Crash Assistant was excluded only from the QA fixture. Public downloads were checked without authentication against SHA-1, SHA-256 and ZIP CRC. Original user mods/configuration were not modified.

Apply order: `base.zip`, `Touhou_Holy_Grail_War_sub_1.zip`, `Touhou_Holy_Grail_War_sub_2.zip`. Original project and asset credits: https://github.com/heIp12/fate-vs-touhou-Server/releases/tag/v1.0.0

## Current public downloads

- [base.zip](https://github.com/sohxx7/fvt-resourcepacks/releases/download/v2026.10.26-mc26.3.3/base.zip)
- [Touhou_Holy_Grail_War_sub_1.zip](https://github.com/sohxx7/fvt-resourcepacks/releases/download/v2026.10.26-mc26.3.3/Touhou_Holy_Grail_War_sub_1.zip)
- [Touhou_Holy_Grail_War_sub_2.zip](https://github.com/sohxx7/fvt-resourcepacks/releases/download/v2026.10.26-mc26.3.3/Touhou_Holy_Grail_War_sub_2.zip)

[SHA-1 / SHA-256 checksums](https://github.com/sohxx7/fvt-resourcepacks/releases/download/v2026.10.26-mc26.3.3/manifest.json)
