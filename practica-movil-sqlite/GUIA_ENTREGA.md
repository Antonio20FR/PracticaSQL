# Guia breve para terminar la practica en GitHub Codespaces

**Alumno:** Juan Antonio Flores Rivera  
**Materia:** Desarrollo Movil  
**Proyecto:** Tareas de Antonio (Expo + SQLite)

## Subida del codigo

1. En Moodle, abre el enlace de la plantilla del profesor y usa **Use this template > Create a new repository**. Ponle por ejemplo `practica-movil-flores`. **Captura 1:** pagina del nuevo repositorio.
2. En el repositorio, abre **Code > Codespaces > Create codespace on main**. **Captura 2:** editor de Codespaces.
3. Sustituye en tu repositorio el contenido de `App.js`, `app.json` y `README.md` por los archivos personalizados de este ZIP. Si ya tiene los demas archivos de la plantilla, dejalos. Si el proyecto se sube sin plantilla, sube **el contenido dentro de `practica-movil-sqlite/`** a la raiz del repositorio.
4. En la terminal del Codespace, usa tu nombre real y el correo vinculado a GitHub:

```bash
git config --global user.name "Juan Antonio Flores Rivera"
git config --global user.email "TU_CORREO_DE_GITHUB"
npm install
```

   **Captura 3:** terminal sin errores al instalar. Nota: la configuracion `.devcontainer` puede ejecutar `npm install` automaticamente al crear el entorno.
5. Ejecuta:

```bash
npx expo start --web
```

   En la pestana **PORTS**, abre el puerto 8081; agrega **tres tareas**, marca una como completada y elimina otra. **Captura 4:** app con tareas visibles.
6. La personalizacion ya esta hecha en el ZIP: titulo **Tareas de Antonio** y color **#0D9488**. Comprueba la actualizacion de la vista previa. **Captura 5:** pantalla personalizada.
7. En la terminal, verifica los cambios y subelos:

```bash
git status
git add -A
git commit -m "Personalizo mi practica"
git push
```

   **Captura 6:** ultimo commit visible en github.com.
8. Deten o cierra el Codespace, vuelve a abrirlo desde el **mismo navegador y origen web**, comprueba si las tareas permanecen y anota el resultado de la prueba.
9. Abre el archivo DOCX del informe: escribe tu **matricula**, pega la **URL real del repositorio**, reemplaza las **seis casillas de evidencia** con tus capturas y registra el resultado de la prueba de persistencia. Exporta a PDF y entrega en Moodle.

## Sobre SQLite

En este proyecto `sql.js` ejecuta SQLite con WebAssembly en el navegador. Los cambios se exportan como bytes, se codifican en base64 y se guardan en `localStorage`, con la clave `practica_tareas_db_v1`. La persistencia depende del perfil y del origen web del navegador, no del almacenamiento en disco del Codespace.
