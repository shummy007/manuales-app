# Manuales: app para Android

Proyecto de Android que muestra la biblioteca de supervivencia **sin el Manual médico** (que tiene su propia app). Funciona sin internet: todo el contenido está dentro de la app (`app/src/main/assets/index.html`).

## Opción A: que GitHub la compile (sin instalar nada)

1. Crear una cuenta gratis en github.com.
2. Crear un repositorio nuevo (botón **New**), por ejemplo `manuales`, privado.
3. En el repositorio: **Add file → Upload files**, arrastrar **todo el contenido de esta carpeta** (incluida la carpeta oculta `.github`) y tocar **Commit changes**.
   - Si el navegador no sube la carpeta `.github`, crear a mano el archivo: **Add file → Create new file**, nombre `.github/workflows/build.yml`, y pegar el contenido de ese archivo.
4. Ir a la pestaña **Actions**: se ejecuta "Compilar APK" (tarda unos 5 minutos). Si no arranca solo, entrar a "Compilar APK" y tocar **Run workflow**.
5. Cuando termina (tilde verde), entrar a la ejecución y descargar **Manuales-apk** al final de la página. Es un .zip con `app-debug.apk` adentro.
6. Pasar el `.apk` al teléfono, abrirlo y permitir "instalar apps de origen desconocido" cuando lo pida.

## Opción B: con Android Studio

Abrir esta carpeta con Android Studio, esperar a que sincronice y usar **Build → Build APK(s)**.

## Actualizar el contenido

Reemplazar `app/src/main/assets/index.html` por una versión nueva y volver a compilar. Subir `versionCode` en `app/build.gradle` para que el teléfono la acepte como actualización.
