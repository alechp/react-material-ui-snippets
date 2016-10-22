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
--------
<h3 id="AutoComplete">AutoComplete</h3>
```
import React from 'react';
import AutoComplete from 'material-ui/AutoComplete';

export default class AutoCompleteExampleSimple extends React.Component {

  constructor(props) {
    super(props);

    this.state = {
      dataSource: [],
    };
  }

  handleUpdateInput = (value) => {
    this.setState({
      dataSource: [
        value,
        value + value,
        value + value + value,
      ],
    });
  };

  render() {
    return (
      <div>
        <AutoComplete
          hintText="Type anything"
          dataSource={this.state.dataSource}
          onUpdateInput={this.handleUpdateInput}
        />
        <AutoComplete
          hintText="Type anything"
          dataSource={this.state.dataSource}
          onUpdateInput={this.handleUpdateInput}
          floatingLabelText="Full width"
          fullWidth={true}
        />
      </div>
    );
  }
}
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
import React from 'react';
import Badge from 'material-ui/Badge';
import IconButton from 'material-ui/IconButton';
import NotificationsIcon from 'material-ui/svg-icons/social/notifications';

const BadgeExampleSimple = () => (
  <div>
    <Badge
      badgeContent={4}
      primary={true}
    >
      <NotificationsIcon />
    </Badge>
    <Badge
      badgeContent={10}
      secondary={true}
      badgeStyle={{top: 12, right: 12}}
    >
      <IconButton tooltip="Notifications">
        <NotificationsIcon />
      </IconButton>
    </Badge>
  </div>
);

export default BadgeExampleSimple;
```
--------
<h3 id="BottomNavigation">Bottom Navigation</h3>
```
import React, {Component} from 'react';
import FontIcon from 'material-ui/FontIcon';
import {BottomNavigation, BottomNavigationItem} from 'material-ui/BottomNavigation';
import Paper from 'material-ui/Paper';
import IconLocationOn from 'material-ui/svg-icons/communication/location-on';

const recentsIcon = <FontIcon className="material-icons">restore</FontIcon>;
const favoritesIcon = <FontIcon className="material-icons">favorite</FontIcon>;
const nearbyIcon = <IconLocationOn />;

/**
 * A simple example of `BottomNavigation`, with three labels and icons
 * provided. The selected `BottomNavigationItem` is determined by application
 * state (for instance, by the URL).
 */
class BottomNavigationExampleSimple extends Component {
  state = {
    selectedIndex: 0,
  };

  select = (index) => this.setState({selectedIndex: index});

  render() {
    return (
      <Paper zDepth={1}>
        <BottomNavigation selectedIndex={this.state.selectedIndex}>
          <BottomNavigationItem
            label="Recents"
            icon={recentsIcon}
            onTouchTap={() => this.select(0)}
          />
          <BottomNavigationItem
            label="Favorites"
            icon={favoritesIcon}
            onTouchTap={() => this.select(1)}
          />
          <BottomNavigationItem
            label="Nearby"
            icon={nearbyIcon}
            onTouchTap={() => this.select(2)}
          />
        </BottomNavigation>
      </Paper>
    );
  }
}

export default BottomNavigationExampleSimple;
```
--------

<h3 id="Buttons">Buttons</h3>
--------
<h4 id="FlatButton">Flat Button</h4>
```
import React from 'react';
import FlatButton from 'material-ui/FlatButton';

const FlatButtonExampleSimple = () => (
  <div>
    <FlatButton label="Default" />
    <FlatButton label="Primary" primary={true} />
    <FlatButton label="Secondary" secondary={true} />
    <FlatButton label="Disabled" disabled={true} />
  </div>
);

export default FlatButtonExampleSimple;
```
<h4>Flat Button</h4>
```
import React from 'react';
import RaisedButton from 'material-ui/RaisedButton';

const style = {
  margin: 12,
};

const RaisedButtonExampleSimple = () => (
  <div>
    <RaisedButton label="Default" style={style} />
    <RaisedButton label="Primary" primary={true} style={style} />
    <RaisedButton label="Secondary" secondary={true} style={style} />
    <RaisedButton label="Disabled" disabled={true} style={style} />
    <br />
    <br />
    <RaisedButton label="Full width" fullWidth={true} />
  </div>
);

export default RaisedButtonExampleSimple;
```
<h4>Floating Action Button</h4>
```
import React from 'react';
import FloatingActionButton from 'material-ui/FloatingActionButton';
import ContentAdd from 'material-ui/svg-icons/content/add';

const style = {
  marginRight: 20,
};

const FloatingActionButtonExampleSimple = () => (
  <div>
    <FloatingActionButton style={style}>
      <ContentAdd />
    </FloatingActionButton>

    <FloatingActionButton mini={true} style={style}>
      <ContentAdd />
    </FloatingActionButton>

    <FloatingActionButton secondary={true} style={style}>
      <ContentAdd />
    </FloatingActionButton>

    <FloatingActionButton mini={true} secondary={true} style={style}>
      <ContentAdd />
    </FloatingActionButton>

    <FloatingActionButton disabled={true} style={style}>
      <ContentAdd />
    </FloatingActionButton>

    <FloatingActionButton mini={true} disabled={true} style={style}>
      <ContentAdd />
    </FloatingActionButton>
  </div>
);

export default FloatingActionButtonExampleSimple;
```
<h4>Icon Button</h4>
```
import React from 'react';
import IconButton from 'material-ui/IconButton';

const IconButtonExampleSimple = () => (
  <div>
    <IconButton iconClassName="muidocs-icon-custom-github" />
    <IconButton iconClassName="muidocs-icon-custom-github" disabled={true} />
  </div>
);

export default IconButtonExampleSimple;
```
--------
<h3 id="Card">Card</h3>
```
import React from 'react';
import {Card, CardActions, CardHeader, CardMedia, CardTitle, CardText} from 'material-ui/Card';
import FlatButton from 'material-ui/FlatButton';

const CardExampleWithAvatar = () => (
  <Card>
    <CardHeader
      title="URL Avatar"
      subtitle="Subtitle"
      avatar="images/jsa-128.jpg"
    />
    <CardMedia
      overlay={<CardTitle title="Overlay title" subtitle="Overlay subtitle" />}
    >
      <img src="images/nature-600-337.jpg" />
    </CardMedia>
    <CardTitle title="Card title" subtitle="Card subtitle" />
    <CardText>
      Lorem ipsum dolor sit amet, consectetur adipiscing elit.
      Donec mattis pretium massa. Aliquam erat volutpat. Nulla facilisi.
      Donec vulputate interdum sollicitudin. Nunc lacinia auctor quam sed pellentesque.
      Aliquam dui mauris, mattis quis lacus id, pellentesque lobortis odio.
    </CardText>
    <CardActions>
      <FlatButton label="Action1" />
      <FlatButton label="Action2" />
    </CardActions>
  </Card>
);

export default CardExampleWithAvatar;
```
--------
<h3 id="Chip">Chip</h3>
```
import React from 'react';
import Avatar from 'material-ui/Avatar';
import Chip from 'material-ui/Chip';
import FontIcon from 'material-ui/FontIcon';
import SvgIconFace from 'material-ui/svg-icons/action/face';
import {blue300, indigo900} from 'material-ui/styles/colors';

const styles = {
  chip: {
    margin: 4,
  },
  wrapper: {
    display: 'flex',
    flexWrap: 'wrap',
  },
};

function handleRequestDelete() {
  alert('You clicked the delete button.');
}

function handleTouchTap() {
  alert('You clicked the Chip.');
}

/**
 * Examples of Chips, using an image [Avatar](/#/components/font-icon), [Font Icon](/#/components/font-icon) Avatar,
 * [SVG Icon](/#/components/svg-icon) Avatar, "Letter" (string) Avatar, and with custom colors.
 *
 * Chips with the `onRequestDelete` property defined will display a delete icon.
 */
export default class ChipExampleSimple extends React.Component {

  render() {
    return (
      <div style={styles.wrapper}>

        <Chip
          style={styles.chip}
        >
          Text Chip
        </Chip>

        <Chip
          onRequestDelete={handleRequestDelete}
          onTouchTap={handleTouchTap}
          style={styles.chip}
        >
          Deletable Text Chip
        </Chip>

        <Chip
          onTouchTap={handleTouchTap}
          style={styles.chip}
        >
          <Avatar src="images/uxceo-128.jpg" />
          Image Avatar Chip
        </Chip>

        <Chip
          onRequestDelete={handleRequestDelete}
          onTouchTap={handleTouchTap}
          style={styles.chip}
        >
          <Avatar src="images/ok-128.jpg" />
          Deletable Avatar Chip
        </Chip>

        <Chip
          onTouchTap={handleTouchTap}
          style={styles.chip}
        >
          <Avatar icon={<FontIcon className="material-icons">perm_identity</FontIcon>} />
          FontIcon Avatar Chip
        </Chip>

        <Chip
          onRequestDelete={handleRequestDelete}
          onTouchTap={handleTouchTap}
          style={styles.chip}
        >
          <Avatar color="#444" icon={<SvgIconFace />} />
          SvgIcon Avatar Chip
        </Chip>

        <Chip onTouchTap={handleTouchTap} style={styles.chip}>
          <Avatar size={32}>A</Avatar>
          Text Avatar Chip
        </Chip>

        <Chip
          backgroundColor={blue300}
          onRequestDelete={handleRequestDelete}
          onTouchTap={handleTouchTap}
          style={styles.chip}
        >
          <Avatar size={32} color={blue300} backgroundColor={indigo900}>
            MB
          </Avatar>
          Colored Chip
        </Chip>
      </div>
    );
  }
}
```
--------
<h3 id="DatePicker">Date Picker</h3>
```
import React from 'react';
import DatePicker from 'material-ui/DatePicker';

/**
 * The Date Picker defaults to a portrait dialog. The `mode` property can be set to `landscape`.
 * You can also disable the Dialog passing `true` to the `disabled` property.
 */
const DatePickerExampleSimple = () => (
  <div>
    <DatePicker hintText="Portrait Dialog" />
    <DatePicker hintText="Landscape Dialog" mode="landscape" />
    <DatePicker hintText="Dialog Disabled" disabled={true} />
  </div>
);

export default DatePickerExampleSimple;
```
--------
<h3 id="Dialog">Dialog</h3>
```
import React from 'react';
import Dialog from 'material-ui/Dialog';
import FlatButton from 'material-ui/FlatButton';
import RaisedButton from 'material-ui/RaisedButton';

/**
 * Dialog with action buttons. The actions are passed in as an array of React objects,
 * in this example [FlatButtons](/#/components/flat-button).
 *
 * You can also close this dialog by clicking outside the dialog, or with the 'Esc' key.
 */
export default class DialogExampleSimple extends React.Component {
  state = {
    open: false,
  };

  handleOpen = () => {
    this.setState({open: true});
  };

  handleClose = () => {
    this.setState({open: false});
  };

  render() {
    const actions = [
      <FlatButton
        label="Cancel"
        primary={true}
        onTouchTap={this.handleClose}
      />,
      <FlatButton
        label="Submit"
        primary={true}
        keyboardFocused={true}
        onTouchTap={this.handleClose}
      />,
    ];

    return (
      <div>
        <RaisedButton label="Dialog" onTouchTap={this.handleOpen} />
        <Dialog
          title="Dialog With Actions"
          actions={actions}
          modal={false}
          open={this.state.open}
          onRequestClose={this.handleClose}
        >
          The actions in this window were passed in as an array of React objects.
        </Dialog>
      </div>
    );
  }
}
```
--------
<h3 id="Divider">Divider</h3>
```
import React from 'react';
import Divider from 'material-ui/Divider';
import Paper from 'material-ui/Paper';
import TextField from 'material-ui/TextField';

const style = {
  marginLeft: 20,
};

const DividerExampleForm = () => (
  <Paper zDepth={2}>
    <TextField hintText="First name" style={style} underlineShow={false} />
    <Divider />
    <TextField hintText="Middle name" style={style} underlineShow={false} />
    <Divider />
    <TextField hintText="Last name" style={style} underlineShow={false} />
    <Divider />
    <TextField hintText="Email address" style={style} underlineShow={false} />
    <Divider />
  </Paper>
);

export default DividerExampleForm;
```
--------
<h3 id="Drawer">Drawer</h3>
```
import React from 'react';
import Drawer from 'material-ui/Drawer';
import MenuItem from 'material-ui/MenuItem';
import RaisedButton from 'material-ui/RaisedButton';

export default class DrawerSimpleExample extends React.Component {

  constructor(props) {
    super(props);
    this.state = {open: false};
  }

  handleToggle = () => this.setState({open: !this.state.open});

  render() {
    return (
      <div>
        <RaisedButton
          label="Toggle Drawer"
          onTouchTap={this.handleToggle}
        />
        <Drawer open={this.state.open}>
          <MenuItem>Menu Item</MenuItem>
          <MenuItem>Menu Item 2</MenuItem>
        </Drawer>
      </div>
    );
  }
}
```
--------
<h3 id="GridList">Grid List</h3>
```
Hide source
import React from 'react';
import {GridList, GridTile} from 'material-ui/GridList';
import IconButton from 'material-ui/IconButton';
import Subheader from 'material-ui/Subheader';
import StarBorder from 'material-ui/svg-icons/toggle/star-border';

const styles = {
  root: {
    display: 'flex',
    flexWrap: 'wrap',
    justifyContent: 'space-around',
  },
  gridList: {
    width: 500,
    height: 450,
    overflowY: 'auto',
  },
};

const tilesData = [
  {
    img: 'images/grid-list/00-52-29-429_640.jpg',
    title: 'Breakfast',
    author: 'jill111',
  },
  {
    img: 'images/grid-list/burger-827309_640.jpg',
    title: 'Tasty burger',
    author: 'pashminu',
  },
  {
    img: 'images/grid-list/camera-813814_640.jpg',
    title: 'Camera',
    author: 'Danson67',
  },
  {
    img: 'images/grid-list/morning-819362_640.jpg',
    title: 'Morning',
    author: 'fancycrave1',
  },
  {
    img: 'images/grid-list/hats-829509_640.jpg',
    title: 'Hats',
    author: 'Hans',
  },
  {
    img: 'images/grid-list/honey-823614_640.jpg',
    title: 'Honey',
    author: 'fancycravel',
  },
  {
    img: 'images/grid-list/vegetables-790022_640.jpg',
    title: 'Vegetables',
    author: 'jill111',
  },
  {
    img: 'images/grid-list/water-plant-821293_640.jpg',
    title: 'Water plant',
    author: 'BkrmadtyaKarki',
  },
];

/**
 * A simple example of a scrollable `GridList` containing a [Subheader](/#/components/subheader).
 */
const GridListExampleSimple = () => (
  <div style={styles.root}>
    <GridList
      cellHeight={180}
      style={styles.gridList}
    >
      <Subheader>December</Subheader>
      {tilesData.map((tile) => (
        <GridTile
          key={tile.img}
          title={tile.title}
          subtitle={<span>by <b>{tile.author}</b></span>}
          actionIcon={<IconButton><StarBorder color="white" /></IconButton>}
        >
          <img src={tile.img} />
        </GridTile>
      ))}
    </GridList>
  </div>
);

export default GridListExampleSimple;
```
--------
<h3 id="Icons">Icons</h3>
--------
<h4 id="FontIcon">Font Icon</h4>
```
import React from 'react';
import FontIcon from 'material-ui/FontIcon';
import {blue500, red500, greenA200} from 'material-ui/styles/colors';

const iconStyles = {
  marginRight: 24,
};

const FontIconExampleSimple = () => (
  <div>
    <FontIcon
      className="muidocs-icon-action-home"
      style={iconStyles}
    />

    <FontIcon
      className="muidocs-icon-action-home"
      style={iconStyles}
      color={blue500}
    />

    <FontIcon
      className="muidocs-icon-action-home"
      style={iconStyles}
      color={red500}
      hoverColor={greenA200}
    />
  </div>
);

export default FontIconExampleSimple;
```
--------
<h4 id="SVGIcon">SVG Icon</h4>
```
import React from 'react';
import {blue500, red500, greenA200} from 'material-ui/styles/colors';
import SvgIcon from 'material-ui/SvgIcon';

const iconStyles = {
  marginRight: 24,
};

const HomeIcon = (props) => (
  <SvgIcon {...props}>
    <path d="M10 20v-6h4v6h5v-8h3L12 3 2 12h3v8z" />
  </SvgIcon>
);

const SvgIconExampleSimple = () => (
  <div>
    <HomeIcon style={iconStyles} />
    <HomeIcon style={iconStyles} color={blue500} />
    <HomeIcon style={iconStyles} color={red500} hoverColor={greenA200} />
  </div>
);

export default SvgIconExampleSimple;
```
--------
<h3 id="List">List</h3>
```
import React from 'react';
import MobileTearSheet from '../../../MobileTearSheet';
import {List, ListItem} from 'material-ui/List';
import ContentInbox from 'material-ui/svg-icons/content/inbox';
import ActionGrade from 'material-ui/svg-icons/action/grade';
import ContentSend from 'material-ui/svg-icons/content/send';
import ContentDrafts from 'material-ui/svg-icons/content/drafts';
import Divider from 'material-ui/Divider';
import ActionInfo from 'material-ui/svg-icons/action/info';

const ListExampleSimple = () => (
  <MobileTearSheet>
    <List>
      <ListItem primaryText="Inbox" leftIcon={<ContentInbox />} />
      <ListItem primaryText="Starred" leftIcon={<ActionGrade />} />
      <ListItem primaryText="Sent mail" leftIcon={<ContentSend />} />
      <ListItem primaryText="Drafts" leftIcon={<ContentDrafts />} />
      <ListItem primaryText="Inbox" leftIcon={<ContentInbox />} />
    </List>
    <Divider />
    <List>
      <ListItem primaryText="All mail" rightIcon={<ActionInfo />} />
      <ListItem primaryText="Trash" rightIcon={<ActionInfo />} />
      <ListItem primaryText="Spam" rightIcon={<ActionInfo />} />
      <ListItem primaryText="Follow up" rightIcon={<ActionInfo />} />
    </List>
  </MobileTearSheet>
);

export default ListExampleSimple;
```
--------
<h3 id="Menus">Menus</h3>
--------
<h4 id="Menu">Menu</h4>
```
import React from 'react';
import Paper from 'material-ui/Paper';
import Menu from 'material-ui/Menu';
import MenuItem from 'material-ui/MenuItem';

const style = {
  display: 'inline-block',
  margin: '16px 32px 16px 0',
};

const MenuExampleSimple = () => (
  <div>
    <Paper style={style}>
      <Menu>
        <MenuItem primaryText="Maps" />
        <MenuItem primaryText="Books" />
        <MenuItem primaryText="Flights" />
        <MenuItem primaryText="Apps" />
      </Menu>
    </Paper>
    <Paper style={style}>
      <Menu>
        <MenuItem primaryText="Refresh" />
        <MenuItem primaryText="Help &amp; feedback" />
        <MenuItem primaryText="Settings" />
        <MenuItem primaryText="Sign out" />
      </Menu>
    </Paper>
  </div>
);

export default MenuExampleSimple;
```
--------
<h4 id="IconMenu">Icon Menu</h4>
```
import React from 'react';
import IconMenu from 'material-ui/IconMenu';
import MenuItem from 'material-ui/MenuItem';
import IconButton from 'material-ui/IconButton';
import MoreVertIcon from 'material-ui/svg-icons/navigation/more-vert';

/**
 * Simple Icon Menus demonstrating some of the layouts possible using the `anchorOrigin` and
 * `targetOrigin` properties.
 */
const IconMenuExampleSimple = () => (
  <div>
    <IconMenu
      iconButtonElement={<IconButton><MoreVertIcon /></IconButton>}
      anchorOrigin={{horizontal: 'left', vertical: 'top'}}
      targetOrigin={{horizontal: 'left', vertical: 'top'}}
    >
      <MenuItem primaryText="Refresh" />
      <MenuItem primaryText="Send feedback" />
      <MenuItem primaryText="Settings" />
      <MenuItem primaryText="Help" />
      <MenuItem primaryText="Sign out" />
    </IconMenu>
    <IconMenu
      iconButtonElement={<IconButton><MoreVertIcon /></IconButton>}
      anchorOrigin={{horizontal: 'left', vertical: 'bottom'}}
      targetOrigin={{horizontal: 'left', vertical: 'bottom'}}
    >
      <MenuItem primaryText="Refresh" />
      <MenuItem primaryText="Send feedback" />
      <MenuItem primaryText="Settings" />
      <MenuItem primaryText="Help" />
      <MenuItem primaryText="Sign out" />
    </IconMenu>
    <IconMenu
      iconButtonElement={<IconButton><MoreVertIcon /></IconButton>}
      anchorOrigin={{horizontal: 'right', vertical: 'bottom'}}
      targetOrigin={{horizontal: 'right', vertical: 'bottom'}}
    >
      <MenuItem primaryText="Refresh" />
      <MenuItem primaryText="Send feedback" />
      <MenuItem primaryText="Settings" />
      <MenuItem primaryText="Help" />
      <MenuItem primaryText="Sign out" />
    </IconMenu>
    <IconMenu
      iconButtonElement={<IconButton><MoreVertIcon /></IconButton>}
      anchorOrigin={{horizontal: 'right', vertical: 'top'}}
      targetOrigin={{horizontal: 'right', vertical: 'top'}}
    >
      <MenuItem primaryText="Refresh" />
      <MenuItem primaryText="Send feedback" />
      <MenuItem primaryText="Settings" />
      <MenuItem primaryText="Help" />
      <MenuItem primaryText="Sign out" />
    </IconMenu>
  </div>
);

export default IconMenuExampleSimple;
```
--------
<h4 id="DropDownMenu">DropDown Menu</h4>
```
import React from 'react';
import DropDownMenu from 'material-ui/DropDownMenu';
import MenuItem from 'material-ui/MenuItem';

const styles = {
  customWidth: {
    width: 200,
  },
};

export default class DropDownMenuSimpleExample extends React.Component {

  constructor(props) {
    super(props);
    this.state = {value: 1};
  }

  handleChange = (event, index, value) => this.setState({value});

  render() {
    return (
      <div>
        <DropDownMenu value={this.state.value} onChange={this.handleChange}>
          <MenuItem value={1} primaryText="Never" />
          <MenuItem value={2} primaryText="Every Night" />
          <MenuItem value={3} primaryText="Weeknights" />
          <MenuItem value={4} primaryText="Weekends" />
          <MenuItem value={5} primaryText="Weekly" />
        </DropDownMenu>
        <br />
        <DropDownMenu
          value={this.state.value}
          onChange={this.handleChange}
          style={styles.customWidth}
          autoWidth={false}
        >
          <MenuItem value={1} primaryText="Custom width" />
          <MenuItem value={2} primaryText="Every Night" />
          <MenuItem value={3} primaryText="Weeknights" />
          <MenuItem value={4} primaryText="Weekends" />
          <MenuItem value={5} primaryText="Weekly" />
        </DropDownMenu>
      </div>
    );
  }
}
```
--------
<h3 id="Paper">Paper</h3>
```
import React from 'react';
import Paper from 'material-ui/Paper';

const style = {
  height: 100,
  width: 100,
  margin: 20,
  textAlign: 'center',
  display: 'inline-block',
};

const PaperExampleSimple = () => (
  <div>
    <Paper style={style} zDepth={1} />
    <Paper style={style} zDepth={2} />
    <Paper style={style} zDepth={3} />
    <Paper style={style} zDepth={4} />
    <Paper style={style} zDepth={5} />
  </div>
);

export default PaperExampleSimple;
```
--------
<h3 id="Popover">Popover</h3>
```
import React from 'react';
import RaisedButton from 'material-ui/RaisedButton';
import Popover from 'material-ui/Popover';
import Menu from 'material-ui/Menu';
import MenuItem from 'material-ui/MenuItem';

export default class PopoverExampleSimple extends React.Component {

  constructor(props) {
    super(props);

    this.state = {
      open: false,
    };
  }

  handleTouchTap = (event) => {
    // This prevents ghost click.
    event.preventDefault();

    this.setState({
      open: true,
      anchorEl: event.currentTarget,
    });
  };

  handleRequestClose = () => {
    this.setState({
      open: false,
    });
  };

  render() {
    return (
      <div>
        <RaisedButton
          onTouchTap={this.handleTouchTap}
          label="Click me"
        />
        <Popover
          open={this.state.open}
          anchorEl={this.state.anchorEl}
          anchorOrigin={{horizontal: 'left', vertical: 'bottom'}}
          targetOrigin={{horizontal: 'left', vertical: 'top'}}
          onRequestClose={this.handleRequestClose}
        >
          <Menu>
            <MenuItem primaryText="Refresh" />
            <MenuItem primaryText="Help &amp; feedback" />
            <MenuItem primaryText="Settings" />
            <MenuItem primaryText="Sign out" />
          </Menu>
        </Popover>
      </div>
    );
  }
}
```
--------
<h3 id="Progress">Progress</h3>
--------
<h4 id="CircularProgress">Circular Progress</h4>
```
import React from 'react';
import CircularProgress from 'material-ui/CircularProgress';

const CircularProgressExampleSimple = () => (
  <div>
    <CircularProgress />
    <CircularProgress size={60} thickness={7} />
    <CircularProgress size={80} thickness={5} />
  </div>
);

export default CircularProgressExampleSimple;
```
--------
<h4 id="LinearProgress">Linear Progress</h4>
```
import React from 'react';
import LinearProgress from 'material-ui/LinearProgress';

const LinearProgressExampleSimple = () => (
  <LinearProgress mode="indeterminate" />
);

export default LinearProgressExampleSimple;
```
--------
<h4 id="RefreshIndicator">Refresh Indicator</h4>
```
import React from 'react';
import RefreshIndicator from 'material-ui/RefreshIndicator';

const style = {
  container: {
    position: 'relative',
  },
  refresh: {
    display: 'inline-block',
    position: 'relative',
  },
};

const RefreshIndicatorExampleSimple = () => (
  <div style={style.container}>
    <RefreshIndicator
      percentage={30}
      size={40}
      left={10}
      top={0}
      status="ready"
      style={style.refresh}
    />
    <RefreshIndicator
      percentage={60}
      size={50}
      left={65}
      top={0}
      status="ready"
      style={style.refresh}
    />
    <RefreshIndicator
      percentage={80}
      size={60}
      left={120}
      top={0}
      color="red"
      status="ready"
      style={style.refresh}
    />
    <RefreshIndicator
      percentage={100}
      size={70}
      left={175}
      top={0}
      color="red" // Overridden by percentage={100}
      status="ready"
      style={style.refresh}
    />
  </div>
);

export default RefreshIndicatorExampleSimple;
```
--------
<h3 id="SelectField">Select Field</h3>
```
import React, {Component} from 'react';
import SelectField from 'material-ui/SelectField';
import MenuItem from 'material-ui/MenuItem';

const styles = {
  customWidth: {
    width: 150,
  },
};

/**
 * `SelectField` is implemented as a controlled component,
 * with the current selection set through the `value` property.
 * The `SelectField` can be disabled with the `disabled` property.
 */
export default class SelectFieldExampleSimple extends Component {
  state = {
    value: 1,
  };

  handleChange = (event, index, value) => this.setState({value});

  render() {
    return (
      <div>
        <SelectField
          floatingLabelText="Frequency"
          value={this.state.value}
          onChange={this.handleChange}
        >
          <MenuItem value={1} primaryText="Never" />
          <MenuItem value={2} primaryText="Every Night" />
          <MenuItem value={3} primaryText="Weeknights" />
          <MenuItem value={4} primaryText="Weekends" />
          <MenuItem value={5} primaryText="Weekly" />
        </SelectField>
        <br />
        <SelectField floatingLabelText="Frequency" value={1} disabled={true}>
          <MenuItem value={1} primaryText="Disabled" />
          <MenuItem value={2} primaryText="Every Night" />
        </SelectField>
        <br />
        <SelectField
          floatingLabelText="Frequency"
          value={this.state.value}
          onChange={this.handleChange}
          style={styles.customWidth}
        >
          <MenuItem value={1} primaryText="Custom width" />
          <MenuItem value={2} primaryText="Every Night" />
          <MenuItem value={3} primaryText="Weeknights" />
          <MenuItem value={4} primaryText="Weekends" />
          <MenuItem value={5} primaryText="Weekly" />
        </SelectField>
        <br />
        <SelectField
          floatingLabelText="Frequency"
          value={this.state.value}
          onChange={this.handleChange}
          autoWidth={true}
        >
          <MenuItem value={1} primaryText="Auto width" />
          <MenuItem value={2} primaryText="Every Night" />
          <MenuItem value={3} primaryText="Weeknights" />
          <MenuItem value={4} primaryText="Weekends" />
          <MenuItem value={5} primaryText="Weekly" />
        </SelectField>
      </div>
    );
  }
}
```
--------
<h3 id="Slider">Slider</h3>
```
import React from 'react';
import Slider from 'material-ui/Slider';

/**
 * The `defaultValue` property sets the initial position of the slider.
 * The slider appearance changes when not at the starting position.
 */
const SliderExampleSimple = () => (
  <div>
    <Slider />
    <Slider defaultValue={0.5} />
    <Slider defaultValue={1} />
  </div>
);

export default SliderExampleSimple;
```
--------
<h3 id="Switches">Switches</h3>
--------
<h4 id="Checkbox">Checkbox</h4>
```
import React from 'react';
import Checkbox from 'material-ui/Checkbox';
import ActionFavorite from 'material-ui/svg-icons/action/favorite';
import ActionFavoriteBorder from 'material-ui/svg-icons/action/favorite-border';
import Visibility from 'material-ui/svg-icons/action/visibility';
import VisibilityOff from 'material-ui/svg-icons/action/visibility-off';

const styles = {
  block: {
    maxWidth: 250,
  },
  checkbox: {
    marginBottom: 16,
  },
};

const CheckboxExampleSimple = () => (
  <div style={styles.block}>
    <Checkbox
      label="Simple"
      style={styles.checkbox}
    />
    <Checkbox
      checkedIcon={<ActionFavorite />}
      uncheckedIcon={<ActionFavoriteBorder />}
      label="Custom icon"
      style={styles.checkbox}
    />
    <Checkbox
      checkedIcon={<Visibility />}
      uncheckedIcon={<VisibilityOff />}
      label="Custom icon of different shapes"
      style={styles.checkbox}
    />
    <Checkbox
      label="Disabled unchecked"
      disabled={true}
      style={styles.checkbox}
    />
    <Checkbox
      label="Disabled checked"
      checked={true}
      disabled={true}
      style={styles.checkbox}
    />
    <Checkbox
      label="Label on the left"
      labelPosition="left"
      style={styles.checkbox}
    />
  </div>
);

export default CheckboxExampleSimple;
```
--------
<h4 id="RadioButton">Radio Button</h4>
```
import React from 'react';
import {RadioButton, RadioButtonGroup} from 'material-ui/RadioButton';
import ActionFavorite from 'material-ui/svg-icons/action/favorite';
import ActionFavoriteBorder from 'material-ui/svg-icons/action/favorite-border';

const styles = {
  block: {
    maxWidth: 250,
  },
  radioButton: {
    marginBottom: 16,
  },
};

const RadioButtonExampleSimple = () => (
  <div>
    <RadioButtonGroup name="shipSpeed" defaultSelected="not_light">
      <RadioButton
        value="light"
        label="Simple"
        style={styles.radioButton}
      />
      <RadioButton
        value="not_light"
        label="Selected by default"
        style={styles.radioButton}
      />
      <RadioButton
        value="ludicrous"
        label="Custom icon"
        checkedIcon={<ActionFavorite />}
        uncheckedIcon={<ActionFavoriteBorder />}
        style={styles.radioButton}
      />
    </RadioButtonGroup>
    <RadioButtonGroup name="shipName" defaultSelected="community">
      <RadioButton
        value="enterprise"
        label="Disabled unchecked"
        disabled={true}
        style={styles.radioButton}
      />
      <RadioButton
        value="community"
        label="Disabled checked"
        disabled={true}
        style={styles.radioButton}
      />
    </RadioButtonGroup>
    <RadioButtonGroup name="notRight" labelPosition="left" style={styles.block}>
      <RadioButton
        value="reverse"
        label="Label on the left"
        style={styles.radioButton}
      />
    </RadioButtonGroup>
  </div>
);

export default RadioButtonExampleSimple;
```
--------
<h4 id="Toggle">Toggle</h4>
```
import React from 'react';
import Toggle from 'material-ui/Toggle';

const styles = {
  block: {
    maxWidth: 250,
  },
  toggle: {
    marginBottom: 16,
  },
  thumbOff: {
    backgroundColor: '#ffcccc',
  },
  trackOff: {
    backgroundColor: '#ff9d9d',
  },
  thumbSwitched: {
    backgroundColor: 'red',
  },
  trackSwitched: {
    backgroundColor: '#ff9d9d',
  },
  labelStyle: {
    color: 'red',
  },
};

const ToggleExampleSimple = () => (
  <div style={styles.block}>
    <Toggle
      label="Simple"
      style={styles.toggle}
    />
    <Toggle
      label="Toggled by default"
      defaultToggled={true}
      style={styles.toggle}
    />
    <Toggle
      label="Disabled"
      disabled={true}
      style={styles.toggle}
    />
    <Toggle
      label="Label on the right"
      labelPosition="right"
      style={styles.toggle}
    />
    <Toggle
      label="Styling"
      thumbStyle={styles.thumbOff}
      trackStyle={styles.trackOff}
      thumbSwitchedStyle={styles.thumbSwitched}
      trackSwitchedStyle={styles.trackSwitched}
      labelStyle={styles.labelStyle}
    />
  </div>
);

export default ToggleExampleSimple;
```
--------
<h3 id="Snackbar">Snackbar</h3>
```
import React from 'react';
import Snackbar from 'material-ui/Snackbar';
import RaisedButton from 'material-ui/RaisedButton';

export default class SnackbarExampleSimple extends React.Component {

  constructor(props) {
    super(props);
    this.state = {
      open: false,
    };
  }

  handleTouchTap = () => {
    this.setState({
      open: true,
    });
  };

  handleRequestClose = () => {
    this.setState({
      open: false,
    });
  };

  render() {
    return (
      <div>
        <RaisedButton
          onTouchTap={this.handleTouchTap}
          label="Add to my calendar"
        />
        <Snackbar
          open={this.state.open}
          message="Event added to your calendar"
          autoHideDuration={4000}
          onRequestClose={this.handleRequestClose}
        />
      </div>
    );
  }
}
```
--------
<h3 id="Stepper">Stepper</h3>
```
import React from 'react';
import {
  Step,
  Stepper,
  StepLabel,
} from 'material-ui/Stepper';
import RaisedButton from 'material-ui/RaisedButton';
import FlatButton from 'material-ui/FlatButton';

/**
 * Horizontal steppers are ideal when the contents of one step depend on an earlier step.
 * Avoid using long step names in horizontal steppers.
 *
 * Linear steppers require users to complete one step in order to move on to the next.
 */
class HorizontalLinearStepper extends React.Component {

  state = {
    finished: false,
    stepIndex: 0,
  };

  handleNext = () => {
    const {stepIndex} = this.state;
    this.setState({
      stepIndex: stepIndex + 1,
      finished: stepIndex >= 2,
    });
  };

  handlePrev = () => {
    const {stepIndex} = this.state;
    if (stepIndex > 0) {
      this.setState({stepIndex: stepIndex - 1});
    }
  };

  getStepContent(stepIndex) {
    switch (stepIndex) {
      case 0:
        return 'Select campaign settings...';
      case 1:
        return 'What is an ad group anyways?';
      case 2:
        return 'This is the bit I really care about!';
      default:
        return 'You\'re a long way from home sonny jim!';
    }
  }

  render() {
    const {finished, stepIndex} = this.state;
    const contentStyle = {margin: '0 16px'};

    return (
      <div style={{width: '100%', maxWidth: 700, margin: 'auto'}}>
        <Stepper activeStep={stepIndex}>
          <Step>
            <StepLabel>Select campaign settings</StepLabel>
          </Step>
          <Step>
            <StepLabel>Create an ad group</StepLabel>
          </Step>
          <Step>
            <StepLabel>Create an ad</StepLabel>
          </Step>
        </Stepper>
        <div style={contentStyle}>
          {finished ? (
            <p>
              <a
                href="#"
                onClick={(event) => {
                  event.preventDefault();
                  this.setState({stepIndex: 0, finished: false});
                }}
              >
                Click here
              </a> to reset the example.
            </p>
          ) : (
            <div>
              <p>{this.getStepContent(stepIndex)}</p>
              <div style={{marginTop: 12}}>
                <FlatButton
                  label="Back"
                  disabled={stepIndex === 0}
                  onTouchTap={this.handlePrev}
                  style={{marginRight: 12}}
                />
                <RaisedButton
                  label={stepIndex === 2 ? 'Finish' : 'Next'}
                  primary={true}
                  onTouchTap={this.handleNext}
                />
              </div>
            </div>
          )}
        </div>
      </div>
    );
  }
}

export default HorizontalLinearStepper;
```
--------
<h3 id="Subheader">Subheader</h3>
```
import React from 'react';
import MobileTearSheet from '../../../MobileTearSheet';
import Avatar from 'material-ui/Avatar';
import {List, ListItem} from 'material-ui/List';
import Subheader from 'material-ui/Subheader';
import Divider from 'material-ui/Divider';
import CommunicationChatBubble from 'material-ui/svg-icons/communication/chat-bubble';

const ListExampleChat = () => (
  <MobileTearSheet>
    <List>
      <Subheader>Recent chats</Subheader>
      <ListItem
        primaryText="Brendan Lim"
        leftAvatar={<Avatar src="images/ok-128.jpg" />}
        rightIcon={<CommunicationChatBubble />}
      />
      <ListItem
        primaryText="Eric Hoffman"
        leftAvatar={<Avatar src="images/kolage-128.jpg" />}
        rightIcon={<CommunicationChatBubble />}
      />
      <ListItem
        primaryText="Grace Ng"
        leftAvatar={<Avatar src="images/uxceo-128.jpg" />}
        rightIcon={<CommunicationChatBubble />}
      />
      <ListItem
        primaryText="Kerem Suer"
        leftAvatar={<Avatar src="images/kerem-128.jpg" />}
        rightIcon={<CommunicationChatBubble />}
      />
      <ListItem
        primaryText="Raquel Parrado"
        leftAvatar={<Avatar src="images/raquelromanp-128.jpg" />}
        rightIcon={<CommunicationChatBubble />}
      />
    </List>
    <Divider />
    <List>
      <Subheader>Previous chats</Subheader>
      <ListItem
        primaryText="Chelsea Otakan"
        leftAvatar={<Avatar src="images/chexee-128.jpg" />}
      />
      <ListItem
        primaryText="James Anderson"
        leftAvatar={<Avatar src="images/jsa-128.jpg" />}
      />
    </List>
  </MobileTearSheet>
);

export default ListExampleChat;
```
--------
<h3 id="Table">Table</h3>
```
import React from 'react';
import {Table, TableBody, TableHeader, TableHeaderColumn, TableRow, TableRowColumn} from 'material-ui/Table';


const TableExampleSimple = () => (
  <Table>
    <TableHeader>
      <TableRow>
        <TableHeaderColumn>ID</TableHeaderColumn>
        <TableHeaderColumn>Name</TableHeaderColumn>
        <TableHeaderColumn>Status</TableHeaderColumn>
      </TableRow>
    </TableHeader>
    <TableBody>
      <TableRow>
        <TableRowColumn>1</TableRowColumn>
        <TableRowColumn>John Smith</TableRowColumn>
        <TableRowColumn>Employed</TableRowColumn>
      </TableRow>
      <TableRow>
        <TableRowColumn>2</TableRowColumn>
        <TableRowColumn>Randal White</TableRowColumn>
        <TableRowColumn>Unemployed</TableRowColumn>
      </TableRow>
      <TableRow>
        <TableRowColumn>3</TableRowColumn>
        <TableRowColumn>Stephanie Sanders</TableRowColumn>
        <TableRowColumn>Employed</TableRowColumn>
      </TableRow>
      <TableRow>
        <TableRowColumn>4</TableRowColumn>
        <TableRowColumn>Steve Brown</TableRowColumn>
        <TableRowColumn>Employed</TableRowColumn>
      </TableRow>
    </TableBody>
  </Table>
);

export default TableExampleSimple;
```
--------
<h3 id="Tabs">Tabs</h3>
```
import React from 'react';
import {Tabs, Tab} from 'material-ui/Tabs';
import Slider from 'material-ui/Slider';

const styles = {
  headline: {
    fontSize: 24,
    paddingTop: 16,
    marginBottom: 12,
    fontWeight: 400,
  },
};

function handleActive(tab) {
  alert(`A tab with this route property ${tab.props['data-route']} was activated.`);
}

const TabsExampleSimple = () => (
  <Tabs>
    <Tab label="Item One" >
      <div>
        <h2 style={styles.headline}>Tab One</h2>
        <p>
          This is an example tab.
        </p>
        <p>
          You can put any sort of HTML or react component in here. It even keeps the component state!
        </p>
        <Slider name="slider0" defaultValue={0.5} />
      </div>
    </Tab>
    <Tab label="Item Two" >
      <div>
        <h2 style={styles.headline}>Tab Two</h2>
        <p>
          This is another example tab.
        </p>
      </div>
    </Tab>
    <Tab
      label="onActive"
      data-route="/home"
      onActive={handleActive}
    >
      <div>
        <h2 style={styles.headline}>Tab Three</h2>
        <p>
          This is a third example tab.
        </p>
      </div>
    </Tab>
  </Tabs>
);

export default TabsExampleSimple;
```
--------
<h3 id="TextField">Text Field</h3>
```
import React from 'react';
import TextField from 'material-ui/TextField';

const TextFieldExampleSimple = () => (
  <div>
    <TextField
      hintText="Hint Text"
    /><br />
    <br />
    <TextField
      hintText="The hint text can be as long as you want, it will wrap."
    /><br />
    <TextField
      id="text-field-default"
      defaultValue="Default Value"
    /><br />
    <TextField
      hintText="Hint Text"
      floatingLabelText="Floating Label Text"
    /><br />
    <TextField
      hintText="Hint Text"
      floatingLabelText="Fixed Floating Label Text"
      floatingLabelFixed={true}
    /><br />
    <TextField
      hintText="Password Field"
      floatingLabelText="Password"
      type="password"
    /><br />
    <TextField
      hintText="MultiLine with rows: 2 and rowsMax: 4"
      multiLine={true}
      rows={2}
      rowsMax={4}
    /><br />
    <TextField
      hintText="Message Field"
      floatingLabelText="MultiLine and FloatingLabel"
      multiLine={true}
      rows={2}
    /><br />
    <TextField
      hintText="Full width"
      fullWidth={true}
    />
  </div>
);

export default TextFieldExampleSimple;
```
--------
<h3 id="TimePicker">Time Picker</h3>
```
import React from 'react';
import TimePicker from 'material-ui/TimePicker';

const TimePickerExampleSimple = () => (
  <div>
    <TimePicker
      hintText="12hr Format"
    />
    <TimePicker
      format="24hr"
      hintText="24hr Format"
    />
    <TimePicker
      disabled={true}
      format="24hr"
      hintText="Disabled TimePicker"
    />
  </div>
);

export default TimePickerExampleSimple;
```
--------
<h3 id="Toolbar">Toolbar</h3>
```
import React from 'react';
import IconMenu from 'material-ui/IconMenu';
import IconButton from 'material-ui/IconButton';
import FontIcon from 'material-ui/FontIcon';
import NavigationExpandMoreIcon from 'material-ui/svg-icons/navigation/expand-more';
import MenuItem from 'material-ui/MenuItem';
import DropDownMenu from 'material-ui/DropDownMenu';
import RaisedButton from 'material-ui/RaisedButton';
import {Toolbar, ToolbarGroup, ToolbarSeparator, ToolbarTitle} from 'material-ui/Toolbar';

export default class ToolbarExamplesSimple extends React.Component {

  constructor(props) {
    super(props);
    this.state = {
      value: 3,
    };
  }

  handleChange = (event, index, value) => this.setState({value});

  render() {
    return (
      <Toolbar>
        <ToolbarGroup firstChild={true}>
          <DropDownMenu value={this.state.value} onChange={this.handleChange}>
            <MenuItem value={1} primaryText="All Broadcasts" />
            <MenuItem value={2} primaryText="All Voice" />
            <MenuItem value={3} primaryText="All Text" />
            <MenuItem value={4} primaryText="Complete Voice" />
            <MenuItem value={5} primaryText="Complete Text" />
            <MenuItem value={6} primaryText="Active Voice" />
            <MenuItem value={7} primaryText="Active Text" />
          </DropDownMenu>
        </ToolbarGroup>
        <ToolbarGroup>
          <ToolbarTitle text="Options" />
          <FontIcon className="muidocs-icon-custom-sort" />
          <ToolbarSeparator />
          <RaisedButton label="Create Broadcast" primary={true} />
          <IconMenu
            iconButtonElement={
              <IconButton touch={true}>
                <NavigationExpandMoreIcon />
              </IconButton>
            }
          >
            <MenuItem primaryText="Download" />
            <MenuItem primaryText="More Info" />
          </IconMenu>
        </ToolbarGroup>
      </Toolbar>
    );
  }
}
```
--------
