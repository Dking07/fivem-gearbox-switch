# DKING GEARBOX SWITCH

![](https://cdn.discordapp.com/attachments/1295245827039563866/1295245935198212156/Gearbox_Switch.png?ex=670df347&is=670ca1c7&hm=e85becd87f5147e5914d958450b60e71cada6fe3ebe122b8e0f8d7994e882452&)

## DESCRIPTION

### Enable manual gear shifting through a command or keybind.

## CHANGES

* Add the 'gearbox' command and a keybind to toggle manual gear shifting on and off.

## PURCHASE

* [TEBEX](https://dking.tebex.io/package/6498306)

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

## PREVIEW

### Coming soon...

## Discord

### [Dking Warehouse](https://discord.gg/Rw6vjcXspG)

# COPYRIGHT

## BY [DKING](https://github.com/Dking07) 2024 ©
