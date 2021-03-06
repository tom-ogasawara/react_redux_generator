# React-Redux File Generator

[![npm version](https://badge.fury.io/js/redux-file-gen.svg)](https://badge.fury.io/js/redux-file-gen)  [![Build Status](https://travis-ci.org/davidhu2000/react_redux_generator.svg?branch=master)](https://travis-ci.org/davidhu2000/react_redux_generator)

This generator helps to create the necessary files for a react-redux application. It follows the file structure below. The `frontend` folder is stored at the root directory of the application.

## New features in version 1.2
- [Action](docs/action.md) generator detects keyword `receive` in action name and automatically add the argument name and key-value pair to the function.
- [Util](docs/util.md) generator detects keyword `fetch` in util name and automatically add a basic `ajax` request in the body of the function.
- Added command `remove` or `r` to remove generated files.
- [Reducer](docs/reducer.md) now accepts actions and will automatically add the import and case statements.

## Installation
```
npm install -g redux-file-gen
```

In order to create the terminal command `redux`, this package needs to be installed globally.

## Usage

```
redux [command] [fileType] [options]
```

## File structure

```
frontend
  |- actions
    |- <actionName>_actions.js
  |- components
    |- <componentName>
      |- <componentName>.jsx
      |- <componentName>_container.jsx
    |- app.jsx
    |- root.jsx
  |- reducers
    |- root_reducer.js
    |- <reducerName>_reducer.js
  |- store
    |- store.js
  |- util
    |- <utilName>_util.js
  |- <projectName>.jsx
```

## Commands

| Command           | Function                    |
|-------------------|-----------------------------|
| `generate`, `g`   | use the file generator      |
| `remove`, `r`     | remove the generated files  |
| `--help`, `-h`    | see available commands      |
| `--version`, `-v` | see current package version |


## FileTypes

| FileType                                 | Function                                                            |
|------------------------------------------|---------------------------------------------------------------------|
| `base <projectName>`                     | generate `app.jsx`, `root.jsx`, `<projectName>.jsx`, and `store.js` |
| `action <name> [action1] [action2] ...`  | generate `<name>_actions.js` with specified actions                 |
| `component <name> [options]`             | generate `<name>.jsx` and `<name>_container.jsx`                    |
| `reducer <name> [action1] [action2] ...` | generate `<name>_reducer.js`                                        |
| `util <name> [util1] [util2] ...`        | generate `<name>_util.js` with specified utils                      |

## Options

| Option                  | Function                          |
|-------------------------|-----------------------------------|
| `--functional`, `-f`    | create functional component       |
| `--no-container`, `-nc` | do not create component container |

## For more details regard different types of files
- [Base](docs/base.md)
- [Action](docs/action.md)
- [Component](docs/component.md)
- [Reducer](docs/reducer.md)
- [Store](docs/store.md)
- [Utility](docs/util.md)

## Version notes

To see what features are added during each update, click [here](docs/update_notes.md)

## Contributing

To request a feature or report an issue, click [here](https://github.com/davidhu2000/react_redux_generator/issues).
