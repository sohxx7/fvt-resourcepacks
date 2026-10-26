# FvT Minecraft 26.3 Resource Packs

Preserve all 51 FvT screen-effect handlers while repairing Minecraft 26.3 shader reload compatibility.

The monolithic legacy `main_fx` conditional chain has been separated into individual effect functions with a flat dispatcher. Each of the 51 effect bodies is byte-for-byte identical to the prior effect implementation, including grayscale, inversion, cinematic tinting, bloom and darkening. The dedicated `end_of_frame` pipeline uses private FvT shaders and leaves shared vanilla blit shaders intact. Custom shader effects are enabled.

Native validation used the affected full Fabulously Optimized mod combination, Java 25.0.1, G1, and the user's heap layout in isolated fixtures. All three packs loaded, two actual Minecraft resource reloads completed, and native GPU frames demonstrated grayscale, inversion and darkening. Grayscale pixel analysis confirmed zero RGB-channel difference in the sampled world region. Crash Assistant was excluded only from QA; original client files were not modified.

The previously documented fixed-depth and merged-layer visual limitations remain. This release retains effect logic; it does not claim complete visual parity with 1.21.7 or exhaustive gameplay validation of every effect.

The two supplemental packs, original textures and sounds are unchanged. Apply order: `base.zip`, `Touhou_Holy_Grail_War_sub_1.zip`, `Touhou_Holy_Grail_War_sub_2.zip`.

Original project and asset credits: https://github.com/heIp12/fate-vs-touhou-Server/releases/tag/v1.0.0

## Public downloads (effects enabled)

- [base.zip](https://github.com/sohxx7/fvt-resourcepacks/releases/download/v2026.10.26-mc26.3.6-effects/base.zip)
- [Touhou_Holy_Grail_War_sub_1.zip](https://github.com/sohxx7/fvt-resourcepacks/releases/download/v2026.10.26-mc26.3.6-effects/Touhou_Holy_Grail_War_sub_1.zip)
- [Touhou_Holy_Grail_War_sub_2.zip](https://github.com/sohxx7/fvt-resourcepacks/releases/download/v2026.10.26-mc26.3.6-effects/Touhou_Holy_Grail_War_sub_2.zip)

[Checksums](https://github.com/sohxx7/fvt-resourcepacks/releases/download/v2026.10.26-mc26.3.6-effects/manifest.json)
