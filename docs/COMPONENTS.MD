<h1>Detailed</h1>

<h2>Summary</h2>
| Code | Image | 
|:-----|:------|
| <a href="#AppBar">App Bar</a> |  |
| <a href="#AutoComplete">Auto Complete</a> | |
| <a href="#Avatar">Avatar</a> | |
| <a href="#Badge">Badge</a> | |
| <a href="#BottomNavigation">Bottom Navigation</a> | |
| <a href="#Buttons">Buttons</a> | |
| <a href="#FlatButton">Flat Button</a> | |
| <a href="#RaisedButton">Raised Button</a> | |
| <a href="#FloatingActionButton">Floating Action Button</a> | |
| <a href="#IconButton">Icon Button</a> | |
| <a href="#Card">Card</a> | | 
| <a href="#Chip">Chip</a> | |
| <a href="#Date Picker">Date Picker</a> | |
| <a href="#Dialog">Dialog</a> | |
| <a href="#Divider">Divider</a> | |
| <a href="#Drawer">Drawer</a> | |
| <a href="#Grid List">Grid List</a> | |
| <a href="#Icons">Icons</a> | |
| <a href="#FontIcon">Font Icon</a> | |
| <a href="#SVGIcon">SVG Icon</a> | |
| <a href="#List">List</a> | |
| <a href="#Menus">Menus</a> | |
| <a href="#Menu">Menu</a> | |
| <a href="#IconMenu">Icon Menu</a> | |
| <a href="#DropDownMenu">DropDown Menu</a> | |
| <a href="#Paper">Paper</a> | |
| <a href="#Popover">Paper</a> | |
| <a href="#Progress">Progress</a> | |
| <a href="#CircularProgress">Circular Progress</a> | |
| <a href="#LinearProgress">Linear Progress</a> | |
| <a href="#RefreshIndicator">Refresh Indicator</a> | |
| <a href="#SelectField">Select Field</a> | |
| <a href="#Slider">Slider</a> | |
| <a href="#Switches">Switches</a> | |
| <a href="#Checkbox">Checkbox</a> | |
| <a href="#RadioButton">Radio Button</a> | |
| <a href="#Toggle">Toggle</a> | |
| <a href="#Snackbar">Snackbar</a> | |
| <a href="#Stepper">Stepper</a> | |
| <a href="#Subheader">Subheader</a> | |
| <a href="#Table">Table</a> | |
| <a href="#Tabs">Tabs</a> | |
| <a href="#TextField">Text Field</a> | |
| <a href="#TimePicker">Time Picker</a> | |
| <a href="#Toolbar">Toolbar</a> | |

--------
<h2>Code</h2>
<h3 id="AppBar">App Bar</h3>

**Simple Example**
```
import React from 'react';
import AppBar from 'material-ui/AppBar';

/**
 * A simple example of `AppBar` with an icon on the right.
 * By default, the left icon is a navigation-menu.
 */
const AppBarExampleIcon = () => (
  <AppBar
    title="Title"
    iconClassNameRight="muidocs-icon-navigation-expand-more"
  />
);

export default AppBarExampleIcon;

```


**Buttons Example**
```
import React from 'react';
import AppBar from 'material-ui/AppBar';
import IconButton from 'material-ui/IconButton';
import NavigationClose from 'material-ui/svg-icons/navigation/close';
import FlatButton from 'material-ui/FlatButton';

function handleTouchTap() {
  alert('onTouchTap triggered on the title component');
}

const styles = {
  title: {
    cursor: 'pointer',
  },
};

/**
 * This example uses an [IconButton](/#/components/icon-button) on the left, has a clickable `title`
 * through the `onTouchTap` property, and a [FlatButton](/#/components/flat-button) on the right.
 */
const AppBarExampleIconButton = () => (
  <AppBar
    title={<span style={styles.title}>Title</span>}
    onTitleTouchTap={handleTouchTap}
    iconElementLeft={<IconButton><NavigationClose /></IconButton>}
    iconElementRight={<FlatButton label="Save" />}
  />
);

export default AppBarExampleIconButton;
```

**Composition Example**
```
import React, {Component} from 'react';
import AppBar from 'material-ui/AppBar';
import IconButton from 'material-ui/IconButton';
import IconMenu from 'material-ui/IconMenu';
import MenuItem from 'material-ui/MenuItem';
import FlatButton from 'material-ui/FlatButton';
import Toggle from 'material-ui/Toggle';
import MoreVertIcon from 'material-ui/svg-icons/navigation/more-vert';
import NavigationClose from 'material-ui/svg-icons/navigation/close';

class Login extends Component {
  static muiName = 'FlatButton';

  render() {
    return (
      <FlatButton {...this.props} label="Login" />
    );
  }
}

const Logged = (props) => (
  <IconMenu
    {...props}
    iconButtonElement={
      <IconButton><MoreVertIcon /></IconButton>
    }
    targetOrigin={{horizontal: 'right', vertical: 'top'}}
    anchorOrigin={{horizontal: 'right', vertical: 'top'}}
  >
    <MenuItem primaryText="Refresh" />
    <MenuItem primaryText="Help" />
    <MenuItem primaryText="Sign out" />
  </IconMenu>
);

Logged.muiName = 'IconMenu';

/**
 * This example is taking advantage of the composability of the `AppBar`
 * to render different components depending on the application state.
 */
class AppBarExampleComposition extends Component {
  state = {
    logged: true,
  };

  handleChange = (event, logged) => {
    this.setState({logged: logged});
  };

  render() {
    return (
      <div>
        <Toggle
          label="Logged"
          defaultToggled={true}
          onToggle={this.handleChange}
          labelPosition="right"
          style={{margin: 20}}
        />
        <AppBar
          title="Title"
          iconElementLeft={<IconButton><NavigationClose /></IconButton>}
          iconElementRight={this.state.logged ? <Logged /> : <Login />}
        />
      </div>
    );
  }
}

export default AppBarExampleComposition;
```
--------
<h3 id="AutoComplete">AutoComplete</h3>

**Simple Example**
```

```
--------
<h3 id="Avatar">Avatar</h3>
```
import React from 'react';
import Avatar from 'material-ui/Avatar';
import FileFolder from 'material-ui/svg-icons/file/folder';
import FontIcon from 'material-ui/FontIcon';
import List from 'material-ui/List/List';
import ListItem from 'material-ui/List/ListItem';

import {
  blue300,
  indigo900,
  orange200,
  deepOrange300,
  pink400,
  purple500,
} from 'material-ui/styles/colors';

const style = {margin: 5};

/**
 * Examples of `Avatar` using an image, [Font Icon](/#/components/font-icon), [SVG Icon](/#/components/svg-icon)
 * and "Letter" (string), with and without custom colors at the default size (`40dp`) and an alternate size (`30dp`).
 */
const AvatarExampleSimple = () => (
  <List>
    <ListItem
      disabled={true}
      leftAvatar={
        <Avatar src="images/uxceo-128.jpg" />
      }
    >
      Image Avatar
    </ListItem>
    <ListItem
      disabled={true}
      leftAvatar={
        <Avatar
          src="images/uxceo-128.jpg"
          size={30}
          style={style}
        />
      }
    >
      Image Avatar with custom size
    </ListItem>
    <ListItem
      disabled={true}
      leftAvatar={
        <Avatar icon={<FontIcon className="muidocs-icon-communication-voicemail" />} />
      }
    >
      FontIcon Avatar
    </ListItem>
    <ListItem
      disabled={true}
      leftAvatar={
        <Avatar
          icon={<FontIcon className="muidocs-icon-communication-voicemail" />}
          color={blue300}
          backgroundColor={indigo900}
          size={30}
          style={style}
        />
      }
    >
      FontIcon Avatar with custom colors and size
    </ListItem>
    <ListItem
      disabled={true}
      leftAvatar={
        <Avatar icon={<FileFolder />} />
      }
    >
      SvgIcon Avatar
    </ListItem>
    <ListItem
      disabled={true}
      leftAvatar={
        <Avatar
          icon={<FileFolder />}
          color={orange200}
          backgroundColor={pink400}
          size={30}
          style={style}
        />
      }
    >
      SvgIcon Avatar with custom colors and size
    </ListItem>
    <ListItem
      disabled={true}
      leftAvatar={<Avatar>A</Avatar>}
    >
      Letter Avatar
    </ListItem>
    <ListItem
      disabled={true}
      leftAvatar={
        <Avatar
          color={deepOrange300}
          backgroundColor={purple500}
          size={30}
          style={style}
        >
          A
        </Avatar>
      }
    >
      Letter Avatar with custom colors and size
    </ListItem>
  </List>
);

export default AvatarExampleSimple;
```
--------
<h3 id="Badge">Badge</h3>
```

```
--------
<h3 id="BottomNavigation">Bottom Navigation</h3>
```

```
--------

<h3 id="Buttons">Buttons</h3>
```

```
--------
<h4 id="FlatButton">Flat Button</h4>
```

```
<h4>Flat Button</h4>
```

```
<h4>Flat Button</h4>
```

```
<h4>Flat Button</h4>
```

```
--------
<h3 id="Card">Card</h3>
```

```
--------
<h3 id="Chip">Chip</h3>
```

```
--------
<h3 id="DatePicker">Date Picker</h3>
```

```
--------
<h3 id="Dialog">Dialog</h3>
```

```
--------
<h3 id="Divider">Divider</h3>
```

```
--------
<h3 id="Drawer">Drawer</h3>
```

```
--------
<h3 id="GridList">Grid List</h3>
```

```
--------
<h3 id="Icons">Icons</h3>
```

```
--------
<h4 id="FontIcon">Font Icon</h4>
```

```
--------
<h4 id="SVGIcon">SVG Icon</h4>
```

```
--------
<h3 id="List">List</h3>
```

```
--------
<h3 id="Menus">Menus</h3>
```

```
--------
<h4 id="Menu">Menu</h4>
```

```
--------
<h4 id="IconMenu">Icon Menu</h4>
```

```
--------
<h4 id="DropDownMenu">DropDown Menu</h4>
```

```
--------
<h3 id="Paper">Paper</h3>
```

```
--------
<h3 id="Popover">Popover</h3>
```

```
--------
<h3 id="Progress">Progress</h3>
```

```
--------
<h4 id="CircularProgress">Circular Progress</h4>
```

```
--------
<h4 id="LinearProgress">Linear Progress</h4>
```

```
--------
<h4 id="RefreshIndicator">Refresh Indicator</h4>
```

```
--------
<h3 id="SelectField">Select Field</h3>
```

```
--------
<h3 id="Slider">Slider</h3>
```

```
--------
<h3 id="Switches">Switches</h3>
```

```
--------
<h4 id="Checkbox">Checkbox</h4>
```

```
--------
<h4 id="RadioButton">Radio Button</h4>
```

```
--------
<h4 id="Toggle">Toggle</h4>
```

```
--------
<h3 id="Snackbar">Snackbar</h3>
```

```
--------
<h3 id="Stepper">Stepper</h3>
```

```
--------
<h3 id="Subheader">Subheader</h3>
```

```
--------
<h3 id="Table">Table</h3>
```

```
--------
<h3 id="Tabs">Tabs</h3>
```

```
--------
<h3 id="TextField">Text Field</h3>
```

```
--------
<h3 id="TimePicker">Time Picker</h3>
```

```
--------
<h3 id="Toolbar">Toolbar</h3>
```

```
--------
