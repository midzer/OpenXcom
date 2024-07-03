# Emscripten

## Build

```
mkdir build
cd build
emcmake cmake .. -DCMAKE_BUILD_TYPE=Release
```

## Link

```
em++ libyaml-cpp.a */*/*.o */*.o *.o -flto -O3 -o index.html -sUSE_SDL=2 -sUSE_SDL_IMAGE=2 -sSDL2_IMAGE_FORMATS='["lbm"]' -sUSE_SDL_MIXER=2 -sSDL2_MIXER_FORMATS='["cat"]' -sASYNCIFY -sINITIAL_MEMORY=192mb -sLEGACY_GL_EMULATION -sERROR_ON_UNDEFINED_SYMBOLS=0 --preload-file common/ --preload-file standard/ --preload-file UFO/ --preload-file TFTD/ --preload-file options.cfg --closure 1 -sEXPORTED_RUNTIME_METHODS=['allocate'] -Wl,-u,fileno
```
