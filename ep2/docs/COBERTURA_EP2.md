# Reporte de cobertura — EduBío 360 EP2

**Fecha:** 26 de octubre de 2026

**Comando:** `npm run test:coverage`
**Proveedor:** v8, mediante Vitest

| Métrica | Cobertura |
|---|---:|
| Sentencias | 92,50 % |
| Ramas | 82,34 % |
| Funciones | 82,80 % |
| Líneas | 92,50 % |

Se ejecutaron 72 pruebas distribuidas en 15 archivos, sin fallos en la ejecución registrada. Los módulos incluidos abarcan componentes, contexto, repositorios, servicios, páginas y validaciones. Se excluyen archivos de tests, configuración, dependencias, recursos públicos y el punto de montaje de la aplicación.

El reporte HTML detallado se genera en `coverage/index.html`. El archivo `coverage/coverage-summary.json` entrega las cantidades cubiertas y totales, por archivo y de forma global.

El comportamiento del mapa incrustado y la adaptación visual a distintos dispositivos requieren comprobaciones adicionales en un navegador. El control de acceso es simulado y no constituye seguridad de servidor. La pauta de EP2 no fija un porcentaje mínimo ni solicita JaCoCo.
