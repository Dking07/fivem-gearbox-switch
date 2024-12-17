# GEARBOX SWITCH [STANDALONE]
![](https://cdn.discordapp.com/attachments/1295245827039563866/1315387394899574855/Gearbox_Switch_512x512.png?ex=67573979&is=6755e7f9&hm=001e50da835a8c92ebd9016f2a4912c18eee3e8f4527f021a30c1723aba80d2d&)
## DESCRIPTION

### Enable manual gear shifting through a command or keybind.

## CHANGES

* Add the 'gearbox' command and a keybind to toggle manual gear shifting on and off with animation.

## GET NOW

* [DOWNLOAD](https://dking.tebex.io/package/6562197)

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
![](https://media.discordapp.net/attachments/1295245827039563866/1315391152194584596/config_512.png?ex=676271b9&is=67612039&hm=66305cc0f11180d0eb2bef042a6aeb1647e62fa28f243f07983c845d899c1a3d&=&format=webp&quality=lossless&width=463&height=540)

## ANIMATION CONFIG
![](https://cdn.discordapp.com/attachments/1295245827039563866/1315391161757864016/animation_config_512.png?ex=67573cfb&is=6755eb7b&hm=d83d5255c40d3eb41c5a2bd0297a49041ae0950dde9069f8889fe8e6c104bf05&)

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

## BY [DKING](https://github.com/Dking07) 2024 ©
