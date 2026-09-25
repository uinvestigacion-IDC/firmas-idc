# Firmas IDC

Generador de firmas de correo electrónico en HTML para el Instituto de Educación Superior Público "Diseño y Comunicación" (IDC). Produce una firma en tablas con estilos en línea, con el logo del programa de estudio, los colores de cada especialidad y los datos de contacto de la persona usuaria.

Versión: septiembre de 2026.

## Contenido del paquete

| Archivo | Descripción |
|---|---|
| `firmas-idc.html` | Generador. Archivo único de unos 245 KB que incluye estilos, código, logos e íconos. |
| `firmas-idc-imagenes.zip` | Carpeta `firmas-idc` con las 30 imágenes que usa la firma, para publicarlas en un servidor público. |
| `README.md` | Este documento. |

## Requisitos

- Navegador de escritorio: Chrome, Edge, Firefox o Safari.
- Cuenta de correo institucional en Google Workspace ("Correo de IDC"), usada desde el navegador.
- Una carpeta pública en internet para las imágenes (por ejemplo, GitHub Pages).

El archivo HTML funciona sin instalación. Solo la tipografía de la interfaz (Lexend e IBM Plex Mono) se descarga de Google Fonts; sin conexión, la interfaz usa Helvetica o Arial.

## Especialidades y colores

| Clave | Especialidad | Color | Logo |
|---|---|---|---|
| `inst` | Institucional | `#0072b9` | `idc.png` |
| `int` | Diseño de Interiores | `#009c9d` | `logo-int.png` |
| `pub` | Diseño Publicitario | `#009ad3` | `logo-pub.png` |
| `mod` | Diseño de Modas | `#e14a94` | `logo-mod.png` |
| `cav` | Comunicación Audiovisual | `#f3a20b` | `logo-cav.png` |

Colores institucionales: `#f3a100`, `#0072b9`, `#555553`, `#545452`, `#4a4b56`.

El color de la especialidad se aplica al filete vertical, al texto del área, a los íconos de contacto y a la línea "Primer Instituto Licenciado".

## Estructura de la firma

Diseño horizontal de dos columnas:

- Columna izquierda (190 px): logo del programa de estudio o logo institucional, y debajo el texto "Primer Instituto Licenciado / Resolución Viceministerial N.° 164-2025-MINEDU".
- Filete vertical de 3 px en el color de la especialidad.
- Columna derecha: nombre (19 px), cargo (13 px), área (11 px, mayúsculas) y datos de contacto (12 px) con íconos de 16 px: correo, teléfono, celular, sitio web y dirección.
- Aviso de confidencialidad opcional al pie (10 px).

Tipografía: Typo Formal Demo para el nombre y Louis George Cafe para el texto, con Helvetica y Arial como alternativas. Quien recibe el correo ve Typo Formal Demo y Louis George Cafe solo si tiene esas fuentes instaladas. En el nombre, los signos de puntuación se escriben en Helvetica, porque la versión Demo de Typo Formal no dibuja bien el punto.

## Uso del generador

1. Abrir `firmas-idc.html` en el navegador.
2. Elegir la especialidad.
3. Completar "Datos personales": nombre, cargo, área, correo, teléfono, celular, sitio web y dirección. Los campos vacíos no aparecen en la firma.
4. En "Logotipos", pegar la dirección de la carpeta pública de imágenes (ver la sección siguiente).
5. Pulsar "Previsualizar" para ver la firma a tamaño real dentro de un correo de ejemplo, con fondo claro u oscuro.
6. Pulsar "Guardar datos". Los datos quedan en el almacenamiento local del navegador (clave `idc-firmas-v2`) y no se comparten con otros equipos ni con otras personas.
7. Pulsar "Copiar firma" y pegarla en Gmail.

Mientras no haya carpeta pública de imágenes, la página muestra el aviso "Antes de instalar".

Otras opciones:

- "Marcadores de contacto": íconos en círculo de color o letras (E, T, M, W, D).
- "Mostrar también el logo institucional IDC": agrega el logo institucional debajo del logo del programa.
- Cargar un logo propio para la especialidad, desde un archivo o una URL.
- Cargar los archivos de Typo Formal Demo y Louis George Cafe para verlas en la vista previa.
- "Copiar código HTML": copia el código fuente de la firma.
- "Restablecer ejemplo": vuelve a los datos de ejemplo.

## Publicación de las imágenes

Gmail no muestra las imágenes incrustadas en la firma (base64) y rechaza firmas de más de 10 000 caracteres. Por eso los logos y los íconos deben estar en una dirección pública.

La carpeta `firmas-idc` contiene 30 archivos. No hay que cambiarles el nombre, porque el generador arma las direcciones a partir de ellos:

- `idc.png`: logo institucional.
- `logo-int.png`, `logo-pub.png`, `logo-mod.png`, `logo-cav.png`: logos de programa.
- `icono-{tipo}-{clave}.png`: 25 íconos de 48 × 48 px, que se muestran a 16 px. Los tipos son `mail`, `tel`, `cel`, `web` y `dir`, y las claves son las de la tabla de especialidades.

Pasos en GitHub Pages:

1. En github.com: botón `+` › New repository. Nombre: `firmas-idc`. Visibilidad: Public. Botón Create repository.
2. Add file › Upload files. Subir los 30 archivos, es decir, el contenido de la carpeta y no la carpeta. Botón Commit changes.
3. Settings › Pages. Source: Deploy from a branch. Branch: `main`, carpeta `/ (root)`. Botón Save.
4. Después de uno o dos minutos, abrir `https://USUARIO.github.io/firmas-idc/idc.png` para comprobar que el logo carga.
5. Pegar `https://USUARIO.github.io/firmas-idc/` en el campo "Carpeta pública de imágenes" y pulsar "Guardar datos".

Si se cambia una imagen, hay que reemplazar el archivo con el mismo nombre en el repositorio.

## Instalación en Gmail (Correo de IDC)

1. En el generador, pulsar "Copiar firma".
2. En mail.google.com: ícono de engranaje › Ver todos los ajustes.
3. En la pestaña General, bajar hasta la fila "Firma", que está entre "Crear contactos para el autocompletado" e "Indicadores de nivel personal". Para ir directo, buscar el texto "No hay ninguna firma" con Ctrl + F.
4. Pulsar "Crear", escribir el nombre `IDC` y confirmar.
5. Hacer clic en el recuadro de texto y pegar con Ctrl + V (Cmd + V en Mac).
6. En "Valores predeterminados de firma", elegir `IDC` en "Para correos nuevos" y en "Al responder/reenviar". Si la cuenta tiene varias direcciones en "Enviar como", hacerlo en la dirección que corresponda.
7. Pulsar "Guardar cambios" al final de la pestaña General, después de "Respuesta automática".
8. Enviar un correo de prueba a otra cuenta.

La app de Gmail para celular tiene su propio ajuste de firma, solo de texto, y no usa esta firma.

## Problemas frecuentes

| Síntoma | Causa | Solución |
|---|---|---|
| Cuadros vacíos en lugar del logo o los íconos | La carpeta pública es incorrecta o todavía no está activa | Abrir la dirección de la carpeta seguida de `idc.png` en el navegador |
| La firma se pega sin formato | El navegador no permitió copiar con formato | Pulsar de nuevo "Copiar firma"; la firma queda seleccionada en la vista previa y se copia con Ctrl + C |
| Gmail indica que la firma es demasiado larga | Las imágenes van incrustadas | Completar la carpeta pública de imágenes antes de copiar |
| La tipografía cambia a Helvetica o Arial | Quien recibe no tiene instaladas las fuentes de la marca | Es el comportamiento esperado |
| Las imágenes no se ven en la cuenta que recibe | Esa cuenta tiene activado "Preguntar antes de mostrar imágenes externas" | Pulsar "Mostrar imágenes" en el mensaje |

## Limitaciones conocidas

- La guía de instalación cubre solo Gmail desde el navegador.
- Los nombres de los menús de Gmail pueden cambiar con actualizaciones de Google. Los pasos 2 a 7 se basan en la configuración de Correo de IDC de septiembre de 2026.
- El nombre de la ventana que aparece después de pulsar "Crear" y las listas de "Valores predeterminados de firma" no se verificaron en pantalla.
- Typo Formal Demo es una versión de demostración. Antes de usarla en la firma institucional conviene revisar su licencia.
- Los tonos de los logos de Diseño de Modas (cercano a `#c83186`) y Comunicación Audiovisual (cercano a `#e09c28`) no coinciden exactamente con los colores de especialidad `#e14a94` y `#f3a20b`.

## Créditos

Mg. Mario Quiroz Martínez. Unidad de Investigación, IES Público "Diseño y Comunicación", Lima, 2026.
