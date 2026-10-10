# SCADA Planta Desaladora Coquimbo – Simulador P&ID

Simulador tipo SCADA de la Planta Desaladora Coquimbo en un **único archivo HTML** (sin dependencias, funciona sin conexión).

## Uso
Abrir `index.html` en el navegador, o publicarlo con GitHub Pages (Settings → Pages → Deploy from branch → `main` / root).

## Pantallas
- **P&ID unificado**: esquema animado con equipos, faceplates, alarmas, tendencias y escenarios; zoom y desplazamiento.
- **⚡ Energía**: potencia y energía acumulada por sistema y equipo, kWh/m³ y recuperación del ERD.
- **🎚 Regulación Q**: consigna de producción de 0 a 1.200 L/s con rampa, modularidad de racks de osmosis inversa y lazos de control.
- **📈 Eficiencia**: punto de operación vs. diseño, curva de consumo específico y curva bomba–sistema.
- **✔ Cumplimiento**: matriz de 46 requisitos (Filosofía de control, Criterios de diseño, Filosofía de operación) y 20 verificaciones en vivo.
- Emisario de rechazo paralelo a la captación, con cámara de carga y difusores.
- Exportación: HTML autónomo, SVG, PNG, CSV y JSON.

## Supuestos del modelo
Carga mínima 70 % por rack de OI; rampa de consigna 20 L/s/min; cámara de carga del emisario 120 m³; curvas de bombas típicas (no de fabricante). Es un simulador didáctico, **no** reemplaza el sistema de control real.
