# Observador Digital

Aplicacion web para asistencia, observador del estudiante, atencion a padres, firma digital simple, calificaciones y exportacion en Excel.

## Probar

Abrir con servidor local:

```bash
python -m http.server 8765
```

Luego entrar a:

```text
http://127.0.0.1:8765/
```

## Publicar en GitHub Pages

1. Crear un repositorio.
2. Subir el contenido de esta carpeta.
3. Activar GitHub Pages desde `Settings > Pages`.
4. Seleccionar la rama principal y la carpeta raiz.

Si usas el archivo portable `index.html`, el escudo institucional ya queda incluido dentro del archivo y no necesitas subir el PDF o PNG por separado.

## Conectar con Google Sheets

1. Crear o abrir un Google Sheet.
2. Ir a `Extensiones > Apps Script`.
3. Pegar el contenido de `google_apps_script.gs`.
4. Implementar como aplicacion web.
5. Copiar la URL del despliegue.
6. Pegarla en `Ajustes > URL del endpoint` dentro de la app.
7. Al abrir o actualizar la app, se cargan automaticamente los datos de Google Sheets.
8. Cada vez que se guarda asistencia, observador, contacto, estudiante, atencion a padres o notas, la app envia automaticamente los cambios a Google Sheets.
9. El boton `Actualizar ahora` queda como respaldo manual para cargar y enviar en un solo paso.

Cuando actualices `google_apps_script.gs`, vuelve a desplegar una nueva version de la aplicacion web en Apps Script para que la URL use el codigo nuevo.

## Datos

Los estudiantes estan en `data/students.json`, importados desde la lista original.

Las exportaciones generales salen en Excel `.xlsx`. El observador individual se descarga como documento HTML imprimible para conservar observaciones y firmas.
