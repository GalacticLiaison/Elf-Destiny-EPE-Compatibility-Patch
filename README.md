# Elf Destiny + EPE Compatibility Patch

This mod allows Elf Destiny to work with the Ethnicities & Portraits Expanded mod.

- Elf Destiny: https://steamcommunity.com/sharedfiles/filedetails/?id=3114064450
- EPE: https://steamcommunity.com/sharedfiles/filedetails/?id=2507209632

Supports CK3 1.20, Elf Destiny Beta_v2.0.7 and EPE for 1.20.0.3.

## Load Order
- EPE
- Elf Destiny
- Elf Dest + EPE Compatch

## What the patch merges
Each file below is shipped by both mods (or one mod's copy hides the other's change), so the patch carries a merged copy.

| File | Base | Changes added on top |
| --- | --- | --- |
| `gfx/models/portraits/*_head/*_head.asset` | EPE | Elf Destiny elf ear blendshape |
| `gfx/FX/jomini/portrait.shader` | Elf Destiny | EPE shadow depth bias |
| `gui/window_character.gui` | Elf Destiny | EPE window width and portrait offsets |
| `gfx/portraits/customization_rules/00_portrait_customization.txt` | Elf Destiny | EPE nude ruler designer clothes override |
| `common/genes/zzz_elf_destiny_gene_overrides.txt` | Elf Destiny | EPE `group = body` on `gene_age` |
| `common/genes/zzz_dark_elf_eye_accessory.txt` | Elf Destiny | EPE `old_eyes` template, moved to index 12 |
| `common/scripted_triggers/zzz_elf_destiny_epe_compatch_triggers.txt` | Elf Destiny | Re-asserts the magi armor and helmet exemption over EPE's vanilla copies |
| `gfx/portraits/{skin,hair,eye}_palette.dds` | EPE | Elf Destiny's custom eye colours (left edge strip) and hair colours (top left corner) |
| `gfx/portraits/portrait_modifiers/zzz_clothes_brd.txt` | Elf Destiny | EPE nude ruler designer option |

## Updating after a game or mod patch
Re-diff each file above against the new versions of both mods, keeping the base column and re-applying the other mod's changes.

### Known Issues
- zzz_clothes_brd
    - used for the toggle nudity button, causes crash to desktop when entering ruler designer
