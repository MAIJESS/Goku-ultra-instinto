# Goku Ultra Instinto — tema para Kino TV

Un solo estilo para toda la app (celular y TV): azul noche profundo con **plata** como color principal, inspirado en la transformación Ultra Instinto. Reemplaza el logo de Kino por el nombre **GOKU** en plateado.

## Qué cambia

| Elemento | Valor |
|---|---|
| Acento y foco | Plata `#D4DEEC` / `#E8F0FB` |
| Fondo | Degradado azul noche `#04060B → #16233D` |
| Tarjetas y paneles | `#0B111D` / `#162033` con borde plateado fino |
| Texto | `#F2F6FC` y `#A9B6C9` |
| Logo | Wordmark **GOKU** (menú, cabecera y riel abierto del TV) y marca **G** (riel cerrado del TV) |
| Reproductor | Botones más grandes y circulares, barra de progreso más gruesa |
| Movimiento | Zoom de foco 1.08 (1.10 en TV), cambio suave de imágenes |
| Experiencia | Sugiere la experiencia **completa** (Kino pregunta antes; no cambia nada sin el sí de la persona) |

El logo usa solo vectores con colores fijos, así que siempre se ve plateado aunque la persona cambie el acento.

## Requisitos

- **Kino 0.9.81 o posterior** (`apiVersion` 18).
- Sin permisos, sin red y sin código: es un plugin de solo datos (`"hosts": []`).

## Instalación

1. Sube esta carpeta a un repositorio de GitHub (los archivos en la raíz o en una subcarpeta).
2. En Kino: **Ajustes ▸ Plugins ▸ Agregar** e ingresa `usuario/repositorio` (con subcarpeta si aplica).
3. Ve a **Ajustes ▸ Apariencia**, elige **Goku Ultra Instinto** y toca **Usar este tema**.

## Personalización (Ajustes ▸ Apariencia ▸ Personalizar)

- Color de acento: plata, blanco, azul hielo, lila o cian aura.
- Color del borde.
- Redondeo de las tarjetas (0–20).
- Zoom de foco (1.00–1.12).
- Fondo.

Las muestras de color funcionan bien con el control remoto del TV.

## Archivos

- `kino-plugin.json`: manifiesto y tema (`appThemes`).
- `plugin.js`: vacío a propósito (`export {};`); Kino lo carga y no llama nada.
- `icon.png`: ícono de 256×256 (propuesta visual: melena plateada con aura sobre fondo azul noche).
- `README.md`: este archivo.

## Validar antes de publicar

Con el kit del repositorio `kinotvapp/kino-plugins`:

```
node sdk/validate.mjs .
```

No debería mostrar advertencias de contraste ni de rangos. Verifica el resultado final en Kino (la vista previa de Apariencia), porque el kit no dibuja colores.

## Notas

- El `id` del tema (`goku-ultra-instinto`) no debe cambiar después de publicar: de él cuelgan la elección y los ajustes de la persona.
- Kino mantiene su propio logo en la pantalla de inicio, la puerta de entrada y las pantallas de decisión (compras, consentimientos, bloqueo +18).
- Opcional: agrega tu nombre en `author` y tu repositorio en `homepage` dentro de `kino-plugin.json`.
- Fan-made, sin afiliación con los creadores de Dragon Ball.
