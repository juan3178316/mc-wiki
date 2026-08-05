# **changelogs**

# **V2.0.1 - realease (Hotfix)**
- Fix critical issues created in Minecraft 26.40

## **V2.0.0 - release**
- Bug fixes and improve in Javascript code:
  - All JavaScript code is Flattened `(Flattening)`.
    - changes in the class `UnstackingTotem()`.
    - remove property `damageSource` of `EntityHurtBeforeEvent`. (unnecessary property).
      - Now the void totem script detect correctly that player will have the effect. reason: before, the script detect the first player that have the same name to the player effect, now works by the player ID:
      Before:
      ```
      this.player = world.getPlayers({name:namePlayer})[0];
      ```
      After:
      ```
      this.player = world.getPlayers().find(p => p.id == id);
      ```
      - update `stackingTotem` function (it's an UI form) result for better coding.
      - remove `invClear` and `#itemSlotClear` property to class `StorageTotem` for better coding.
  - Now update `@minecraft/server` to 2.8.0 for better coding.
  - Now update `@minecraft/server-ui` to 2.1.0 for add `DDUI` data drive UI, (dynamic UI screen).
  - update `totemUI` screen to `DDUI`.
  - update `stackingTotem` screen to `DDUI`.
  - Now when you are stacking totems, the stacked totem will put in the first empty slot of your inventory. (and fix a bug that remove items in your inventory before stack your totem).
- Update `min engine version` to 1.26.30, Now you require 26.30 Minecraft version to play this add-on.
- Update `format_version` of this addon from `2` to `3`. (this is for add Pack settings in behavior pack manifest) (experimental feature locked).
- Now this addon support multilanguage:
  - `es_ES`.
- Added a new feature:

### Fast un-stacking
This feature allow stack and unstack your totem of undying.

for access a this one your need use the next command:

"`/fus` or `/st:fus`". this have 3 properties:
- `Query`: you check if this feature is unlock or not.
- `true` and `false`: Enable or disable this feature.

When your interact with a totem in hand you stack another totems in your inventory, but if you're sneaking you can unstack your stacked totem of your hand.

## **V1.1.0 - release**
- Support `Vibrant Visuals`.
- Support achivements.
- Bug fixes and improve in Javascript code:
  - Now unstacked totems it's more safety.
  - Now totems spawn in your feet.
  - Now all messages and notifications in the code support multiple languages.
  - You can't lose your tótems in incorrect places.