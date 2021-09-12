
# Neutralino.js hello world

https://neutralino.js.org/

## Netralino.js install

Assumes node/npm installed with
```
sudo apt install nodejs
sudo apt install npm
```

## Create the neutralino.js development environment

The instructions on the neutralino.js website (https://neutralino.js.org/) have the node modules installed *globally*, which IMHO
isn't necessary. In this case the `node_modules` directory is local to the dev directory, and we use the path
`./node_modules/.bin/neu` for the neutralino CLI executable (it would be worth temporarily adding`./node_modules/.bin` to the
`PATH`.

```
mkdir neutralinojs
cd neutralinojs/
npm install @neutralinojs/neu
```

## Init a new application

This will create a simple app with html, css and js files as a working template that can be editted.
```
./node_modules/.bin/neu create neutralino_hello_world
```
Test run with
```
cd neutralino_hello_world
../node_modules/.bin/neu run
```

## Edit the source code for your app

The source files for the app are in `neutralino_hello_world/resources`:
```
index.html
styles.css
js/main.js
js/neutralino.js
```
i.e. the app is implemented in JS, HTML and CSS which you can modify as you would expect. `neutralino.js` is the required
neutralino component (12KB).

## Build your app into executables for each platform
```
../node_modules/.bin/neu build --release
```
The `neutralino_hello_world/dist/neutralino_hello_world` directory contains the executables for each platform:
```
neutralino_hello_world-linux_ia32
neutralino_hello_world-linux_x64
neutralino_hello_world-mac_x64
neutralino_hello_world-win_x64.exe
neutralinojs.log
res.neu
WebView2Loader.dll
```

## Run the built application
```
./dist/neutralino_hello_world/neutralino_hello_world-linux_x64
```
