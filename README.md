# GEARBOX SWITCH [STANDALONE]

<div align="center">
<img src="https://cdn.discordapp.com/attachments/1295245827039563866/1315387394899574855/Gearbox_Switch_512x512.png?ex=679d18f9&is=679bc779&hm=f7e30c60930e14189181a8435aa89f61a7b40487c3ff98fb87c89b6862b1319a&" width="500px" />
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
<img src="https://cdn.discordapp.com/attachments/1295245827039563866/1315391161757864016/animation_config_512.png?ex=67a7a87b&is=67a656fb&hm=5ef26229bb00ee1574876237fc9a12f28be431f9e0f1d263a51ac0f27c47fcab&" width="400px" />
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