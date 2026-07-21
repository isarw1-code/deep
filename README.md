# Deepmarkers · password screen

Reproducción de la pantalla de contraseña de Deepmarkers.

- Escribe la contraseña y pulsa **Enter**.
- Contraseña correcta (`helio`) → muestra **Access granted**.
- Contraseña incorrecta → muestra **Incorrect password**.
- **Need the password?** → pide permiso de cámara y muestra tu reflejo a pantalla completa (efecto espejo).
- **Esc** → cierra la cámara y libera el dispositivo.

## Importante sobre la cámara

El acceso a la cámara (`getUserMedia`) **solo funciona en un contexto seguro**:

- ✅ **GitHub Pages** (sirve por HTTPS) → funciona.
- ✅ `http://localhost` → funciona (para probar en local).
- ❌ Abrir el archivo con doble clic (`file://`) → el navegador **no** dará acceso a la cámara.

El navegador **siempre** mostrará su propio aviso pidiendo permiso; no se puede activar la cámara de forma oculta.
El vídeo se muestra únicamente en la propia pantalla del visitante: **no se graba, ni se guarda, ni se envía a ningún servidor.**

## Probar en local

```bash
cd deep
python3 -m http.server 8000
# abre http://localhost:8000
```

## Subir a GitHub Pages

```bash
cd deep
git init
git add .
git commit -m "Deepmarkers password screen"
git branch -M main
git remote add origin https://github.com/TU_USUARIO/TU_REPO.git
git push -u origin main
```

Luego en GitHub: **Settings → Pages → Branch: `main` / root → Save**.
La página quedará en `https://TU_USUARIO.github.io/TU_REPO/`.

## Tipografía

La fuente es **JetBrains Mono** (monospace), incrustada en el propio repo
(`assets/fonts/JetBrainsMono-Regular-latin.woff2`) mediante `@font-face`.
No depende de Google Fonts, así que funciona sin conexión y sin llamadas externas.

## Archivos

```
deep/
├── index.html        # la página
├── assets/
│   ├── logo.png      # logo Deep (blanco sobre transparente)
│   └── fonts/
│       └── JetBrainsMono-Regular-latin.woff2
└── README.md
```
