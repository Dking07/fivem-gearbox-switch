# GEARBOX SWITCH [STANDALONE]

<div align="center">
<img src="https://github.com/user-attachments/assets/c5e7b9c4-2ad2-4655-8714-cd474336be60" width="500px" />
</div>

## DESCRIPTION

Gear shift system that adds clutch or sequential gear shifting mechanics to FiveM, with custom animations and sound effects.

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
- Easy to integrate
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

* [Download](https://portal.cfx.re/assets/granted-assets) script;
* Place it in the resources folder;
* Add 'ensure dking_gearbox' (without quotes) to server.cfg.

## HOW TO USE

* Use the '/gearbox' command or bind (both configurable in config/config.lua) to enable or disable manual gear shifting.
* To switch gears use the binds `clutch` + `GearUp` and `GearDown`, configurable in: Settings > Key Bindings > FiveM.

## MODIFICATIONS

### To work, you need to modify the handlings that you want the script to take effect on.

* Add CCarHandlingData in the SubHandlingData section, like this:
  ```xml
  <SubHandlingData>
    <Item type="CCarHandlingData">
    </Item>
    <Item type="NULL" />
    <Item type="NULL" />
  </SubHandlingData>
  ```

## DEPENDENCIES

* GameBuild 3095 or higher
* [ox_lib](https://github.com/overextended/ox_lib) (Only for notifys)

## Discord

### [Dking Warehouse](https://discord.gg/Rw6vjcXspG)

## CHANGELOGS

<details>
  <summary><h2 style="display: inline;">Expand</h2></summary>

  <details>
    <summary style="margin-left: 20px;"><h3 style="display: inline;">1.1</h3></summary>
    <ul style="margin-left: 20px;">
      <li>Added blacklist of vehicle models that will not be affected by the script.</li>
    </ul>
  </details>

  <details>
    <summary style="margin-left: 20px;"><h3 style="display: inline;">1.2</h3></summary>
    <ul style="margin-left: 20px;">
      <li>Added gear shift animation.</li>
    </ul>
  </details>

  <details>
    <summary style="margin-left: 20px;"><h3 style="display: inline;">1.3</h3></summary>
    <ul style="margin-left: 20px;">
      <li>Added manual and sequential shift sound effects;</li>
      <li>Added sequential gear shift animation;</li>
      <li>Added new right hand gear shift animation;</li>
      <li>Added exports for:</li>
      <details>
        <summary>Exports</summary>
        <ul>
          <li>Toggles the manual gearbox on/off;</li>
          <li>Enables the manual gearbox;</li>
          <li>Disables the manual gearbox;</li>
          <li>Checks if the manual gearbox is currently enabled;</li>
          <li>Gets the current gear of the vehicle;</li>
          <li>Manually triggers the gear shift animation.</li>
        </ul>
      </details>
    </ul>
  </details>

  <details>
    <summary style="margin-left: 20px;"><h3 style="display: inline;">1.3.2</h3></summary>
    <ul style="margin-left: 20px;">
      <li>Fixed animation names.</li>
    </ul>
  </details>

  <details>
    <summary style="margin-left: 20px;"><h3 style="display: inline;">1.3.3</h3></summary>
    <ul style="margin-left: 20px;">
      <li>Various improvements;</li>
      <li>Changed the logic for shifting gears;</li>
      <li>Changed the binds for shifting gears;</li>
      <li>Clutch system added;</li>
      <li>Changes to exports.</li>
    </ul>
  </details>
</details>

# COPYRIGHT

## BY [DKING](https://github.com/Dking07) 2026 ©