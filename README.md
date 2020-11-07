# OpenHAB2 Widget for Übersicht
This is a small widget für Übersicht where you can have an overview of your openHAB 2 installation on your desktop.

## Preparation
- you need a complete [openHAB 2](https://www.openhab.org/) installation with REST API enabled (which is usually the case).
- you downloaded and installed [Übersicht](http://tracesof.net/uebersicht/)

## Installation
- Copy `openHAB2.widget` to your widgets folder
- Add your openHAB 2 ip to `openHAB2.coffee`

## Advanced

### Refresh Frequency
By default, the widget will update the states every 3 minutes. To adjust this, change the value of `refreshFrequency` in `openHAB2.coffee`. The value should be in milliseconds, so multiply the number of seconds by 1000.

### Itemselection
Add all items that should be displayed in the `items` array in `openHAB2.coffee`.
Every item needs 2 values: 
- name: the itemname in openHAB 2
- type: one of the supported types. I added some types for a better user experience.  
Special type Room: All followed items till the next room are assigned to this room and will be displayed in one column (more information in the section Columns)  
Supportet itemtypes: Switch, Contact, Light (openHAB2 type: Switch), Led-Strip (openHAB2 type: Switch), Dimmer, Rollershutter, Color, DateTime, Location,  Player, String ,Number (openHAB2 type: String), Temperature (openHAB2 type: String), Humidity (openHAB2 type: String), Heating (openHAB2 type: Switch)

### Options for some Itemtypes
- Dimmer: the number of decimal places can be defined by changing the value of `dimmer_decimalplaces` in `openHAB2.coffee`
- Number: the number of decimal places can be defined by changing the value of `number_decimalplaces` in `openHAB2.coffee`
- Temperature: the unit can be defined by changing the value of `--unit_temperature` that can be found in the `style block` in `openHAB2.coffee`

### Appearance

#### Columns
The number of columns can be defined by changing the value of `columns` in `openHAB2.coffee`. A column will only contain one room apart from the last column which contains the rest ot the rooms.
The width of each columns can be defined by changing the value of `width_of_column` in `openHAB2.coffee`.

#### Icons
At the beginning of every coloumn which contains an item, a icon can be displayed that shows the type. Some types support an icon that adapts to the state of the item (e.g. Switch). Icons are enabled from the start, but can be disabled by changing the value of `icons` to false in `openHAB2.coffee`.

#### Position
The position of the widget can be set in the `style block` in `openHAB2.coffee`. 

#### Advanced Appearance
Several options like the text, background or icon color as well as a border can be set in the `style block` in `openHAB2.coffee` by changing the css variables. A description can be found next to the variables.

##Credits
This is not an official openHAB2 widget.  
Please use the issue templates in this repository for bugs. The main openHAB project is not responsible for any malfunction that is caused by the use of the widget!  
Special thanks goes to [badsgahhl](https://github.com/badsgahhl)
