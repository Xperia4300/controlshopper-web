# ControlShopper — Landing page

Sitio de presentación de **ControlShopper**, la app de control de pedidos y ganancias para shoppers, pickers y drivers.

Hecho por [ControlCoding](mailto:supportcontrolcoding@gmail.com).

---

## Qué es esto

Una landing page estática de un solo archivo. Sin build, sin dependencias, sin `npm install`.
Todo el HTML, CSS y JavaScript vive en `index.html`.

```
controlshopper-web/
├── index.html      ← la página completa
├── vercel.json     ← headers de caché y seguridad
├── .gitignore
└── README.md
```

## Cómo verla en local

Abrí `index.html` con doble clic en el navegador. Listo.

Si preferís servirla por HTTP (para probar rutas y anclas tal como en producción):

```bash
python -m http.server 8000
# luego abrí http://localhost:8000
```

## Cómo desplegarla en Vercel

1. Entrá a [vercel.com/new](https://vercel.com/new) e importá este repositorio.
2. Framework Preset: **Other**.
3. Build Command: dejar **vacío**.
4. Output Directory: dejar **vacío** (raíz del proyecto).
5. Deploy.

Cada push a `main` despliega automáticamente.

## Paleta de marca (ControlCoding)

| Color        | Hex       | Uso                                             |
|--------------|-----------|-------------------------------------------------|
| Verde oscuro | `#00524A` | Hero, nav, sección de roles, bloque del fundador |
| Verde noche  | `#00342F` | Footer, pantalla del mockup                      |
| Turquesa     | `#00B5A3` | Botones, acentos, franja de stats, CTA final     |
| Naranjo      | `#F59E0B` | Plan Pro, badge "3 días gratis", paso 03         |
| Menta claro  | `#F1FAF8` | Fondos de secciones alternas                     |

Los colores están definidos como variables CSS en `:root`, al inicio de `index.html`.
Cambiar uno ahí lo cambia en toda la página.

## Tipografía (regla del proyecto)

**Manrope**, de Google Fonts. Es la misma fuente de la app (`@expo-google-fonts/manrope`)
y la del logotipo de ControlCoding. **No se reemplaza**: la coherencia entre app, web y
logo depende de esto.

```
font-family: 'Manrope', system-ui, -apple-system, sans-serif;
```

Pesos cargados: `400 500 600 700 800 900`.

Cómo se usan:

| Elemento                          | Peso | Nota                                        |
|-----------------------------------|------|---------------------------------------------|
| Títulos (h1–h4)                   | 700  | Mantiene las curvas redondeadas de Manrope  |
| H1 del hero                       | 800  | Excepción, por impacto                      |
| Logo ControlShopper / "coding"    | 800  | Definido por la marca                       |
| Botones                           | 600  |                                             |
| Cifras grandes y etiquetas        | 700  |                                             |
| Texto de cuerpo                   | 400  | `line-height: 1.65`                         |

**Por qué 700 y no 800 en los títulos:** en Manrope los pesos muy altos achatan las
curvas y la fuente pierde el carácter redondeado que define la marca. El `letter-spacing`
negativo se mantiene suave (`-.008em`) por la misma razón — apretarla más la endurece.

## Qué incluye

- Hero con mockup del teléfono mostrando el neto del día
- Franja de stats
- Cómo funciona (3 pasos)
- Funciones (4 tarjetas)
- Roles: Shopper / Picker / Driver
- Precios: prueba gratis y Pro mensual
- Comparación con / sin ControlShopper
- Sección del fundador
- Preguntas frecuentes (acordeón nativo con `<details>`)
- CTA final + footer con el logo de ControlCoding
- Botón flotante de WhatsApp

**Mobile:** menú hamburguesa con drawer y fondo oscurecido, y animaciones de aparición
al hacer scroll. Las animaciones respetan `prefers-reduced-motion` y tienen un
temporizador de seguridad: si el `IntersectionObserver` fallara, todo se muestra igual.

## Pendientes antes de publicar

- [ ] Reemplazar el `href="#"` del botón "Disponible en Google Play" por el link real de la ficha
- [ ] Agregar `og:image` y `twitter:card` para que se vea bien al compartir por WhatsApp
- [ ] Agregar favicon (`favicon.ico` o `icon.png` en la raíz)
- [ ] Sumar testimonios reales de los compañeros que probaron la app, con su autorización

## Contacto

- Soporte: supportcontrolcoding@gmail.com
- WhatsApp: [+56 9 5490 1981](https://wa.me/56954901981)
- Política de privacidad: https://xperia4300.github.io/controlshopper-legal/

---

© 2026 ControlCoding
