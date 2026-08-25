# Carta

Una carta virtual, hecha para verse en un iPhone.

Es **un solo archivo** (`index.html`). No usa librerías, ni imágenes, ni videos.
Pesa unos 30 KB, así que abre al instante incluso con datos móviles.

---

## Cómo personalizarla

Abre `index.html` con cualquier editor de texto y busca este bloque
(está más o menos a la mitad del archivo, marcado con ✏️):

```js
const CARTA = {
  ella:        "Mi amor",
  tu:          "Gabriel",
  inicialSello:"G",
  desde: { anio: 2024, mes: 1, dia: 1 },
  ...
};
```

Cambia **solo lo que está entre comillas**. Nada más.

| Campo | Qué hace |
|---|---|
| `ella` | Su nombre. Sale en la portada y en el encabezado. |
| `tu` | Tu nombre, en la firma. |
| `inicialSello` | La letra que va en el sello de cera del sobre. |
| `desde` | La fecha en que empezaron. Alimenta el contador de días. `mes: 1` = enero. |
| `cuerpo1` | Los párrafos románticos. |
| `cita1` / `cita2` | Las dos frases grandes destacadas. |
| `cosas` | La lista de cosas que amas de ella. |
| `cuerpo2` | La disculpa. |
| `cuerpo3` | El cierre. |
| `textoBoton` | Texto del botón final. |
| `respuesta` | Lo que aparece cuando ella lo toca. |
| `whatsapp` | Opcional. Tu número (código de país + número, sin `+` ni espacios) para que ella te conteste. Déjalo `""` para ocultar el botón. |

Dentro de los párrafos puedes usar:
- `<em>texto</em>` → cursiva blanca
- `<strong>texto</strong>` → dorado, para lo importante
- `<br>` → salto de línea

---

## Cómo se ve

1. **Portada:** cielo estrellado y un sobre cerrado con sello de cera. Debajo, en letras claras: *Toca para abrir*.
2. Ella toca el sobre → la solapa se abre en 3D y la hoja doblada asoma.
3. La escena se aleja y **la hoja se despliega**, ya escrita, sobre el cielo estrellado.
4. Todo el mensaje está en **una sola hoja de papel** que ella recorre deslizando: encabezado, carta, lista, contador de días, la disculpa y la firma manuscrita.
5. Contador animado de días juntos.
6. Botón final con lluvia de corazones.
7. Botón de música (♪, arriba a la derecha): melodía suave generada en el momento, sin archivos de audio.

## Detalles pensados para el iPhone

- `100dvh` y `safe-area-inset` → no se corta con la barra de Safari ni con la muesca.
- Vibración suave al abrir el sobre y al tocar el botón final.
- Sin zoom accidental por doble toque.
- Las animaciones se pausan si ella cambia de app (no le come batería).
- Respeta "Reducir movimiento" si lo tiene activado en Accesibilidad.
- Si el navegador congelara las animaciones, la hoja se muestra igual a los 4,5 s. Nunca se queda en blanco.

---

## Publicarla

Con GitHub Pages: **Settings → Pages → Source: `main` / carpeta `/ (root)` → Save**.

En un par de minutos queda en:

```
https://prime119.github.io/Carta/
```

Ese es el link que le mandas.
