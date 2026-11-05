# APEX

> El primer campeonato real de combate humanoide.

![Built with Lovable](https://img.shields.io/badge/built%20with-Lovable-ff69b4)
![HTML5](https://img.shields.io/badge/HTML5-e34f26)
![CSS3](https://img.shields.io/badge/CSS3-1572b6)
![Tailwind](https://img.shields.io/badge/Tailwind-CSS-38bdf8)

## Sobre Apex

**Apex** es la plataforma oficial de un campeonato de combate entre robots humanoides reales. La web está enfocada en **eventos y boletería**: permite comprar entradas, conocer a los peleadores y revivir los mejores momentos de cada pelea.

La propuesta visual combina la fotografía deportiva comercial (estilo UFC) con la tecnología industrial contemporánea (estilo Boston Dynamics / EngineAI). Los robots se presentan como productos de ingeniería que existen hoy, no como personajes de videojuego.

## Secciones

### Header
- Logo tipo marca deportiva a la izquierda.
- Menú sutil: **Cartelera**, **Replays**, **Atletas T800**, **Boletería**.
- CTA primario en rojo: **COMPRAR BOLETAS**.

### Hero (venta de entradas)
- Fotografía de estudio/arena de un humanoide blanco estilo T800 en guardia de combate de MMA, con iluminación cenital dramática.
- Titular: *"EL PRIMER CAMPEONATO REAL DE COMBATE HUMANOIDE"*.
- Módulo de compra directa: fecha del próximo evento en vivo, ciudad/arena, selector de zonas (**Ring Side**, **Preferencial**, **General**) con precio claro y botón CTA rojo.

### Peleadores
- Grid de 3 tarjetas tipo ficha técnica industrial del modelo **T800 "White Eagle"** y sus variantes.
- Fotos en escala de grises/blanco tomadas en el pesaje oficial.
- Datos reales por unidad: peso (kg), torque de articulación (Nm), tipo de actuador y récord de K.O.

### Replays y highlights
- Grid estilo plataforma deportiva (DAZN) con miniaturas de intercambios de golpes, derribos y K.O. técnicos.
- Tarjetas oscuras con borde sutil `#1E2229` y contador de duración del video.

## Dirección de arte

### Estética del robot
Chasis compacto con panelería exterior de polímero técnico blanco ("White Eagle"), articulaciones y servomotores expuestos en gris titanio, y estructura en fibra de carbono y aluminio.
**Sin** pantallas holográficas, láseres ni luces de neón en el cuerpo.

### Paleta de colores

| Uso | Color | Hex |
| --- | --- | --- |
| Fondo principal | Negro Carbón | `#0D0D0D` |
| Contenedores de interfaz | Gris Acero | `#1E2229` |
| Texto secundario | Gris Platino | `#E0E6ED` |
| Texto principal | Blanco | `#FFFFFF` |
| Acción / urgencia | Rojo | `#FF1801` |

> **Regla del rojo:** se reserva **exclusivamente** para llamados a la acción de compra ("BUY TICKETS"), etiquetas de **LIVE** y marcadores de **K.O.** No se usa como decoración.

### Tipografía
- **Teko (Bold):** titulares condensados y agresivos.
- **Rajdhani:** textos técnicos y datos.

### Restricciones visuales (anti-cliché)
- El robot debe verse como un producto de ingeniería real, no como un personaje de ficción.
- Márgenes y espaciados muy amplios, propios de una plataforma de eventos de gama alta.

## Stack tecnológico

Sitio estático, sin frameworks de JavaScript:

- **HTML5** para la estructura
- **CSS3** para estilos propios mínimos
- **[Tailwind CSS](https://tailwindcss.com/)** para el sistema de diseño (paleta y tipografías de Apex definidas como tokens)

## Instalación y uso local

Requisitos: Node.js 18+ y npm (solo para compilar Tailwind).

```bash
git clone https://github.com/<tu-usuario>/apex.git
cd apex
npm install
npm run dev     # compila Tailwind en modo watch
```

Abre `index.html` en el navegador (o con la extensión Live Server de VS Code).

| Comando         | Descripción                                   |
| --------------- | --------------------------------------------- |
| `npm run dev`   | Compila `src/input.css` en modo watch         |
| `npm run build` | Genera `dist/output.css` minificado           |

## Tema de Tailwind

Los colores y tipografías de la dirección de arte viven en `src/input.css`:

```css
@import "tailwindcss";

@theme {
  --color-carbon: #0D0D0D;
  --color-steel: #1E2229;
  --color-platinum: #E0E6ED;
  --color-apex-red: #FF1801;

  --font-display: "Teko", sans-serif;
  --font-tech: "Rajdhani", sans-serif;
}
```

Así puedes usar clases como `bg-carbon`, `text-platinum`, `bg-apex-red` o `font-display` en el HTML.

## Estructura

```
apex/
├── index.html
├── src/
│   └── input.css      # Tailwind + tema de Apex
├── dist/
│   └── output.css     # CSS generado (no editar)
├── assets/            # Imágenes y videos
└── package.json
```

## Hoja de ruta

- [ ] Hero con módulo de compra de entradas
- [ ] Fichas técnicas de peleadores T800
- [ ] Grid de replays y highlights
- [ ] Integración de pasarela de pago para boletería
- [ ] Marcadores LIVE en tiempo real

## Contribuir

1. Haz un fork del repositorio.
2. Crea una rama: `git checkout -b feature/mi-mejora`.
3. Haz commit: `git commit -m "feat: describe tu cambio"`.
4. Sube la rama y abre un Pull Request.

## Licencia

Distribuido bajo licencia MIT. Consulta el archivo `LICENSE`.