Note: This is a BBCode formatted text-file.


[center][img]http://dl.dropbox.com/u/15430487/Online_stuff/DLbanner.png[/img][/center]
[center][url=https://dl.dropbox.com/u/15430487/LS/LICENSE%20AGREEMENT.txt][img]http://i289.photobucket.com/albums/ll205/SAB184/Copyright_Button.jpg[/img][/url][/center]


[b]SoilMod - Soil Management & Growth Control (v2.0.x)[/b]

[i]Remember to check the support topic for any additional information regarding this mod[/i]

[b][u]Changelog[/u][/b]
v2.0.31
- 'Herbicide-X' (or what custom name its given by map-mods) now decrease soil pH levels.
v2.0.30
- Support for a map-mod to override the spray-type names, by having them in the map's modDesc.XML <l10n> section.
  - So if 'Fertilizer NPK' or 'Herbicide B' is not descriptive enough, then the map-maker can overrule these, along with the hud icons [see v2.0.25]
v2.0.29
- Added a 'Herbicide-X' spray-type, which will remove all crops (including grass) at the next growth-cycle.
  - Except if fertilizer (NPK, PK, N) was sprayed in the same area afterwards.
- Re-added the following rule; "if 'kalk' is already one of accepted spray-types on spreader/sprayer, then do not add the ones from SoilMod"
  - The previous problem looked like it was due to forgetting removing other mods that conflict with SoilMod.
- Hiding SoilMod's info-panel, when vehicle info also is.
v2.0.27
- Added effects to chopped-straw.
- Removed the following rule due to possibly conflicting mods; "if 'kalk' is already one of accepted spray-types on spreader/sprayer, then do not add the ones from SoilMod"
- The 'Grow NOW!' action changed to a press-and-hold (2 sec.), before it activates. (Still only available on the server.)
- For multiplayer, attempted to inform clients of days before next growth-cycle.
v2.0.26
- Registering spray-types before the map.i3d is loaded.
v2.0.25
- Ability to use a map's own icons for spray-types, if found in `<mapMod>/fruitHuds` folder.
  - Filenames: `hud_spray_<fillname>.dds` and `hud_spray_<fillname>_small.dds`
- Added support for `ModsSettings` mod, for player-local configurable parameters.
  - SoilMod's info-panel is now a little bit easier to customize the position of.
- Removed SoilMod's spray-/fill-types from 'economy'.
- Tweaked fertilizer/herbicide prices, usage-per-sqm and mass.
- Spanish translation by Alfredo Prieto.
- Some file-extension renames, due to DedicatedServerSoftware issues warnings of too many .TXT/.PNG files.
v2.0.24
- Manure left unprocessed will increase soil moisture.
v2.0.23
- Added support for 'compost'.
- Polish translation updated by Ziuta.
v2.0.x
- Upgraded to FS15 and changed quite a bit.
- Doubled resolution of 'soil pH' levels.
- Changed fertilizer concept to 'nutrition N & PK'.
- Added extra herbicide types for weed germination prevention (for +3 days).
- Added 'soil moisture', so water also affect crop yields.
- Fully grown weed will wither when all 'nutrition N' have been used up in the area.
- Restricted switching spray-type on sprayer only when near a fertilizer tank (or similar fill-trigger.)
- Translations by; DD ModPassion, Gonimy_Vetrom, Iscarriah, mngrazy, Ziuta.


[b][u]Mod description[/u][/b]

'SoilMod' is a mod, for maps that have been correctly prepared, which attempts to add;
- custom control of growth, so it is following the in-game time,
- a proper use for lime/kalk, as soil pH is now included,
- manure must be ploughed/cultivated to take effect,
- automatic weed propagation and usage of herbicide,
- and a few other effects.

PLEASE NOTE! This mod may perhaps not be exactly what you expect or are thinking it is supposed to do. So please be open minded and give constructive criticism and/or suggestions, for how to improve future versions of it.


[b][u]How to 'prepare' the map[/u][/b]  [color=red][b]-- REQUIRED READING! --[/b][/color]

The 'SoilManagement.ZIP' mod will ONLY work on maps that have been prepared for it. There are required additions to be made in the map .I3D file, and these can be found in the ZIP file itself, in folder 'Requirements_for_your_MapI3D'.

It is expected that you know how to use a plain-text editor, like Notepad++ ("Notepad Plus Plus") or similar editor, and are able to navigate in XML text-files like the .I3D file.

[u]Preparing your Map.I3D for SoilMod[/u]

Please study and read the file '[b]Map_Instructions.txt[/b]' found in the ZIP-mod's folder '[b]Requirements_for_your_MapI3D[/b]'. That text-file contains the elements you need to add to your map's I3D file.

Always remember: BEFORE you start editing your map, to MAKE A BACKUP of it. So if anything goes wrong you can revert to the last known good working version of it, and try again.

Be aware that the normal map size is 'x1' (i.e. have density files of 4096 x 4096 pixels.) So if you have a different sized map, you will need to resize the two layer files too!

[i](Note: There are no required changes for the SampleModMap.LUA file as of this time. - The old v1.x instructions will NOT WORK for SoilMod v2.x!)[/i]


[b][u]How to use it in-game[/u][/b]  [color=red][b]-- REQUIRED READING FOR PLAYERS! --[/b][/color]

[color=red]ATTENTION![/color] Since there exist many other mods that modify the internal functions for how spreading/cultivating/harvesting works in Farming Simulator 15, there MAY BE possible mod conflicts when used together with this 'SoilMod'.

So it is [b]highly advisable[/b] to remove or disable any mods [u]and[/u] mod-maps, which potentially could affect the proper operation of 'SoilMod'.

Once you have a correctly prepared map for 'SoilMod', and placed SoilManagement.ZIP in your MODS folder, you are ready to use it in-game.

Go into the game and start the map you have prepared for 'SoilMod'. Note that it is probably possible to continue on an existing savegame, but please experiment with it first, to see if it works for you.

When the map is loading, the SoilMod scripts will print miscellaneous information to the in-game console and LOG.TXT file, which is needed in case a problem occurs. These are clearly indicated coming from 'SoilMod'.

[color=red]ATTENTION![/color] Since SoilMod adds 8 (or 9) extra new 'spray'/'fill'-types ([i]some other mods register them as 'fruit'-types but they don't use them as such[/i]), there may be problems with the "max 64 fill-types" restriction that the base-game has. So do please re-check your LOG.TXT for warnings/errors.


[u]Panel showing the condition of the current area[/u]

In the lower right corner, above the "vehicle panel", SoilMod will show a panel containing some information of the ground within a 10x10 sqm area centered around the player's current position. This is continuously updated every second.

The panel can be toggled on/off by pressing-[i]and-holding-down[/i] the 'SoilMod:Toggle grid overlay' action (default keys: [b]LEFT ALT + I[/b] and keep pressed down)


[u]Grid Heads Up Display[/u]

Sometimes a more graphical representation of an area's hidden properties would be handy. SoilMod now contains a simple "grid display" using colored/sized-dots, which will attempt to show the following four properties; soil pH, soil moisture, nutrition N & nutrition PK.

This "grid display" is cycled through using the 'SoilMod:Toggle grid overlay' action (default keys: [b]LEFT ALT + I[/b]).

The SoilMod panel will show in bold typeface which of the four properties the grid currently shows.


[u]Growth, withering included - happens at midnight every in-game day[/u]

The whole point of making this mod ([i]back then for FS2013[/i]), was for me to know [i]when[/i] the next growth cycle would happen, and be able to affect it in ways yet to determined.

As it is now, growth for [u]all[/u] crops will start [u]every day[/u] at midnight in-game time. - This can be changed in the savegame's CareerSavegame.XML file, if so needed. Look for the 'fmcSoilMod' section.

A progress indicator shows how much have been processed, as the [i]growth update stage[/i] affects a predetermined sized square of the map, which is needed to reduce potential 'game freeze' and network-latency (lag) issues.

[color=red]ATTENTION![/color] Withering is activated! - If that is a problem for you, then; play at a slower time-scale, and/or plan ahead of time.

During the growth cycle, the following things happen:
- Crops (and weeds) grow one stage, unless affected by a particular herbicide type which would either pause the growth or make the crop go withered.
- Nutrition and moisture will be consumed at different growth stages.
- Swaths/windrows and unprocessed manure will be reduced with one level (i.e. slowly dissipate.)
- Unprocessed lime and slurry becomes embedded into the soil, but at a reduced efficiency compared to cultivating it.
- Fertilizer will increase the nutrition levels.
- Weeds affected by herbicide will wither.
- Water from spraying/fertilizing will increase the soil's moisture level.


[u]Basic work-flow for tending your fields[/u]

Continuously examine if the fields has a need for nutrition, moisture or an increase of pH.

Based on the observations, then proceed with one or more of the following tasks:
- If nutrition N is low, then spray with slurry or fertilizer NPK or N. Or spread and plough/cultivate manure.
- If nutrition PK is low, then spray with fertilizer NPK or PK. Or spread and plough/cultivate manure.
- If moisture is low, then spray water and/or fertilizer (any liquid type) and/or herbicide (any type) or wait for rainy weather.
- If soil pH is low, then spread lime.
- If weeds appear, then spray herbicide (take note of correct types for crop) or plough/cultivate.

Then wait for the next growth-cycle, and repeat above.


[u]Soil pH & lime - will affect harvest yields[/u]

The soil pH condition is a new aspect of this mod ([i]except for those who already knew of it[/i]), which will severely affect harvesting yields if the soil becomes too acid.

The SoilMod panel will show what the average soil pH value is for the area - which is NOT the entire field - so keep a close eye on this.

For optimal yields, the soil pH value must be within the 'neutral' range. Anything below or above will affect outcome, according to the following curve, where 100% equals normal yields:

 5.4  =  20%
 5.6  =  70%
 5.8  =  80%
 6.2  =  90%
 6.8  = 100%
 7.5  =  90%
 8.1  =  80%
 8.5  =  50%

Spreading lime will increase the soil pH level, and if ploughed/cultivated into the ground the lime's efficiency will be higher, than when left unprocessed for the next growth cycle.

Due to technical game limitations and the way the script works, pH levels may jump at greater intervals than what would seem realistic.

Using the standard equipment for spreading solid fertilizer (not manure though), it is possible to switch spray type to lime. The F1 helpbox will show what key to press for that. Just be aware of, that the equipment must be near a fertilizer tank to do so.


[u]Water, sun and rain[/u]

The soil's moisture is affected by water and heat.

When spraying slurry, liquid fertilizer or herbicide, the ground's moisture will be increased slightly during the nightly growth-cycle. There is also possibility to actually spray water, if it is needed.

Bad weather - i.e. rain - will increase the ground's moisture too, and does this instantly every hour.
Good weather - i.e. temperature above 22 degrees - will at noon 12:00 o'clock decrease the ground's moisture.

During harvest, the soil moisture will affect yields, from the following curve:

Moisture% - Yield-modifier
       0% -  50% 
      14% -  70%
      57% - 100%
     100% -  70%


[u]Manure & slurry[/u]

Some players have expressed they would like to actually be able to first spread manure/slurry and [i]then[/i] plough/cultivate it into the ground.

This is also something that 'SoilMod' introduces, as spread manure and slurry will not instantly take effect, but have to be "mixed into the ground" to increase the nutrition of the soil, and thereby give better crop yields during harvest.

The tasks for using manure and slurry in 'SoilMod' are as follows:

[b]1.[/b] Spread manure or slurry on the field.
[b]2a.[/b] For best results, manure has to be ploughed into ground, as it will increase nutrition N & PK the most.
[b]2b.[/b] Cultivating manure is less effective.
[b]3.[/b] For slurry, there is no difference in cultivating it or "leaving it unprocessed". Slurry will first increase nutrition levels at the next growth cycle.

Note that manure which is left unprocessed on the terrain, will dissipate over time (3 days), and will in this case NOT increase nutrition levels.


[u]Fertilizer[/u]

There are 3 types of fertilizers, in both solid and liquid form;

- NPK (3-1-1)
- PK (0-3-3)
- N (5-0-0) [i](this type will also decrease soil pH level)[/i]

[i](Note: These are arbitrary in-game levels, and NOT based on anything in real life.)[/i]

Using the standard equipment for spreading fertilizer (not slurry though), it is possible to switch spray type to each fertilizer types. The F1 helpbox will show what key to press for that. Just be aware of, that the equipment must be near a fertilizer tank to do so.


[u]Nutrition levels affects yields[/u]

Due to game technical reasons - which may seem odd/unrealistic - during crop harvest, it is the ground's remaining nutrition levels that determines what the yield-boosts will be.

The curves for these are - for nutrition N:

 x0 =   +0%
 x1 =  +20%
 x2 =  +50%
 x3 =  +70%
 x4 =  +90%
 x5 = +100%
x10 =  +75%
x15 =  +50%

And for nutrition PK:

x0 =   +0%
x1 =  +10%
x2 =  +30%
x3 =  +80%
x4 = +100%
x7 =  +30%

So in other words; try to reach the ground levels 'N x5' and 'PK x4' for the best yield-boosts during harvest.

([i]For a future version: these curves could be made different for specific crop types. However this is currently NOT in v2.0.x[/i])


[u]Weed plants & herbicide - randomly appears in fields[/u]

Patches of weed plants will continuously appear in fields, as their seeds are spread with the winds. Ploughing, cultivating or seeding will remove them, but sometimes using these methods are not possible, so you need to spray herbicide.

SoilMod has 3 + 3 types of herbicides; A, B & C and AA, BB & CC. Any of these herbicides will kill weed plants. However some crops will be affected by a specific type of herbicide. In the worst case, crops becomes withered due to being exposed to the specific herbicide type.

Currently these rules apply for herbicides vs. crop-types:

- B or C can be used on; wheat, barley, rye, oat, rice. [i](Do not use type 'A'.)[/i]
- A or C can be used on; corn/maize, rape/canola, osr, luzerne, klee. [i](Do not use type 'B'.)[/i]
- A or B can be used on; potato, sugarbeet, soybean, sunflower. [i](Do not use type 'C'.)[/i]

When weed plants have been affected by herbicide, they will wither and die some days after. - However by then new weed plants may have appeared closed by... except if there was sprayed the 'double effect' herbicide (AA, BB or CC), which will prevent weed propagation and germination for up to 3 extra days.

Using the standard equipment for spreading liquid fertilizer (not slurry though), it is possible to switch spray type to each of the 3 herbicide types. The F1 helpbox will show what key to press for that.


[u]During the growth-cycle[/u]

The following effects/changes occurs during the growth-cycle:
- When crops at stages 1-7; consumes '1 N'.
- When crops at stages 3 & 5; consumes '1 PK'.
- When crops at stages 2, 3 & 5; decrease soil moisture by '1 internal-level'.
- When crops at stage 3; decrease soil pH by '1 internal-level'.
- Fully grown weeds become withered if there is zero N in soil.
- Weeds (if not withered) consume '1 N' and soil moisture.
- Swath/windrows/manure; decrease amount by 1.


[b][u]Problems or bugs?[/u][/b]

If you encounter problems or bugs using the 'SoilMod' mod, please use the support-thread at http://fs-uk.com - Find the mod (and correct version) in the mods section, in category 'Other - Game Scripts'.

Known defects/bugs:
- Spraying a different kind of fertilizer/herbicide on the field, will replace any other type of fertilizer/herbicide there may have already been there.
- Refilling spreader/sprayer will revert to fertilizer NPK, when using default fertilizer tank.
-- This is solvable, if the map-maker makes more refill tanks; one per fertilizer, herbicide and lime type.


[b][u]Restrictions[/u][/b]

The mod file SoilManagement.ZIP MUST NOT be embedded in any other mod. - However it is accepted if they are included in a mod-pack, when the mod's original hash-values are kept intact.

Please do NOT upload this mod to any other hosting site - I can do that myself, when needed!

Keep the original download link!



Credits:
Script: Decker_MMIV.
Translation 'PL': Ziuta.
Translation 'RU': Gonimy_Vetrom.
Translation 'FR': Iscarriah.
Translation 'DE': mngrazy.
Translation 'IT': DD ModPassion.
Translation 'CZ': Partly by; KingFrame, Albi.
Translation 'ES': Alfredo Prieto.
Graphics: KaosKnite, GIANTS, Decker_MMIV.
