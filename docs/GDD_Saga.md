# Documento de Diseño de Juego — Saga Pitwall Manager

## 1. Visión General de la Franquicia

- **Título de la saga:** Pitwall Manager
- **Género:** Estrategia / Gestión Deportiva en Tiempo Real
- **Rol del Jugador:** Director de Equipo (Team Principal / Jefe de Estrategia)
- **Plataforma:** Navegadores Web (Escritorio)
- **Tecnologías:** HTML5, CSS3, JavaScript Vanilla (ES6 Modules)

Pitwall Manager es una saga de juegos que te sitúa en el muro de boxes de la Fórmula 1.
Cada título está ambientado en una temporada distinta, con sus propias regulaciones,
tecnología y desafíos estratégicos. El núcleo común es la gestión en tiempo real de
neumáticos, combustible, ritmo de carrera y la presión de tomar decisiones con
información limitada.

## 2. Pilares de Diseño (Comunes a toda la saga)

- **Presión en el Muro de Boxes:** Decisiones estratégicas basadas en telemetría
  en tiempo real (o limitada, según la época).
- **Gestión de Recursos Críticos:** Controlar el ritmo para equilibrar velocidad
  con degradación de neumáticos, consumo de combustible y fatiga del piloto.
- **Estética de Ingeniería:** Interfaz de alto contraste y modo oscuro que emula
  las pantallas de datos reales de la Fórmula 1.

## 3. Títulos de la Saga

| Título | Ambientación | Señal de identidad | Enlaces |
|--------|-------------|-------------------|---------|
| **Pitwall Manager: F1 2000** | Temporada 2000 | Comunicaciones por radio con delay por cansancio del piloto. Gestión de V10, combustible y peso. | [GitHub](https://github.com/rreinav/pitwall-manager-f1-2000) · [GDD](games/pitwall-manager-f1-2000/docs/gdd/index.md) |
| **Pitwall Manager: F1 1976** | Temporada 1976 | Sin radio. Órdenes mediante carteles en meta. Fiabilidad mecánica y lógica de pizarra. | [GitHub](https://github.com/rreinav/pitwall-manager-f1-1976) · [GDD](games/pitwall-manager-f1-1976/docs/gdd/index.md) |

## 4. Estructura del Repositorio

```
pitwall-manager/                    # Hub de la saga
├── docs/
│   └── GDD_Saga.md                 # Este documento
├── src/                            # Landing page del hub
│   ├── index.html
│   └── css/style.css
├── games/                          # Juegos individuales (gitignored)
│   ├── pitwall-manager-f1-2000/    # GDD en docs/gdd/
│   └── pitwall-manager-f1-1976/    # GDD en docs/gdd/
├── AGENTS.md
└── README.md
```

Cada juego en `games/` es un repositorio independiente con su propio `.git`,
`package.json` y documentación de diseño detallada en `docs/gdd/`.

## 5. Navegación

- Para los detalles de implementación de cada título, consulta su `docs/gdd/index.md`
  dentro de su directorio en `games/`.
- Para instrucciones del agente de desarrollo, ver `AGENTS.md`.
