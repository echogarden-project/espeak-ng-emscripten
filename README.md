# eSpeak-NG (Emscripten port)

[eSpeak-NG speech synthesizer](https://github.com/espeak-ng/espeak-ng), compiled to JavaScript via Emscripten.

Intended for use with [Echogarden](https://github.com/echogarden-project/echogarden).

## How to build

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
cd espeak
./build-emscripten.sh
```

If successful, the compiled files should be at:
```
espeak-ng/emscripten/espeak-ng.cjs
espeak-ng/emscripten/espeak-ng.data
```
