# GEARBOX SWITCH [STANDALONE]

<div align="center">
<img src="https://github.com/Dking07/fivem-gearbox-switch/blob/main/Gearbox%20Switch.png" width="500px" />
</div>

## DESCRIPTION

### A manual transmission script that adds gear shifting mechanics to FiveM vehicles, with custom animations and sound effects.

## KEY FEATURES

- **Manual Transmission**
  - Seamless switching between automatic and manual transmission
  - Support for both sequential and H-pattern shifting
  - Customizable gear shifting animations
  - High-quality sound effects for each gear change

- **Vehicle-Specific Features**
  - Right-hand drive support with correct animations
  - Sequential transmission support for sports/racing vehicles
  - Customizable vehicle blacklist
  - Different animations for sequential and manual transmissions

- **Rich Sound System**
  - Unique sounds for each gear
  - Separate sound sets for sequential and manual transmissions
  - Adjustable volume controls
  - High-quality audio files

- **Developer-Friendly**
  - Full export system for easy integration
  - Comprehensive configuration options
  - Clean, well-documented code
  - Easy to maintain and extend

## TECHNICAL FEATURES

- Optimized performance with minimal resource usage
- Built-in configuration system
- Customizable key bindings
- Easy installation and setup

## INTEGRATION

- Full exports system for framework integration
- Easy to integrate with inventory systems
- Compatible with most vehicle mods
- Supports both standalone and framework setups

## CONFIGURATION

- Easily customize vehicle lists
- Adjust sound volumes
- Configure key bindings
- Modify animation settings

## GET NOW

* [DOWNLOAD](https://dking.tebex.io/package/6562197)

## HOW TO INSTALL

* [Download](https://keymaster.fivem.net/asset-grants) script;
* Place it in the resources folder;
* Add 'ensure dk_gearbox_switch' (without quotes) to server.cfg.

## HOW TO USE

* Use the '/gearbox' command or bind (both configurable in config.lua) to enable or disable manual gear shifting.
* To switch gears use the 'Shift Gear Up' and 'Shift Gear Down' binds, configurable in: Settings > Key Bindings > GTA Online Vehicles.

## MODIFICATIONS

### To work, you need to modify the handlings that you want the script to take effect on.

* Add CCarHandlingData in the SubHandlingData section, like this:
  ```
  <SubHandlingData>
    <Item type="CCarHandlingData">
    </Item>
    <Item type="NULL" />
    <Item type="NULL" />
  </SubHandlingData>
  ```

## CONFIG
<div align="left">
<img src="https://github.com/Dking07/fivem-gearbox-switch/blob/main/config.png" width="400px" />
</div>

## ANIMATION CONFIG
<div align="left">
<img src="https://github.com/Dking07/fivem-gearbox-switch/blob/main/animation_config.png" width="400px" />
</div>

## PREVIEW

### Coming soon...

## Discord

### [Dking Warehouse](https://discord.gg/Rw6vjcXspG)

## CHANGELOGS

### 1.1

* Added blacklist of vehicle models that will not be affected by the script.

### 1.2

* Added gear shift animation.

### 1.3

* Added manual and sequential shift sound effects;
* Added sequential gear shift animation;
* Added new right hand gear shift animation;
* Added exports for:
  * Toggles the manual gearbox on/off;
  * Enables the manual gearbox;
  * Disables the manual gearbox;
  * Checks if the manual gearbox is currently enabled;
  * Gets the current gear of the vehicle;
  * Manually triggers the gear shift animation;

# COPYRIGHT

## BY [DKING](https://github.com/Dking07) 2025 ©