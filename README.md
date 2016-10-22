#REACT TOOLBOX SNIPPETS

Library reference: http://react-toolbox.com/
Detailed port of component documentation: [COMPONENTS](docs/COMPONENTS.MD)

##Getting Started
1. Open VSCode 
2. Open command palette ```CMD + P```
3. Type "ext install react-toolbox-snippets"
4. Restart


##Shortcuts
| Code | Component Represented             | URL
|------|-----------------------------------|-----------------------------------------------------------------------------------------------|
|rt**ab**&rarr;| AppBar | http://react-toolbox.com/#/components/app_bar |
|rt**ac**&rarr;| AutoComplete | http://react-toolbox.com/#/components/autocomplete |
|rt**a**&rarr;| Avatar | http://react-toolbox.com/#/components/avatar |
|rt**b**&rarr;| Button | http://react-toolbox.com/#/components/button |
|rt**ca**&rarr;| Card | http://react-toolbox.com/#/components/card |
|rt**ch**&rarr;| Chip | http://react-toolbox.com/#/components/chip |
|rt**cb**&rarr;| Checkbox | http://react-toolbox.com/#/components/checkbox |
|rt**dp**&rarr;| DatePicker | http://react-toolbox.com/#/components/date_picker |
|rt**di**&rarr;| Dialog | http://react-toolbox.com/#/components/dialog |
|rt**dr**&rarr;| Drawer | http://react-toolbox.com/#/components/drawer |
|rt**dd**&rarr;| DropDown | http://react-toolbox.com/#/components/dropdown|
|rt**fi**&rarr;| Font Icon | http://react-toolbox.com/#/components/font_icon |
|rt**i**&rarr;| Input | http://react-toolbox.com/#/components/input |
|rt**l**&rarr;| Layout | http://react-toolbox.com/#/components/layout |
|rt**li**&rarr;| Link | http://react-toolbox.com/#/components/link |
|rt**m**&rarr;| Menu | http://react-toolbox.com/#/components/menu |
|rt**n**&rarr;| Navigation | http://react-toolbox.com/#/components/navigation |
|rt**pb**&rarr;| Progress Bar | http://react-toolbox.com/#/components/progress_bar |
|rt**rb**&rarr;| Radio Buttons | http://react-toolbox.com/#/components/radio_group |
|rt**r**&rarr;| Ripple | http://react-toolbox.com/#/components/ripple |
|rt**s**&rarr;| Slider | http://react-toolbox.com/#/components/slider |
|rt**sb**&rarr;| SnackBar | http://react-toolbox.com/#/components/snackbar |
|rt**sw**&rarr;| Switch | http://react-toolbox.com/#/components/switch |
|rt**table**&rarr;| Table | http://react-toolbox.com/#/components/table |
|rt**tabs**&rarr;| Tabs | http://react-toolbox.com/#/components/tabs |
|rt**tt**&rarr;| ToolTips | http://react-toolbox.com/#/components/tooltip |
|rt**tp**&rarr;| Time Picker | http://react-toolbox.com/#/components/time_picker |


-------------------------


##Simple Naming Mnemonic
"Simple" = component where name collision doesn't occur in acronym. 

Every key command shortcut is a combination of:  
[1] The library acronym (__in this case, ReactToolbox = rt__)  
[2] The name of the command (__in this case, commands refer to Component names__)

**Example**
```javascript
rtab = React Toolbox App Bar 
```

##Complex Naming Mnemonic 
"Complex" refers to any place where a naming collision occurs.  


###One Letter Collision
In the event of a naming collision (e.g. rtc = React Toolbox CARD or CHIP?), the second letter of the last word shall be appended.
For every collision at nth letter, append a subsequent letter.   
**Example**
```javascript
rtca = React Toolbox Card
rtch = React Toolbox Chip
```

###Two Letter Collision
Append the last letter of the last word in descending alphabetical order  
**Example**
```javascript
rtl = React Toolbox Layout
rtli = React Toolbox Link
rtlis = React Toolbox List
``` 

###Three Letter Collision
Still name collision after 3 letters? Spell out the word.  
**Example**
```javascript
rttable = React Toolbox Table
rttabs = React Toolbox Tabs
```