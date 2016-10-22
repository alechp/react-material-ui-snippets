<h1>BUILD</h1>

Using [VSCE](https://code.visualstudio.com/docs/tools/vscecli) to Publish to [VSCode Marketplace](https://marketplace.visualstudio.com/)

-------

<h3 id="GettingStarted">Getting Started</h3>
1. Install CLI
```
npm i -g vsce
```

<h4>Install for local use</h4>
1. Package extension
```
vsce package
```

2. [Install extension](https://code.visualstudio.com/docs/extensions/install-extension)
```
code --install-extension react-material-ui-snippets-0.VERSION.0.vsix
```


<h4>Publish to marketplace</h4>
```
vsce publish
```
