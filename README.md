# SCADA Planta Desaladora Coquimbo – Simulador P&ID

Simulador tipo SCADA de la Planta Desaladora Coquimbo (v4) en un **único archivo HTML** (sin dependencias, funciona sin conexión) que **integra tres simuladores**: SCADA/P&ID, unilineal eléctrico y arquitectura de control/comunicaciones.

## Uso
Abrir `index.html` en el navegador, o publicarlo con GitHub Pages (Settings → Pages → Deploy from branch → `main` / root).

## Pantallas
- **P&ID unificado**: esquema animado con equipos, faceplates, alarmas, tendencias y escenarios; zoom y desplazamiento.
- **⚡ Energía**: potencia y energía acumulada por sistema y equipo, kWh/m³ y recuperación del ERD.
- **🎚 Regulación Q**: consigna de producción de 0 a 1.200 L/s con rampa, modularidad de racks de osmosis inversa y lazos de control.
- **📈 Eficiencia**: punto de operación vs. diseño, curva de consumo específico y curva bomba–sistema.
- **✔ Cumplimiento**: matriz de 46 requisitos (Filosofía de control, Criterios de diseño, Filosofía de operación) y 20 verificaciones en vivo.
- **Conducción Norte y estanque final 8.000 m³** (v4): PEAP → línea → estanque → demanda de red, con alarmas de nivel, presión y fuga, y escenarios de punta de demanda y fuga.
- **Click en cualquier equipo o instrumento**: «¿de qué se trata?» con función y referencia.
- **⚡ Unilineal** y **🛰 Control/Com.** (v4): ventanas acopladas por bus (`postMessage` + `BroadcastChannel`); **🧩 Vista integrada** muestra los tres en una sola pantalla. Interruptor abierto o PLC caído dispara el área; red/servidor caído congela datos y bloquea el telemando. **🔗 Externo…** conecta un simulador propio con el contrato v1 (ver pestaña Info).
- Emisario de rechazo paralelo a la captación, con cámara de carga y difusores.
- Exportación: HTML autónomo, SVG, PNG, CSV y JSON.

## Supuestos del modelo
Carga mínima 70 % por rack de OI; rampa de consigna 20 L/s/min; cámara de carga del emisario 120 m³; conducción 5.000 m³ y estanque final 8.000 m³ (sin lámina P&ID en el set), demanda de red ±12 % diario; topologías eléctrica y de control esquemáticas (no tomadas de los planos EL-DGU / IC-PLA-0001); curvas de bombas típicas (no de fabricante). Es un simulador didáctico, **no** reemplaza el sistema de control real.
