# eSpeak-NG (Emscripten port)

[eSpeak-NG speech synthesizer](https://github.com/espeak-ng/espeak-ng), compiled to JavaScript via Emscripten.

Intended for use with [Echogarden](https://github.com/echogarden-project/echogarden).

## How to build

Building is only known to work in Linux. On Windows, use WSL.

Ensure you have essential build tools, like:
```
sudo apt install autoconf automake libtool autotools-dev build-essential gcc g++
```

Ensure you have `python` in path (used by Emscripten).

Clone the EMSDK repository:
```
git clone https://github.com/emscripten-core/emsdk
```

Install and activate EMSDK:
```
cd emsdk
git pull
./emsdk install latest
./emsdk activate latest
source ./emsdk_env.sh
cd ..
```

Clone [Echogarden's eSpeak-NG fork repository](https://github.com/echogarden-project/espeak-ng) and switch to its 'fork' branch:
```
git clone --branch fork https://github.com/echogarden-project/espeak-ng
```

Build eSpeak-NG Emscripten port
```
cd espeak-ng
./build-emscripten.sh
```

If successful, the compiled files should be at:
```
espeak-ng/emscripten/espeak-ng.js
espeak-ng/emscripten/espeak-ng.data
```
