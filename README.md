# Custom-EV-IV-Display-Screen (Terry's Edition)Ver. 1.5 2022.
 Plantilla personalizable para mostar información de EV, IV y BS de nuestro equipo pokémon en una nueva
 pantalla.

 Esta es una Modificación del Custom EV - IV Display Screen de Acimut la cual incluye algunos
 cambios esteticos que la versión original no posee.
 
(Los archivos dentro de la carpeta src\include\ fueron tomados de pokefirered.)
 
Características (Versión de Acimut):
-
+ Compatible con Pokémon Fire Red, Rojo Fuego y Emerald.
+ Puedes cambiar el fondo reemplazando el que viene por defecto, la inyección la insertará
  automáticamente.
+ Se puede cambiar las coordenadas del sprite del pokémon, así como sus textos.
+ El color de la estadística de IVs cambia de acuerdo a la naturaleza.
+ Muestra estadísticas base de acuerdo a la especie.
+ Censura la estadística de los huevos, en cambio, dice aprox. cúantos pasos te falta para la eclosión.
+ Bien bomnito y con somniditos xd
+ Huele a limón.
+ base: Pokémon Fire Red.


Versión de Tio Terry (Mia):
-
+ Continua siendo compatible con Fire Red, Rojo Fuego y Emerald.
  (De momento).
+ 2 colores para Chico y Chica.                      
  (Configurados segun el genero del prota).
+ Reorganización de textos.
+ Naturalezas con nombre e indicadores con su respectivo color.
+ Nivel, Genero y Tipos del Pokémon.
+ Tipo de Poder Oculto segun la suma de Ivs.
+ PokéBalls del equipo.
  (la Pokeball del Pokémon seleccionado se abrira).
+ El fondo, el Nombre, el Nivel del Pokémon se tornaran amarillos si el Pokémon es Shiny.
+ Sigue siendo bomnito y con más somniditos xd
+ Conserva el olor a Limón.
+ base: Pokémon Fire Red.

***Notas:***
Para configuraciones simples aqui esta lo mas fundamental a hacer para compilarlo y usarlo InGame:

- DevkitARM y ARMIPS son necesarios (versiones más recientes).

- Para compilar es necesario tener preproc.exe y gbagfx.exe dentro alguna ruta de la variable PATH

- Abrir el archivo config.mk, buscar y cambiar ff0000 de la siguiente línea por un offset alineado con 
  suficiente espacio libre (más de 0x2000 bytes):
        `INSERT_INTO ?= 0x08ff0000`
- En el archivo config.mk, tambien buscar la siguiente línea
        `ROM_CODE ?= BPRE`
        - dejar BPRE para compilar usando Fire Red
        - cambiar a BPRS para compilar usando Rojo Fuego 
        (Si usas Rojo Fuego ve aqui para ver la configuración del archivo main_eviv.c)
        - cambiar a BPEE para compilar usando Emerald
        (Si usas Emerald ve aqui para ver la configuración del archivo main_eviv.c)

- Compilan ejecutando make con su terminal, y una rom con la inyección aparecerá en una carpeta llamada
  build (Tendra el nombre segun la Versión del juego que acabas de colocar en el archivo config.mk).

- Usar en un script `callasm` seguido por el offset+1 donde insertaron el código.

- Archivos dentro de la carpeta include fueron tomados de pokefirered.