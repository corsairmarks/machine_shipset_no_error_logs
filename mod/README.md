# Overview

Are you a mod developer who is wishing for a quieter `error.log` while you debug with the Machine Shipset active?  Then this mod is for you (and me)!  This mod does **NOT** redistribute any of the graphics from the Machine Shipset, but does redefine and replace entity asset files in order to eliminate many error messages and some syntax errors.

Along the way, I also added missing particles based on the source definitions (generally from the mammalian or molluscoid ships).  Also missing from several files were the variables defining engine trail length.  Between these two refinements, the Machine Shipset looks nicer than ever.

# Changes

Many entity definitions were tweaked to remove (or sometimes add) animations.  "Removed" code was commented out rather than deleted so it should be straightforward to re-enable sections responsible for things for compatibility with NSC, RS, DSS, or ACG.  AryxErin, if you are reading this - feel free to harvest fixes for use in your mod directly.

* `common/species_classes/machine_01_species_classes.txt` mark species class as not randomized, set to use `machine_01` graphical culture
* `common/species_names/machine_mgo_names.txt` fix syntax error for `plexi` (missing `=`)
* `gfx/models/ships/Colossus_Assets/machine_01_colossus.asset`
    * Remove reference to particle `lithoid_01_starbase_core_effect` - does not actually exist despite the game also referencing it
    * Remove animation state from `machine_01_colossus_entity` - the mesh isn't animated
* `gfx/models/ships/Colossus_Assets/machine_01_colossus.gfx`
    * Remove animation definitions - the mesh `machine_01_colossus_frame_mesh` isn't animated
    * Add missing locator to: `frame_ship`
* `gfx/models/ships/Crisis_Assets/machine_01_crisis_entities.asset`
    * ARYXERIN's name should be inside a comment
    * Remove duplicate, non-crises entities (everything from BATTLESHIP and below)
* `gfx/models/ships/Juggernaut_Assets/machine_01_juggernaut.asset`
    * Add missing variables `small_trail_W` and `small_trail_L`
    * Add missing variables `medium_trail_W` and `medium_trail_L`
    * Add missing variables `large_trail_W` and `large_trail_L`
    * Add missing locator: `strike_craft_locator_04`
    * Add missing locator: `strike_craft_locator_05`
    * Add missing locator: `strike_craft_locator_06`
* `gfx/models/ships/Megastructure_Assets/Dyson_Sphere/machine_01_dyson_sphere_entities.asset` remove animation from `machine_01_dyson_sphere_phase_01_entity` - the mesh isn't animated
* `gfx/models/ships/Megastructure_Assets/Gateway/machine_01_gateway.asset`
    * Remove duplicate animation definitions (these animations are defined in the base game)
    * Remove invalid animation from `machine_01_gateway_entity` - the `death` state is not animated
    * Remove invalid animation from `machine_01_deactivated_gateway_entity` - the `death` state is not animated
    * Remove invalid animation from `machine_01_reactivated_gateway_entity` - the `death` state is not animated
* `gfx/models/ships/Megastructure_Assets/Gateway/machine_01_gateway.gfx`
    * Remove animation definitions from `machine_01_gateway_mesh` - the mesh isn't animated
* `gfx/models/ships/Megastructure_Assets/Matter_Decompressor/machine_01_matter_decompressor_01.asset`
    * Remove invalid animation from `machine_01_matter_decompressor_stage_1_construction_entity` - the mesh isn't animated
    * Remove invalid animation from `machine_01_matter_decompressor_stage_2_construction_entity` - the mesh isn't animated
    * Remove invalid animation from `machine_01_matter_decompressor_stage_3_construction_entity` - the mesh isn't animated
    * Remove invalid animation from `machine_01_matter_decompressor_stage_4_construction_entity` - the mesh isn't animated
* `gfx/models/ships/Megastructure_Assets/Matter_Decompressor/machine_01_matter_decompressor_01.gfx` remove mesh that doesn't exist `machine_01_matter_decompressor_destroyed_01_mesh`
* `gfx/models/ships/Megastructure_Assets/Mega_Art/machine_01_mega_art_institution_entites.asset`
    * Remove animation from `machine_01_mega_art_institution_stage_1_entity` - the mesh isn't animated
* `gfx/models/ships/Megastructure_Assets/Mega_Shipyard/machine_01_mega_shipyard_entities.asset`
    Fix improperly-placed closing brace `}` for `machine_01_mega_shipyard_01_stage_1_entity`
    * Add missing animation to `death` state for `machine_01_mega_shipyard_01_stage_1_entity`
    * Remove invalid animation from `machine_01_mega_shipyard_01_stage_1_section_entity` - the `death` state is not animated
    * Add missing animation to `death` state for `machine_01_mega_shipyard_01_stage_2_entity`
    * Remove invalid animation from `machine_01_mega_shipyard_01_stage_2_section_entity` - the `death` state is not animated
    * Add missing animation to `death` state for `machine_01_mega_shipyard_01_stage_3_entity`
    * Remove invalid animation from `machine_01_mega_shipyard_01_stage_3_section_entity` - the `death` state is not animated
* `gfx/models/ships/Megastructure_Assets/Spy_Orb/machine_01_spyorb_entities.asset`
    * Remove animation from `machine_01_spyorb_part_1_entity` - the mesh isn't animated
    * Remove animation from `machine_01_spyorb_part_2_entity` - the mesh isn't animated
    * Remove animation from `machine_01_spyorb_part_2_entity` - the mesh isn't animated
* `gfx/models/ships/Megastructure_Assets/Strategic_Coordination_Centre/machine_01_strategic_coordination_center_01.asset`
    * Remove animation from `machine_01_strategic_coordination_center_stage_2_entity` - the mesh isn't animated
    * Remove animation from `machine_01_strategic_coordination_center_stage_3_entity` - the mesh isn't animated
* `gfx/models/ships/Megastructure_Assets/Think_Tank/machine_01_think_tank_entites.asset`
    * Add missing animation to `construction` state for `machine_01_thinktank_phase_01_entity`
    * Add missing animation to `construction` state for `machine_01_thinktank_phase_02_entity`
    * Add missing animation to `construction` state for `machine_01_thinktank_phase_03_entity`
* `gfx/models/ships/NSC_Assets/_machine_01_entities_explorationship.asset`
    * Remove entity `machine_01_explorationship_entity` that uses a removed mesh
* `gfx/models/ships/NSC_Assets/machine_01_captainx3_entities_Carrier.asset`
    * Remove entity `machine_01_Carrier_entity` that uses a removed mesh
    * Remove entity `machine_01_Carrier_bow_M2S4_entity` that refers to a mesh that does not exist
* `gfx/models/ships/NSC_Assets/machine_01_captainx3_entities_Dreadnought.asset`
    * Remove entity `machine_01_Dreadnought_entity` that uses a removed mesh
    * Remove entity `machine_01_Dreadnought_bow_M2S4_entity` that refers to a mesh that does not exist
* `gfx/models/ships/NSC_Assets/machine_01_captainx3_entities_escortcarrier.asset`
    * Remove entity that uses a removed mesh `machine_01_escortcarrier_entity`
    * Fix missing `_` for particle name `generic_05_exhaust_circle_moving`
* `gfx/models/ships/NSC_Assets/machine_01_captainx3_entities_Flagship.asset` remove reference to particle `nsc_flagship_explosion_particle` that doesn't exist
* `gfx/models/ships/NSC_Assets/machine_01_captainx3_entities_StrikeCruiser.asset`
    * Remove entity `machine_01_StrikeCruiser_entity` that uses a removed mesh
    * Add missing variables `medium_trail_W` and `medium_trail_L`
* `gfx/models/ships/NSC_Assets/machine_01_entities_Battlecruiser.asset`
    * Remove entity `machine_01_Battlecruiser_entity` that uses a removed mesh
    * Fix missing `_` for particle name `generic_05_exhaust_circle_moving`
* `gfx/models/ships/NSC_Assets/machine_01_nsc_ships_meshes.gfx`
    * Uncomment section mesh that was previously duplicated: `machine_01_exploration_cruiser_mid2_mesh`
    * Remove meshes that don't exist: `machine_01_dreadnought_frame_mesh`, `machine_01_flagship_frame_mesh`, `machine_01_battlecruiser_frame_mesh`
* `gfx/models/ships/Old_Assets/machine_01_old_meshes.gfx`
    * Remove mesh that does not exist: `machine_01_old_battleship_bow_M2S4_mesh`
    * Remove mesh that does not exist: `machine_01_old_battleship_mid_2_M4SHB_mesh`
* `gfx/models/ships/RS_Assets/_machine_01_ships_entities_rs_battlecruiser.asset`
    * Add missing variables `medium_trail_W` and `medium_trail_L`
    * Remove animation from `machine_01_rs_battlecruiser_entity` - the mesh isn't animated
* `gfx/models/ships/RS_Assets/_machine_01_ships_entities_rs_dreadnought.asset`
    * Remove entity `machine_01_rs_dreadnought_bow_M2S4_entity` that refers to a mesh that does not exist
    * Add missing variables `medium_trail_W` and `medium_trail_L`
* `gfx/models/ships/RS_Assets/_machine_01_ships_entities_rs_ea_cruiser.asset`
    * Add missing variables `medium_trail_W` and `medium_trail_L`
    * Remove attachment references to an entity that doesn't exist: `rs_emitter_red_entity`
    * Remove attachment references to an entity that doesn't exist: `rs_energy_red_entity`
* `gfx/models/ships/RS_Assets/_machine_01_ships_entities_rs_heavy_dreadnought_type_b.asset`
    * Add missing variables `medium_trail_W` and `medium_trail_L`
    * Remove entity `machine_01_rs_heavy_dreadnought_type_b_bow_M2S4_entity` that refers to a mesh that does not exist
    * Remove attachment reference to an entity that doesn't exist: `machine_01_rs_heavy_dreadnought_type_b_mid2_L3_bottom_entity`
* `gfx/models/ships/RS_Assets/_machine_01_ships_entities_rs_support_cruiser.asset`
    * Add missing variables `medium_trail_W` and `medium_trail_L`
    * Remove attachment reference to an entity that doesn't exist: `rs_emitter_blue_entity`
    * Remove attachment reference to an entity that doesn't exist: `rs_energy_blue_entity`
* `gfx/models/ships/Titan_Assets/machine_01_titan_entities.asset`
    * Fix incorrect mesh reference for `machine_01_titan_entity`
* `gfx/models/ships/machine_01_ships_animations.asset`
    * Remove incorrect prefix "gfx/models/ships" from cruiser death animations
    * Remove (unused) animation that does not exist: `machine_01_cruiser_frame_idle_animation`
    * Remove (unused) animation that does not exist: `machine_01_science_station_idle_animation`
    * Remove (unused) animation that does not exist: `machine_01_science_station_death_animation`
    * Remove (unused) animation that does not exist: `machine_01_orbital_station_main_idle_animation`
    * Remove (unused) animation that does not exist: `machine_01_orbital_station_main_death_animation`
* `gfx/models/ships/machine_01_ships_entities.asset`
    * Replace mis-named particle `large_player_lithoid_ship_explosion_s_effect` with the correct particle `large_player_ship_explosion_particle`
    * Remove entity `machine_01_battleship_bow_M2S4_entity` that uses a removed mesh
    * Remove entity without mesh: `machine_01_orbital_station_entity`
    * Remove entity without mesh: `machine_01_orbital_station_core_entity`
    * Change some entities to use `locator_mesh` instead of meshes that don't exist: `machine_01_colonizer_entity`, `machine_01_transport_entity`
    * Add missing entity: `machine_01_ring_habitat_landmass_entity`
    * Allow nightlights attachment on `machine_01_habitat_phase_03_entity`
    * Remove animation from `machine_01_habitat_phase_03_section_entity` - the mesh isn't animated
    * Remove animation from `machine_01_terraform_station_entity` - the mesh isn't animated
    * Add state timers to `machine_01_terraform_station_entity` matching those on `machine_01_mining_station_entity` (which uses the exact same mesh)
    * Set animation for the `working` and `working_looping` states for `machine_01_constructor_entity` to `idle`; the attached entity `machine_01_construction_ship_entity` is responsible for the actual animation
    * Remove animations from `machine_01_colonizer_entity` - the mesh isn't animated
    * Add missing locator to `machine_01_colonizer_entity`: `part1`
    * Remove animations from `machine_01_science_ship_entity` - the mesh isn't animated
    * Remove animations from `machine_01_transport_entity` - the mesh isn't animated
* `gfx/models/ships/machine_01_ships_meshes.gfx`
    * Remove meshes that do not exist: `machine_01_corvette_S1_mesh`, `machine_01_battleship_bow_M2S4_mesh`, `machine_01_battleship_mid_2_M4SHB_mesh`
    * Remove duplicate meshes: `machine_01_exploration_cruiser_stern_L1_mesh`,
    `machine_01_exploration_cruiser_mid2_mesh`, `machine_01_strike_cruiser_stern_M1_mesh`
    * Remove incompatible animation `machine_01_cruiser_frame_death_animation` from `machine_01_cruiser_frame_mesh` (yes really)
* `gfx/particles/_machine_shipset_supplemental_particles.gfx` (new file) add missing particles:
    * `generic_035_exhaust_circle_moving`
    * `machine_01_0_5_exhaust_idle_particle`
    * `machine_01_1_0_exhaust_idle_particle`
    * `machine_01_1_5_exhaust_idle_particle`
    * `machine_01_2_0_exhaust_idle_particle`
    * `machine_01_2_5_exhaust_idle_particle`
    * `machine_01_3_0_exhaust_idle_particle`
    * `machine_01_10_0_exhaust_idle_particle`
    * `machine_01_1_45_exhaust_idle_particle`
    * `machine_01_2_35_exhaust_idle_particle`
    * `machine_01_1_45_ship_exhaust_moving_particle`
    * `machine_01_2_35_ship_exhaust_moving_particle`
    * `machine_01_1_5_exhaust_oblong_idle_particle`
    * `machine_01_2_0_exhaust_oblong_idle_particle`
    * `machine_01_2_35_exhaust_oblong_idle_particle`
    * `machine_01_1_5_ship_exhaust_oblong_moving_particle`
    * `machine_01_2_0_ship_exhaust_oblong_moving_particle`
* `gfx/particles/lithoid_01_science_core.asset` blank out file to remove duplicate particle (exact duplicate of the base game's particle of the same name)
* `sound/athena_sound_category.asset` (new file) sound effect `athena_cruiser_engine_fire` now has a category

## Compatibility

Will probably cause issues with Machine Shipset compatibility patches for other large mods (New Ship Classes, Downscaled Ships, Real Space System Scale, Aesthetic Cinematic Gameplay).  I don't use any of those mods and did not test for compatibility, but I know that I commented out code related to supporting assets from those mods.  That ensures errors are not generated when they are not installed.

Built for Stellaris version 3.2.\* "Herbert."  Not compatible with achievements.

### Required Dependency Mods

[Machine Shipset](https://steamcommunity.com/sharedfiles/filedetails/?id=2077186491) for the original graphics and other ship-related code.

### Recommended Companion Mods

[Ringworld Graphical Enhancements](https://steamcommunity.com/sharedfiles/filedetails/?id=2628518102), [Shattered Ring Shipset Fix](https://steamcommunity.com/sharedfiles/filedetails/?id=2566249278), or [Subtle Polish: A Collection of Fixes and Enhancements](https://steamcommunity.com/sharedfiles/filedetails/?id=2522974089) to set your Origin: Shattered Ring empires to have ringworlds matching their shipset (graphical culture), which includes the Machine Shipset.

[Machine Shipset Add-on: Shattered Ring Appearance](https://steamcommunity.com/sharedfiles/filedetails/?id=2628980994) ensures that the permanently-destroyed sections for Origin: Shattered Ring using the Machine Shipset properly display as that shipset.  This mod adds missing graphical definitions to the Machine Shipset.

[Aesthetic Terraform Stations](https://steamcommunity.com/sharedfiles/filedetails/?id=2622411084) will give you back the very old-school terraform stations as visual markers for terraforming planets.

[Machine Shipset Add-on: Aesthetic Terraform Station Compatibility](https://steamcommunity.com/sharedfiles/filedetails/?id=2628972292) this compatibility patch ensures the correct Machine Shipset graphics are used for the above terraform stations.

## Changelog

* 1.0.0 Initial version
* 1.1.0 Mark as compatible with Stellaris version 3.2 "Herbert"
    * Add two additional missing locators

## Source Code

Hosted on [GitHub](https://github.com/corsairmarks/machine_shipset_no_error_logs)

### Development Notes

It is best to clone this repository into `<Stellaris User's Directory>/Paradox Interactive/Stellaris/mod`, and then make a connection to the `mod` folder via a `*.mod` file's `path` property.  That will ensure the game can see the files, and also that CWTools will parse them.  Also note that the README.md file exists in the `mod` directory but is symbolically linked in the root directory.