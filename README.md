## Terminal
Se corrió el siguiente comando para compilar usando emscripten:
```
emcc -O3 -s WASM=1 -s EXPORTED_FUNCTIONS="['_solveBoard', '_malloc', '_free']" -s EXPORTED_RUNTIME_METHODS="['cwrap', 'ccall']" sudoku.c -o sudoku.js
```
Se exporta ```_malloc```y ```_free```para manejo de memoria.
## Referencias
- [Código de Solver de Sudoku](https://www.geeksforgeeks.org/c/sudoku-in-c/)
- [Instalar Emscripten](https://emscripten-org.translate.goog/docs/getting_started/downloads.html?_x_tr_sl=en&_x_tr_tl=es&_x_tr_hl=es&_x_tr_pto=tc#platform-notes-installation-instructions-sdk)
- [Guía de C a Wasm](https://web.dev/articles/emscripting-a-c-library?hl=es-419)