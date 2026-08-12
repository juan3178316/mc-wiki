# **changelogs**

## **V2.1.0 - release**
- Bug fixes and improve in Javascript code:
  - Improve potion effect properties.
  - Fix a critical bug that if you fall in the void, the void totem use 2 items instead of 1 item.
    - This bug is existing in V1.6.1
  - Now the void totem has a custom cooldown of 30 ticks (1.5 Second) for avoid spam consume item.
  - Now when you fall in the void and use the void totem, you spawn in an area of 48 block of distance instead of 100 blocks.

## **V2.0.0 - release**
- Update the void totem item texture. (because other add-on use the "same" texture)
  - update the void totem item texture MER for Vibrant Visual support.
- Added attachable to the void totem (Now it's in 3D)
  - The attachable item support emissive texture. (Glow in the dark)
  - update the void totem attachable texture MER for Vibrant Visual support.
- Update `min engine version` to 1.26.30, Now you require 26.30 Minecraft version to play this add-on.
- Update `format_version` of this addon from `2` to `3`. (this is for add Pack settings in resource pack manifest)
- Bug fixes and improve in Javascript code:
  - Now update `@minecraft/server` to 2.8.0 for better coding.
- I added to [LuisR18](https://curseforge.com/members/luisr18) in the credits authors. (He help me to make the void totem 3D item)
  - Fix a bug if you're using a official Minecraft skin and not exported skin.
- Added pack setting in the addon to fix a bug with void totem 3D item in skins. (in resource pack)
  - You can change the pack setting config in-game.
- Added subpacks.
  - Those subpacks are:
    - `2D item`: This subpack make your void totem like a normal 2D item.
    - `3D item (Default)`: This subpack make the void totem in 3D model. (`coming soon with animations`)
- Changes with the lodestone block effect:
  - When you interact with the block:
    - Plays the beacon sound.
    - Plays a new particle that their color is from block coordinate. (`each 100 blocks reset the color value`)
- Changes with the void totem pop effect:
  - now have a new sound when pop the void totem.
  - now have a new particle when poop the void totem. (`black, purple and magenta colors particles`)
- Now for unlock the void totem recipe your require in your inventory: `feather, obsidian, totem of undying or an ender pearl`.


## **V1.6.1 - release**
- Now the void totem `format_version` item it's updated from `1.21.100` to `1.26.0`.
- Bug fixes and improve in Javascript code:
  - Now `player;` `itemHand;` `itemLore;` variables in `TotemPlayerEffect()` class are removed because are not necessary write it.
  - Now callback name is `call`.
  - The pop of the void totem particle now generate less. <span style="color:#8ADA1B;">(Comming soon the particle effect change).</span>
  - Fix a bug where the totem pop sound not reproduce when the lodestone block effect is in an unloaded chunk of player.
  - Now the unstacking totem script detect correctly that player will have the effect. reason: before, the script detect the first player that have the same name to the player effect, now works by the player ID:
  Before:
  ```typescript
  this.player = world.getPlayers({name:namePlayer})[0];
  ```
  After:
  ```typescript
  this.player = world.getPlayers().find(p => p.id == id);
  ```
  - A `function` was removed for execute a `class` directly.
- Now this addon support multilanguage:
  - `en_GB`.
  - `pt_PT`.
  - `zh_TW`.
  - `ja_JP`.
  - `ru_RU`.
- Added file `contents.json` in resources and behaviors pack for index all files in this addon.


## **V1.6.0 - release**
- Fix a bug with action bar text that had some words with black color and not cyan color.
- Bug fixes and improve in Javascript code:
  - Now the callback use `{ cancel, damage, hurtEntity }` instead of `totems`. - Unstable property for now. :'/
  - Now the void totem have a behavior more realistic with the totem of undying. (Now detect the `Offhand` first instead of `Mainhand`)
- Fix a bug with the behavior pack name and description not support `pt-BR` and `zh-CN`language.
- Now this addon support multilanguage:
  - `es_ES`.
  - `fr_FR`.
  - `fr_CA`.
(_In next updates will add more languages._)


# **V1.5.1 - release (HOTFIX)**
- Now the sound `mob.endermen.portal`, play in 60 ticks (3 seconds) after you pop the void totem.
- Now you can teleport to the center block after to use the void totem with the lodestone effect.
- Added colors to the text, (Chat, Action bar, item lore, etc.)
- Now the void totem not keep their properties after to be used.
- Now this addon support multilanguage:
  - `pt-BR`.
  - `zh-CN`.
(_In next updates will add more languages._)
- Bug fixes and improve in Javascript code.

## **V1.5.0 - release**
- Now for you receive the `slow falling` effect when teleport at the top of dimension, the player need to be falling in the air.
- Now you can teleport anywhere interacting with a lodestone. `(BETA)`
  - Before pop the void totem, you teleport to the lodestone block that you used.
  - BUGS with this property:
    - <span style="color:#D3A1EE;">When you are teleported, no play the teleport sound: `mob.endermen.portal`.</span>
    - <span style="color:#D3A1EE;">The void totem keep their properties after to be used.</span>
    - <span style="color:#D3A1EE;">When you are teleported, you spawn in a corner.</span>
  - Those bug will be fix in a hotfix, (maybe in one or two weeks.)
- Bug fixes and improve in Javascript code.

## **V1.4.0 - release**
- Now the void totem support the void of 3 dimensions  (<span style="color:#6BD950;">`Overworld`</span>, <span style="color:#D54A20;">`Nether`</span>, <span style="color:#D3A1EE;">`The End`</span>).
- Now the `TP safety` is adjusted at the dimensions min height and works if the player is down of that value.
- Now if the `TP safety` TP you at the top of dimension, you receive the effect `slow falling` during 45 seconds.
- Now this addon support multilanguage:
  - `es-MX`.
  - `en-US`.
(_In next updates will add more languages._)
- Changes in the void totem crafting:
  - Now it's added a feather at the crafting.
  - Now when you uncrafting the void totem return the feather.
 - Update the format version recipes of `1.12` to `1.26.10`
 - Remove the behavior pack capacibility `script_eval`.


## **V1.3.0 - release**
- Now this addon is compatibility with <span style="color:#FBBB24;">achivements.</span> so you can't lose your achivements in your worlds.
- Now this addon is compatibility with <span style="color:#EA56D6;">Vibrant visuals.</span> _This feature is experimental, so you can find errors with this one._
- Bug fixes and improve in Javascript code:
  - Now the void totem teleport to 4 blocks close yours friends instead of 5 blocks.
  - Remove the component `EntityComponentTypes`.
  - The totem now remove any Effect status.


## **V1.2.1 - release**
- Fix a bug that when a player give `the void totem`, the translate show green.
  - Added `TP safety` in the item text.


## **V1.2.0 - release**
- The void totem teleport safety when fall in the end void.
- The totem require an ender pearl for craft.
  - If you uncraft the totem, return the ender pearl and the others items.
- Bug fixes and improve in Javascript code:
  - Now the code no query every 10 tick to check if the player have lose all of her heart. the code execute 1 o 2 ticks after that the player lose all of her heart.


## **V1.1.0 - release**
- Now you can craft the void totem in any slot of the crafting table. (so in the inventory)
- Now the void totem can uncraft and return the totem of undying and the obsidian.
- Add the `MIT license`. i forgot to add it :(


## **V1.0.0 - release**
Nothing to see here :(

In the next update, I put the changelogs
