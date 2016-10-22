<h1>Material UI Snippets</h2>
Library reference: http://material-ui.com
Detailed Component documentation: [COMPONENTS](docs/COMPONENTS.MD)

<h3>Getting Started</h3>
1. Open VSCode 
2. Open command palette ```CMD + P```
3. Type "ext install react-material-ui-snippets"
4. Restart


<h3>Shortcuts</h3>
| Code | Component Represented             | URL
|------|-----------------------------------|-----------------------------------------------------------------------------------------------|
|mu**ab**&rarr;| AppBar | http://www.material-ui.com/#/components/app_bar |
|mu**ac**&rarr;| AutoComplete | http://www.material-ui.com/#/components/autocomplete |
|mu**a**&rarr;| Avatar | http://www.material-ui.com/#/components/avatar |
|mu**b**&rarr;| Button | http://www.material-ui.com/#/components/button |
|mu**ca**&rarr;| Card | http://www.material-ui.com/#/components/card |
|mu**ch**&rarr;| Chip | http://www.material-ui.com/#/components/chip |
|mu**cb**&rarr;| Checkbox | http://www.material-ui.com/#/components/checkbox |
|mu**dp**&rarr;| DatePicker | http://www.material-ui.com/#/components/date_picker |
|mu**di**&rarr;| Dialog | http://www.material-ui.com/#/components/dialog |
|mu**dr**&rarr;| Drawer | http://www.material-ui.com/#/components/drawer |
|mu**dd**&rarr;| DropDown | http://www.material-ui.com/#/components/dropdown|
|mu**fi**&rarr;| Font Icon | http://www.material-ui.com/#/components/font_icon |
|mu**i**&rarr;| Input | http://www.material-ui.com/#/components/input |
|mu**l**&rarr;| Layout | http://www.material-ui.com/#/components/layout |
|mu**li**&rarr;| Link | http://www.material-ui.com/#/components/link |
|mu**m**&rarr;| Menu | http://www.material-ui.com/#/components/menu |
|mu**n**&rarr;| Navigation | http://www.material-ui.com/#/components/navigation |
|mu**pb**&rarr;| Progress Bar | http://www.material-ui.com/#/components/progress_bar |
|mu**rb**&rarr;| Radio Buttons | http://www.material-ui.com/#/components/radio_group |
|mu**r**&rarr;| Ripple | http://www.material-ui.com/#/components/ripple |
|mu**s**&rarr;| Slider | http://www.material-ui.com/#/components/slider |
|mu**sb**&rarr;| SnackBar | http://www.material-ui.com/#/components/snackbar |
|mu**sw**&rarr;| Switch | http://www.material-ui.com/#/components/switch |
|mu**table**&rarr;| Table | http://www.material-ui.com/#/components/table |
|mu**tabs**&rarr;| Tabs | http://www.material-ui.com/#/components/tabs |
|mu**tt**&rarr;| ToolTips | http://www.material-ui.com/#/components/tooltip |
|mu**tp**&rarr;| Time Picker | http://www.material-ui.com/#/components/time_picker |


-------------------------


##Simple Naming Mnemonic
"Simple" = component where name collision doesn't occur in acronym. 

Every key command shomucut is a combination of:  
[1] The library acronym (__in this case, MaterialUI = mu__)  
[2] The name of the command (__in this case, commands refer to Component names__)

**Example**
```javascript
muab = React Toolbox App Bar 
```

##Complex Naming Mnemonic 
"Complex" refers to any place where a naming collision occurs.  


###One Letter Collision
In the event of a naming collision (e.g. mutc = MaterialUI CARD or CHIP?), the second letter of the last word shall be appended.
For every collision at nth letter, append a subsequent letter.   
**Example**
```javascript
muca = React Toolbox Card
much = React Toolbox Chip
```

###Two Letter Collision
Append the last letter of the last word in descending alphabetical order  
**Example**
```javascript
mul = React Toolbox Layout
muli = React Toolbox Link
mulis = React Toolbox List
``` 

###Three Letter Collision
Still name collision after 3 letters? Spell out the word.  
**Example**
```javascript
mutable = React Toolbox Table
mutabs = React Toolbox Tabs
```