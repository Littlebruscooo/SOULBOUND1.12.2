# Soulbound Turn Battle: 1.12.2 Remake (core)

A from-scratch remake of the core of **Soulbound Turn Battle** by Pixelcite (originally a 1.21.1 Fabric mod)
for **Minecraft 1.12.2 / Forge 14.23.5.2860**. The original mod is MIT-licensed; its textures and sounds are reused
here under that licence (see `LICENSE-ORIGINAL-ASSETS-MIT.txt`). This is *not* a port of the original code, and it
only covers the core battle loop.

## What's in it
- **Turn-based battles.** Hit a hostile mob (or get hit by one) and a battle screen opens. Bosses are excluded.
  Sneak while attacking to fight normally.
- **FIGHT** timing bar (stop the cursor near the middle for more damage), **ACT** (Check / Cheer / Guard),
  **ITEM** (eat food from your inventory to heal), **MERCY** (Spare once Mercy hits 100%, or Flee).
- **Bullet-dodging phase** after each of your turns: four attack patterns (rain, side sweeps, aimed shots, spiral).
- **Seven souls** (craft one: ender pearl + diamond + dye; right-click to equip): Determination (+25% FIGHT damage),
  Bravery (slower, easier timing bar), Integrity (-25% bullet damage), Justice (Cheer +50%), Kindness (heal 2 HP each
  enemy turn), Patience (shorter dodge phase), Perseverance (slower bullets).
- Original battle backgrounds (100), mob portraits, soul sprites, slash effects, bullets, music and sound effects.

Controls: arrows / WASD to move and navigate, Enter / Z / Space to confirm, X / Backspace to go back,
Shift to move slowly while dodging. Escape is disabled on purpose; use MERCY > Flee.

## Not included (compared with the original)
Classes and races, skill trees, parties/recruits, the Dark World dimensions, roguelite/story/quest modes, save points,
mannequins, the Dark Fountain, and anything else beyond the core loop above.

## Building
1. Install JDK 8.
2. Download the **Forge 1.12.2 MDK** (files.minecraftforge.net) and unzip it somewhere.
3. Copy this project's `src/` folder into the MDK (replace the example mod's `src/`), plus `LICENSE-ORIGINAL-ASSETS-MIT.txt`.
4. In the MDK folder: `gradlew setupDecompWorkspace` (first time only), then `gradlew build`.
   The jar appears in `build/libs/` (use the one without `-sources`). Drop it into your 1.12.2 Forge `mods` folder.
   (`gradlew runClient` launches a dev client.)

## Status
Written without access to a Minecraft/Forge toolchain, so it has **not been compiled or run yet**. The Java passes a
syntax check, but expect a few compile errors or API mismatches on the first build. Send them back and they get fixed.
