<h1>Material UI Snippets</h2>
Found myself using material-ui more than react-toolbox, so forked my other snippet extension.

-----------

<h3>Getting Started</h3>
1. Open VSCode 
2. Open command palette ```CMD + P```
3. Type "ext install react-material-ui-snippets"
4. Restart


<h3>Shortcuts</h3>
| Code | Component Represented             | URL
|------|-----------------------------------|-----------------------------------------------------------------------------------------------|
|mu**ab**&rarr;| AppBar | [http://www.material-ui.com/#/components/app-bar](http://www.material-ui.com/#/components/app-bar) |
|mu**ac**&rarr;| AutoComplete | [http://www.material-ui.com/#/components/auto-complete](http://www.material-ui.com/#/components/auto-complete) |
|mu**a**&rarr;| Avatar | [http://www.material-ui.com/#/components/avatar](http://www.material-ui.com/#/components/avatar) |
|mu**b**&rarr;| Button | [http://www.material-ui.com/#/components/button](http://www.material-ui.com/#/components/button) |
|mu**ca**&rarr;| Card | [http://www.material-ui.com/#/components/card](http://www.material-ui.com/#/components/card) |
|mu**ch**&rarr;| Chip | [http://www.material-ui.com/#/components/chip](http://www.material-ui.com/#/components/chip) |
|mu**cb**&rarr;| Checkbox | [http://www.material-ui.com/#/components/checkbox](http://www.material-ui.com/#/components/checkbox) |
|mu**dp**&rarr;| DatePicker | [http://www.material-ui.com/#/components/date-picker](http://www.material-ui.com/#/components/date-picker) |
|mu**di**&rarr;| Dialog | [http://www.material-ui.com/#/components/dialog](http://www.material-ui.com/#/components/dialog) |
|mu**dr**&rarr;| Drawer | [http://www.material-ui.com/#/components/drawer](http://www.material-ui.com/#/components/drawer) |
|mu**fi**&rarr;| Font Icon | [http://www.material-ui.com/#/components/font-icon](http://www.material-ui.com/#/components/font-icon) |
|mu**m**&rarr;| Menu | [http://www.material-ui.com/#/components/menu](http://www.material-ui.com/#/components/menu) |
|mu**s**&rarr;| Slider | [http://www.material-ui.com/#/components/slider](http://www.material-ui.com/#/components/slider) |
|mu**sb**&rarr;| SnackBar | [http://www.material-ui.com/#/components/snackbar](http://www.material-ui.com/#/components/snackbar) |
|mu**table**&rarr;| Table | [http://www.material-ui.com/#/components/table](http://www.material-ui.com/#/components/table) |
|mu**tabs**&rarr;| Tabs | [http://www.material-ui.com/#/components/tabs](http://www.material-ui.com/#/components/tabs) |
|mu**tp**&rarr;| Time Picker | [http://www.material-ui.com/#/components/time-picker](http://www.material-ui.com/#/components/time-picker) |


<h3>Quick Ref</h3> 
<h4>External URI</h4>
Library reference: http://material-ui.com

<h4>Docs</h4>
* `Component breakdown`: [COMPONENTS](docs/COMPONENTS.MD)
* `Extension build`: [BUILD](docs/BUILD.MD)

-------------------------


<h4>Simple Naming Mnemonic
"Simple" = component where name collision doesn't occur in acronym. 

Every key command shomucut is a combination of:  
[1] The library acronym (__in this case, MaterialUI = mu__)  
[2] The name of the command (__in this case, commands refer to Component names__)

**Example**
```javascript
muab = Material UI App Bar 
```

<h4>Complex Naming Mnemonic 
"Complex" refers to any place where a naming collision occurs.  


<h5>One Letter Collision
In the event of a naming collision (e.g. mutc = MaterialUI CARD or CHIP?), the second letter of the last word shall be appended.
For every collision at nth letter, append a subsequent letter.   
**Example**
```javascript
muca = Material UI Card
much = Material UI Chip
```

<h5>Two Letter Collision
Append the last letter of the last word in descending alphabetical order  
**Example**
```javascript
mul = Material UI Layout
muli = Material UI Link
mulis = Material UI List
``` 

<h5>Three Letter Collision
Still name collision after 3 letters? Spell out the word.  
**Example**
```javascript
mutable = Material UI Table
mutabs = Material UI Tabs
```