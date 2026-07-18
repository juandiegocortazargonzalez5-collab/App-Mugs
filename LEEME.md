# Mugs San Cristóbal — Guía de instalación

Tienes 5 archivos:
- `index.html` — la app completa
- `manifest.json` — hace que se pueda "instalar"
- `sw.js` — permite que funcione sin internet
- `icon-192.png` / `icon-512.png` — íconos
- `apps-script.gs` — código para el respaldo en Google Sheets

## Paso 1: Publicar la app en internet (gratis, con GitHub Pages)

La app necesita vivir en una dirección web real (https) para poder instalarse
como app en tu celular. GitHub Pages te da esto gratis.

1. Crea una cuenta en https://github.com si no tienes una.
2. Crea un repositorio nuevo (botón verde "New"). Ponle de nombre `mugs-app`.
   Márcalo como público.
3. Sube los archivos: `index.html`, `manifest.json`, `sw.js`, `icon-192.png`,
   `icon-512.png` (arrástralos a la página del repositorio, "Add file" >
   "Upload files").
4. Ve a "Settings" > "Pages" (menú izquierdo). En "Branch" elige `main` y
   guarda.
5. Espera 1-2 minutos. GitHub te dará una dirección tipo:
   `https://tu-usuario.github.io/mugs-app/`

## Paso 2: Instalar en tu celular Android

1. Abre esa dirección en Chrome desde tu celular.
2. Toca los tres puntos (⋮) arriba a la derecha.
3. Toca "Instalar app" o "Agregar a pantalla de inicio".
4. Listo — aparecerá el ícono de Mugs San Cristóbal como cualquier otra app,
   sin barra de navegador, en pantalla completa.

## Paso 3: Conectar con Google Sheets (respaldo)

1. Ve a https://sheet.new — se crea una hoja de cálculo nueva.
2. Nómbrala "Pedidos Mugs SC".
3. Ve a "Extensiones" > "Apps Script".
4. Borra el código que aparece por defecto y pega todo el contenido de
   `apps-script.gs`.
5. Guarda el proyecto (ícono de disquete arriba).
6. Clic en "Implementar" (arriba a la derecha) > "Nueva implementación".
   - Tipo: **Aplicación web**
   - Ejecutar como: **Yo** (tu cuenta)
   - Quién tiene acceso: **Cualquier usuario**
7. Google te pedirá autorizar permisos — es tu propia cuenta, es seguro,
   solo escribe en tu propia hoja.
8. Copia la "URL de la aplicación web" que te entrega (empieza con
   `https://script.google.com/macros/s/...`).
9. Abre la app Mugs San Cristóbal en tu celular > ⚙️ Ajustes > pega esa URL
   en "Respaldo en Google Sheets" > Guardar enlace.
10. Toca "☁️ Respaldar todo ahora" cada vez que quieras enviar copia de tus
    pedidos a la hoja. También puedes hacerlo una vez al día como rutina.

## Cómo funciona la app día a día

- Los pedidos se guardan **en tu celular** (rápido, funciona sin internet).
- El botón "Respaldar ahora" envía una copia a tu Google Sheet como respaldo
  — así no dependes 100% del celular.
- También puedes usar "⬇️ Descargar respaldo local" en Ajustes para guardar
  un archivo de respaldo adicional cuando quieras.

## Importante sobre el borrado de datos

En Chrome, borrar solo "caché" NO borra tus pedidos. Pero borrar
"datos de sitio" o "todos los datos de navegación" SÍ los borra. Por eso el
respaldo en Sheets es importante — úsalo con frecuencia, sobre todo antes de
limpiar el celular o cambiar de equipo.

## Actualizar la app más adelante

Si quieres agregarle funciones (inventario, gráficas, historial de cliente,
etc.), vuelve a subir el `index.html` actualizado al mismo repositorio de
GitHub — reemplaza el archivo. La próxima vez que abras la app se
actualizará sola.
