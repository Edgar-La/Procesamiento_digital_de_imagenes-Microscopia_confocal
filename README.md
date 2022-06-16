# Procesamiento_digital_de_imagenes-Microscopia_confocal

## Manual para el usuario
1. Agregar la imagen que se desa analizar (con extension .czi y cuidando que no tenga mas de 4 canales de color) en las carpetas __\Color_channels\Images__ & __\scripts\Images__
2. Acceder al archivo __Main.m__ que se encuentra en la raíz del repositorio, este es un script escrito en Matlab
3. En este script se debe colocar el nombre de la imagen agregada en el paso 1, este se escribe en la variable _file_name_, el nombre se escribe entre comillas simples y sin la extensión. 
4. Correr el programa.
5. De forma automática se creará una carpeta con el nombre de la imagen dentro de la carpeta __Resultados__, como su nombre lo indica aquí se guardarán los resultados de correr el código.

### Descripcion de los resultados

#### Imagenes
1. _Celulas_en_duda_ : Imagen que contiene las células que no se lograron segmentar correctamente.
2. _Celulas_Segmentadas_ : Imagen que contiene las células que se lograron segmentar correctamente.
3. _Celulas_Segmentadas_Enumeradas_ : Imagen del punto 2 pero a cada célula se le asignó un número.
4. _Clasificacion sobre el marcaje [Marcaje]_ : Imagen de la clasificación sobre un marcaje. Color Azul significa que la célula no contiene la proteína en cuestión (Célula Negativa), color Verde significa que la célula contiene la proteína en cuestión (Célula Positiva), Color Rojo significa que la célula no se segmentó correctamente.
5. _Imagen_Original_Grises_ : Imagen del canal DAPI en escala de grises.
6. _Regiones_ : Imagen que contiene 3 regiones, una región con poca densidad de células, otra con densidad media y una con densidad alta.

#### Tablas
1. _Conteo_General_ : Contiene la cantidad todal de células positivas y negativas de cada marcaje.
2. _Expresion_canal1_canal2_ : Contiene la comparación entre el canal 1 y 2 (cuantas células son postivas para ambos marcajes, cuantas negativas, etc.)
3. _Expresion_canal1_canal3_ : Contiene la comparación entre el canal 1 y 3 (cuantas células son postivas para ambos marcajes, cuantas negativas, etc.)
4. _Expresion_canal2_canal3_ : Contiene la comparación entre el canal 2 y 3 (cuantas células son postivas para ambos marcajes, cuantas negativas, etc.)
5. _ID_Canales_ : Contiene los nombres de los marcajes (sin contar DAPI) con su respectivo ID. 
6. _Tabla_Propiedades_Marcaje_ID_ : Contiene una tabla con características de cada célula segmentada, las columnas son: Área (área de la célula en píxeles), Area proteina dentro de celula (en píxeles), Porcentaje proteina dentro de celula, Eje mayor (longitud del eje mayor en píxeles), Eje menor (longitud del eje menor en píxeles), orientación (Ángulo de inclinación en grados), Inten_media nucleo (intensidad media del núcleo), Inten_media_proteina (intensidad media de la proteína que se encuentra dentro del núcleo), Estado (si la célula es positiva o negativa para el marcaje en cuestión, 0 significa célula negativa, 1 significa célula positiva y 2 significa célulaque no se segmentó correctamente), Region de pertenencia (indica la región donde se encuentra la célula)
7. _Tabla_Regiones_ : Contiene el conteo de células por regiones, las columnas son: Regiones (Indica la región en cuestión), Nucleos por region (Cantidad de cpelulas encontradas en la región dada), Area (área total de la región en micras cuadradas), Densidad (división del número de células encontradas entre el área).

## Manual técnino
### Separar en canales una imagen .czi

### Procesar imágenes de los canales

### Programa de transparencia


Autores:
* [Edgar Lara Arellano](https://github.com/Edgar-La)
* [David Ángel Alba Bonilla](https://github.com/DavidAlba2627)
* [Uriel Cárdenas Aguilar](https://github.com/Uriel148)
