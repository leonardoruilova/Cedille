# Microkernel Cédlle 


El Microkernel Cédille esta disenado para mantener much codigo en ejecucion fuera del nucleo. Esto implica que Cédille es inherentemente mas estable y seguro ya que sus servicios mas importantes son ejecutados con menores permisos. Los servicios mas importantes son ejecutados como daemons en espacio de usuario con los mismos  permisos (but possibly heightend) tal como otros procesos.

En el Microkernel Cédille utilizamos mucho de BSD asi como del modelo de procesos del nucleo Mach. Especificamente, utilizamos tareas en vez de procesos y utilizamos ports para IPC.

Sin embargo el Microkernel Cédille no es Mach ni algun otro nucleo de comun uso, es un proyecto diferente, inspirado por los anteriores. 
En el Microkernel Cédille  existe un interes de lograr mas cualidades UNIX que en Mach, but still have its own thing going.

### Licencia

Este proyecto esta liberado bajo la licencia MIT:
```
Permission is hereby granted, free of charge, to any person obtaining a copy of
this software and associated documentation files (the "Software"), to deal in
the Software without restriction, including without limitation the rights to
use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of
the Software, and to permit persons to whom the Software is furnished to do so,
subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS
FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR
COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER
IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN
CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
```

## Compilacion


1. Por favor utilice una implementacion de gcc / clang / para compilar.
2. Asegurese que cross compiles correctly, and targets the correct thing.
3. Determine un sistema de salida como iso,imagen o elf. If you can't decide, just build an elf for now. (Use `make kernel`)
4. Compile el kernel entregando al compilador las opciones directamente mediante la linea de comandos

Ejemplo:
On my host machine for building x86:
`make CC=i686-elf-gcc LD=i686-elf-gcc GENISO=genisoimage` which I have aliased to `make_kernel` in bash

Por favor, lea `doc/Porting Architecture.md` para mayor informacion.


## Spanish translation


Esta traduccion ha sido liberada a los Comunes bajo una licencia CC-BY-NC-SA, su autor es Virgilio Leonardo Ruilova
