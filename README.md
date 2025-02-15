# GEARBOX SWITCH [STANDALONE]

<div align="center">
<img src="https://github.com/Dking07/fivem-backup/blob/main/My%20Scripts/Gearbox%20Switch/Gearbox%20Switch.png" width="500px" />
</div>

## DESCRIPTION

### Enable manual gear shifting through a command or keybind.

## CHANGES

* Add the 'gearbox' command and a keybind to toggle manual gear shifting on and off with animation.

## GET NOW

* [DOWNLOAD](https://dking.tebex.io/package/6575155)

## HOW TO INSTALL

* [Download](https://keymaster.fivem.net/asset-grants) script;
* Place it in the resources folder;
* Add 'ensure dk_gearbox_switch' (without quotes) to server.cfg.

## HOW TO USE

* Use the '/gearbox' command or the keybind (configurable in the FiveM keybinds section) to toggle manual gear shifting on or off.
* To use manual gear shifting, use the 'Shift Gear Up' and 'Shift Gear Down' keybinds, configurable in Settings > Key Bindings > GTA Online Vehicles.

### To work, you need to modify the handlings that you want the script to take effect on.

### Modifications

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
<img src="https://cdn.discordapp.com/attachments/1295245827039563866/1315391152194584596/config_512.png?ex=679d1c79&is=679bcaf9&hm=a2eb12b807dab018fad88ca56492fd670c95576a5fa8672807350a147f07ed93&" width="400px" />
</div>

## ANIMATION CONFIG
<div align="left">
<img src="https://github.com/Dking07/fivem-backup/blob/main/My%20Scripts/Gearbox%20Switch/animation_config.png" width="400px" />
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

# COPYRIGHT

## BY [DKING](https://github.com/Dking07) 2025 ©