# Overview

Simple demonstration of using a [jsconfig.json](lambda/jsconfig.json) file in a lambda project that uses zip layers for `node_modules`, used to answer a [StackOverflow Question](https://stackoverflow.com/questions/62645700/running-aws-lambda-with-layers-using-nodejs-in-vscode-on-local-machine).

This allows naked imports in the [lambda/index.js](lambda/index.js) to find the modules that are only installed in the [layer/package.json](layer/package.json) project.

# Example

For example, in `index.js`, without the `jsconfig.json` file the following import will have no type information, but with the `jsconfig.json` file it will have type information:

```
import axios from 'axios';
```

## Screenshot

![](assets/vscode-type-info.png)
