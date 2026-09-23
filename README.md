# GEARBOX SWITCH [STANDALONE]

<div align="center">
<img src="https://github.com/user-attachments/assets/c5e7b9c4-2ad2-4655-8714-cd474336be60" alt="Thumbnail" width="500px" />
</div>

## DESCRIPTION

Bring authentic manual and sequential transmission dynamics to your FiveM server with the **Gearbox Switch System**. Engineered for both standalone servers and economic roleplay environments, this script introduces 100% manual shifting control, realistic clutch engagement, ignition cutting, rev-matching (punta-tacco), custom interior animations, and immersive 3D audio.

> **NOTE:** Requires GTA V **GameBuild 3095 or higher** and vehicle handlings configured with `CCarHandlingData` in `SubHandlingData` to take full effect.

Featuring custom addon sound effects (`.awc`) attached directly to vehicle entities, responsive clutch physics that disengage power and realistically decelerate the vehicle, dynamic left/right-hand drive shifting animations, and full inventory item integration for mechanics, this resource delivers an unparalleled driving experience.

## KEY FEATURES

### **Realistic Transmission & Clutch Mechanics**
- **100% Manual Shifting**: Completely eliminates unwanted automatic gear shifting when active — every gear upshift and downshift is commanded by the driver.
- **Sequential & H-Pattern Support**: Seamless shifting experience supporting both sequential transmissions (ideal for sports/race cars) and manual gearboxes.
- **Clutch Engagement & Deceleration**: Holding the clutch down disengages the drivetrain, allowing realistic RPM coasting and natural vehicle deceleration.
- **Ignition Cut & Rev-Matching**: Integrated ignition cutting during fast shifts and automated rev-matching (*Punta-Tacco* / Heel-and-Toe) on downshifts.
- **Reverse Gear Calibration**: Smooth, realistic reverse gear acceleration and gear validation avoiding drivetrain lockups.

### **Dual Operating Architecture**
- **Standalone Mode (`'ALONE'`)**: Plug-and-play operation with KVP persistence (global or vehicle-specific), ox_lib keybinds/commands, and zero database requirements.
- **Roleplay Mode (`'RP'`)**: Physical item installation by mechanics, OneSync StateBag synchronization (`hasManualGearbox`), raycast vehicle detection, and framework compatibility.

### **Dynamic Shifting Animations**
- **Custom Shifting Animations**: Custom ped animations for gear shifting (`dking@anim@gear`) for both upshifts and downshifts.
- **Right-Hand Drive (RHD) Support**: Automatic detection and manual fallback for RHD vehicles with dedicated left-hand shifting animations.
- **Transmission-Specific Animations**: Distinct animation styles for sequential shift levers vs. traditional manual shifters.

### **High-Fidelity 3D Positional Audio**
- **Custom Addon Audio**: Built with custom wavepacks (`dking02gearbox.awc` and `dking02gearbox_sounds.dat`) loaded natively into GTA V audio banks.
- **Entity-Attached Sounds**: High-fidelity sound effects for every gear change, clutch engagement, and sequential shift lever click originating directly from the vehicle.

### **Vehicle Compatibility & Control**
- **Customizable Blacklist**: Easily exclude specific vehicle models or classes from gearbox mechanics.
- **Sequential Vehicle List**: Define specific performance cars to automatically operate with sequential transmission characteristics.

## GET NOW

* [DOWNLOAD](https://dking.tebex.io/package/6562197)

## HOW TO INSTALL

1. [Download](https://portal.cfx.re/assets/granted-assets) the script;
2. Place the `dking_gearbox` folder in your server's `resources` directory;
3. Ensure you have `ox_lib` installed and started;
4. Add `ensure dking_gearbox` to your `server.cfg`.

> **Note for RP Mode**: If running `Config.Mode = 'RP'`, ensure entity state bag synchronization is enabled and configure your inventory or mechanic scripts to trigger `UseInstallItem` or `InstallVehicleGearbox`.

## HOW TO USE

### Standalone Mode (`Config.Mode = 'ALONE'`)
- `/gearbox` (or `F10` key) - Toggle manual gearbox mode on or off.
- `LMENU` (Left Alt) - Press and hold clutch pedal.
- `LSHIFT` (Left Shift) - Shift gear up (requires clutch if clutch is enabled, unless vehicle is in sequential mode).
- `LCONTROL` (Left Ctrl) - Shift gear down (requires clutch if clutch is enabled, unless vehicle is in sequential mode).
- *All keybinds can be reconfigured in `config/commands.lua` or individually by players in **Settings > Key Bindings > FiveM**.*

### Roleplay Mode (`Config.Mode = 'RP'`)
1. Mechanics approach the vehicle with the gearbox module item in their inventory;
2. Use the item (`UseInstallItem` export) or execute the installation export in front of the vehicle;
3. Once installed, the vehicle entity receives the replicated StateBag (`hasManualGearbox = true`);
4. The driver can then toggle and utilize manual shifting in that vehicle.

## HANDLING SETUP

To allow the script to take full effect on your custom vehicles, ensure their `handling.meta` contains `CCarHandlingData` inside `<SubHandlingData>`:

```xml
<SubHandlingData>
  <Item type="CCarHandlingData">
  </Item>
  <Item type="NULL" />
  <Item type="NULL" />
</SubHandlingData>
```

## EXPORTS

<details>
  <summary><h2 style="display: inline;">Expand Exports API</h2></summary>

### Client Exports

| Export | Description | Return |
|---|---|---|
| `exports['dking_gearbox']:SetGearboxState(enabled)` | Enables or disables manual gearbox on current vehicle | `boolean` |
| `exports['dking_gearbox']:GetGearboxState()` | Gets current gearbox active state | `boolean` |
| `exports['dking_gearbox']:ToggleGearboxState()` | Toggles manual gearbox state on current vehicle | `boolean` |
| `exports['dking_gearbox']:GetGearboxFullState()` | Returns complete runtime state snapshot | `table` |
| `exports['dking_gearbox']:HasVehicleGearbox([veh])` | Checks if vehicle has manual gearbox module installed | `boolean` |
| `exports['dking_gearbox']:UseInstallItem(data, slot)` | Usable item handler for inventory systems (e.g. ox_inventory) | `boolean` |

### Server Exports

| Export | Description | Return |
|---|---|---|
| `exports['dking_gearbox']:SetPlayerGearboxState(playerId, enabled)` | Enables or disables gearbox for specific player by server ID | `boolean` |
| `exports['dking_gearbox']:InstallVehicleGearbox(vehicleNetId)` | Installs manual gearbox hardware on vehicle entity (StateBag) | `boolean, string` |
| `exports['dking_gearbox']:RemoveVehicleGearbox(vehicleNetId)` | Removes manual gearbox hardware from vehicle entity | `boolean, string` |
| `exports['dking_gearbox']:HasVehicleGearbox(vehicleNetId)` | Checks if vehicle entity has hardware module installed | `boolean` |

</details>

## CONFIGURATION

The resource provides modular configuration files split across `config/`:
- `config/config.lua`: Master settings (`Config.Mode`, `Config.KVPSave`, `Config.ActiveClutch`, `Config.SoundEffects`, and `Config.Blacklist`).
- `config/commands.lua`: Command names, descriptions, ACE permissions, and keybind mappings (`gearbox`, `clutch`, `gearup`, `geardown`).
- `config/animation_config.lua`: Shifting animation durations, sequential cars list (`SequentialCars`), RHD cars list (`RHDCars`), and animation dictionary mappings.
- `config/notifys.lua`: Notification configurations and styling for ox_lib notifications.
- `locales/`: Multi-language dictionary files (`en.lua`, `pt-br.lua`).

## PREVIEW

* [YouTube](https://youtu.be/YmGZNqnDEBM)

## DEPENDENCIES

* GameBuild 3095 or higher
* [ox_lib](https://github.com/overextended/ox_lib)

## SUPPORT

### [Discord](https://discord.gg/Rw6vjcXspG)

## CHANGELOGS

<details>
  <summary><h2 style="display: inline;">Expand Changelogs</h2></summary>

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

  <details>
    <summary style="margin-left: 20px;"><h3 style="display: inline;">1.3.5</h3></summary>
    <ul style="margin-left: 20px;">
      <li>Fixed animations not working.</li>
    </ul>
  </details>

  <details>
    <summary style="margin-left: 20px;"><h3 style="display: inline;">1.3.6</h3></summary>
    <ul style="margin-left: 20px;">
      <li>Changed all sound effects logic.</li>
    </ul>
  </details>

  <details>
    <summary style="margin-left: 20px;"><h3 style="display: inline;">1.3.7</h3></summary>
    <ul style="margin-left: 20px;">
      <li>Completely removed any automatic shifting when the gearbox is activated, now 100% of gear changes are done manually;</li>
      <li>Added ignition cut and rev match (Punta-Tacco) systems;</li>
      <li>Added clutch engagement system, now if you keep the clutch pressed while moving, the car starts to slow down;</li>
      <li>Added a few more improvements and fixes;</li>
      <li>Updated exports.</li>
    </ul>
  </details>

  <details>
    <summary style="margin-left: 20px;"><h3 style="display: inline;">1.3.8</h3></summary>
    <ul style="margin-left: 20px;">
      <li>Added dual operating mode (<code>Config.Mode</code>) supporting Standalone (<code>ALONE</code>) and Roleplay (<code>RP</code>);</li>
      <li>Added vehicle hardware gating via OneSync entity state bags (<code>hasManualGearbox</code>) in RP mode;</li>
      <li>Added item-based gearbox installation support with vehicle raycast detection;</li>
      <li>Added new server and client exports for vehicle transmission management.</li>
    </ul>
  </details>
</details>

# COPYRIGHT

## BY [DKING](https://github.com/Dking07) 2026 ©