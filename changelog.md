1.21
fixed some more invisible textures

restored 3d castingfx

added interactive activators vr

fixed lots of little things, landscape seams, leftover bugs from the last version

floating objects, banners, lanterns

fixed crash in dawnfang cc

simplified and improved PBR landscape textures so they didn't overlap with other overhauls

fixed a bunch of crap I didn't even write them all down because im a lazy little shit


1.2

chose heather with skoglendi for denser coverage and splashes of color, and more performant than the previous grass for more density

fixed black spots in walls

fixed lighting , unholy mix of lux and TL/CSL , got window lights and torches working properly

added guns, made my own skse plugin to fix guns

why do I do this to myself

lots of other shit idk, forgot to write it down

oh yeah, changed back to astralite weathers again

added mountain fogs

removed a statue in bannered mare that caused an npc to walk into it like an idiot

removed fortified whiterun lanterns as they were in wrong places

redid tree lods to be lighter

pbr tree lods are pain

completely broke the list and lost the load order and a bunch of plugins, so had to restore from an older backup and reconstruct things mod by mod, so that took a week which was fun

updated CS for VR upscaling

I counted so far 114 minor fixes for various things, floating objects etc

added fantasia landscapes as its more colorful

added city trees for more color

general change to aesthetic to suit tempus high fantasy vibe more

removed eslified mods, it was too annoying to keep track

removed Elysium estate - kept causing landscape issues, and there are other housing options

removed efps - patching was a pain

removed jswords  to simplify leveled list patching

vanilla trees pbr + lightwood trees PBR to claw back some performance

aspens ablaze pbr for more color

added CS performance profiles again now that upscaling is back, making that more meaningful

overall theme of update - claw back performance, reduce complexity, and add density and color instead of sheer texture resolution / mesh complexity

added solstheim reborn fort frostmoth

removed handy crafting

removed some creature mods

lots of other shit, I mean it took me a month of solid work every day, I been a busy little bee, any way thanks for reading this, how you doing? you all good? make sure to drink enough water. 


1.0

Updated: address library, CS light, light placer, True Light, Better Bellows, Illuminous Dawnbreaker, Window Shadows Ultimate, ambient templates for lighting mods, Cathedral PBR plants, Exists High Hrothgar PBR, Tomato’s Whiterun PBR

Added:

Dynamic Wetness

HF Whiterun Bridges

Wade in Water VR

Colorful Map Markers VR

Colorful Compass Markers VR

Dynamic Location Popups VR

Crosshairs with different colors VR

Elemental Fury VR

Level list crash fix VR

Nordic Farmfield Stonewalls

Somewhat Okay Snowdrifts

Dragon Actually Fall Down

Better Rock Lichen

Northern Roads + PBR

Vanaheimr PBR AIO

Modern Hay PBR

Mihail Animals PBR

Glorious Doors of Skyrim PBR

Reinstated NOTWL PBR

3D Whiterun Trellis PBR

Updated SLAWF

Reinstated Praedy’s Sky

Beyond Skyrim Bruma PBR

Book Covers PBR

Changes:

Tweaked blocking behavior to avoid blocking spells/projectiles by accident

Removed Lanterns of Skyrim → replaced with Bottles Light Placer config

Weapons and armor no longer weightless

Simplified lighting patches

Removed Alternate Perspective vanilla Helgen start (bugged cart) → back to ASLAL with patches reinstated

Fixed ugly ground shrubs

Whiterun doors lighter wood (other wood dark)

Removed physical torch lighting (not everyone has flame spell)

Removed Palaces Castles Enhanced → replaced with Spaghetti’s

WR fieldgrass from Tomato → Skyland

No ugly rock moss persists

Fixed road signs invisible post

Modified NTOWL tree stumps dirt texture

Fixed land seams

Switched to Lux

Optimization:

Install size reduced by ~180 GB (backed up & moved overwritten files)

Startup/load times optimized (BSA packaging large texture mods)

VRAMr now default & mandatory (due to optimizations)

Known Issues:

Windhelm building near bridge has gap under door

Window light exteriors not working

Landscape seam near Redbag’s Rorikstead

0.9

OpenComposite disabled by default

VR menu mouse fix disabled by default

Reduced Faultier landscapes & AIO → 2k (from 4k)

Removed VRAMr output (simplified release process)

Adjusted Spellsiphon ward: reduced effectiveness & healing, increased light radius, removed vibration, light always active → torch+ward hybrid

Fixed Blue Palace interior (conflict from courtyard mod)

Removed terrain shadows (more dramatic exterior lighting)

Updated VR address library

Fixed dessicated corpses always having 100 gold (Meridia’s temple)

Added stealth detection fixes (lite)

Added crafting recipe distributor

Exists farmhouses 4k → 2k

Added Tomato’s farmhouses for walls

Switched to PBR ERM

Added PBR armor & weapons remastered

Added diverse PBR shrubs

Fixed hollow chickens

Added seamless dynamic cubemaps

Updated WSU (patch hub + dynamic interior lighting)

Updated PGpatcher (still white clothes issue)

Many visual/minor bug fixes

0.8

Removed Sure of Stealing

Added:

Mum’s the Word NG

More Alternate Perspective starts

Solitude Weaver’s Lane

No Loading in the Thieves Guild

Missives

Inertia

Core Impact Framework

Clouds All Over

Mists of Tamriel

CS Particle Patch

Strongbox Diversification

Dynamic Locational Armor & Weapon Impacts

Headshot Kills

Dwemer Traps

Boulders

Vampire Hunter’s Stake

Stab the Heart (CIF)

Sanguine Symphony

QuickLoot

Peasartom’s PBR Fieldgrass (overwrite Faultier’s)

Fortified Whiterun (+ Lanterns)

Nether’s Follower Framework

Skyfalls Blue Palace Courtyard

Fixes:

Glitchy blood textures

Water reflection crash

HS Interiors vs Distinct Interiors conflicts

Empowerment patch missing

Floating baskets

Mountain flowers harvesting

Updates:

Window Shadows Ultimate

Settling Items crash fix

CS latest dev build

Extras:

Added Object Interaction Framework support

Added Weightless Stuff (QoL)

Lots of small bugs fixed (some forgotten to note down)

Known Issues:

Some interiors still have mismatched lighting/floating objects

Floating lanterns in Falkreath

Rare bug: all NPCs turn invisible after long play (~14h), reload fixes

Character’s little finger stretches when using Prayer ability (funny, not game-breaking)

0.5

Added BardVR

ESLified some plugins

Removed redundant/unloaded SKSE plugins (don’t work in VR):

Immersive Equipment Displays

Simple Dual Sheath

SSMT_Fix (spring sneak movement)

Removed Bounty Quests Redone (VR issues)

Removed Valhalla Combat (not suited to VR)

Added Blade Blunt VR

Fixed floating lanterns (Soljund’s Sinkhole, Dawnstar, Morthal)

Swapped ASLAL → Alternate Perspective (test pathing crash fix)

Relic Hunter start → AP

Added Local Map Upgrade VR

Added Azurite Weathers: Alluring Sunsets/Sunrises

Added Description Framework

Fixed Local Map glitches (Bruma overwrite)

Fixed purple baskets (BoS mismatch)

Added Spellwheel VR MCM recorder defaults

Summary:

Fixed deadbodycleanupscript crash

Fixed College stairs

Removed Valravn

Added Steeds of Ultima VR

Added Conduit

Added Odin patch for Wards Functionality Extended

Solitude palace guard findmount crash fix

Breezehome normal exterior, different interior

Finished js_placed_light_patch

Added Skyrvraan patcher

Added/removed various water mods (settled on Water for ENB)

Removed Markarth Outskirts + JK’s Markarth (performance/nav issues)

Added Tomato’s Markarth CM + Spaghetti’s Markarth

Removed Markarth PBR

Fixed floating lanterns, duplicate statue

Increased Skoglendi lushness

Bumped Dyndolod quality

Removed other Dyndolod/grass performance options

Removed stamina cost for attacks

Matched LOD color blending

0.4

Updated: Light Placer, Placed Light, Address Library

Added: PBR Solitude, Riften, Windhelm

Fixed fire magic textures

Removed sword ferns

Added BFCO anims, removable torches

Removed Ancient Dwemer Metal/Pipework (redundant with PBR)

Cleaned download archives (removed Bridges of Skyrim, etc.)

Removed transparent rock acne

Added performance grass options + CS profiles (performance/upscaler)

Fixed Companions darkface

0.3

Removed Grass LOD

Removed Bridges of Skyrim (MemoryManager pathing crash)

Fixed player potion usage with Ultimate Animated Potions (excluded player, kept for NPCs)
