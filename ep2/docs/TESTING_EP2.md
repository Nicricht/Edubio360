# EduBío 360

## Informe de pruebas — Evaluación Parcial 2

**Asignatura:** DSY1104 · Desarrollo Fullstack II

**Versión:** EP2
**Fecha:** 26 de octubre de 2026

### 1. Objetivo

Comprobar la navegación, el estado, las validaciones, la persistencia local, el CRUD y los flujos de roles migrados desde el frontend de la primera evaluación.

### 2. Herramientas

| Herramienta | Aplicación |
|---|---|
| Vitest | Ejecución y afirmaciones de pruebas |
| React Testing Library | Renderizado y consulta de componentes React |
| user-event | Simulación de escritura, selección y clics |
| jsdom | Entorno de navegador durante las pruebas |
| Cobertura v8 | Informe de líneas, ramas, funciones y sentencias |
| TypeScript y Vite | Verificación de tipos y compilación |

### 3. Ejecución

```bash
cd ep2
npm ci
npm run test:run
npm run test:coverage
npm run build
```

El reporte HTML se consulta en `ep2/coverage/index.html` después de ejecutar la cobertura. Se debe conservar la salida de ejecución y el reporte al momento de preparar la entrega.

### 4. Casos verificados

| Área | Casos representativos |
|---|---|
| Atomic Design y componentes | Propiedades tipadas, tarjetas, enlaces, comportamiento del comparador |
| Catálogo | Listado de 21 registros, filtros combinados, búsqueda sin tildes, estado vacío |
| Validaciones | RUN módulo 11, correo, contraseña, contacto, registro, ofertas y cupos |
| Ofertas | Crear, consultar, editar y eliminar; confirmación de eliminación; cupos |
| Usuarios | Registro, lista, cambio de rol, eliminación y cambios de comuna |
| Repository | Operaciones CRUD, identificación de registros y persistencia local |
| Sesiones | Ingreso por rol, rechazo de credenciales inválidas, cierre y cuentas inactivas |
| Orientación | Solicitud pendiente, asignación, reprogramación, cancelación, resultado, historial y avisos |
| Rutas protegidas | Redirección de usuario sin sesión y restricción de perfil |
| React Router | Inicio, vistas públicas, mapa, paneles y página inexistente |

### 5. Cobertura y resultados

**Resultados registrados el 26 de octubre de 2026:**

| Indicador | Resultado |
|---|---:|
| Archivos de pruebas | 15 |
| Pruebas aprobadas | 72 de 72 |
| Cobertura de líneas | 92,50 % |
| Cobertura de sentencias | 92,50 % |
| Cobertura de ramas | 82,34 % |
| Cobertura de funciones | 82,80 % |
| Compilación TypeScript + Vite | Correcta |

Los resultados se obtienen ejecutando `npm run test:coverage` en la versión correspondiente de la rama. El porcentaje mide qué partes del código fueron recorridas, pero no sustituye la revisión de las afirmaciones ni las pruebas de interfaz.

La pauta exige al menos 15 pruebas pertinentes y un reporte reproducible; no establece un porcentaje mínimo de cobertura. En esta entrega se incluyen pruebas de renderizado, eventos, validaciones, condiciones, filtros y las cuatro operaciones CRUD.

### 6. Archivos y exclusiones

Se evalúan los módulos TypeScript y TSX incluidos en el proyecto mediante la configuración de cobertura de Vitest. Los archivos de configuración, la carpeta `dist`, los recursos estáticos y las dependencias externas no forman parte del código funcional sometido a cobertura.

### 7. Comportamientos pendientes y limitaciones

- Las pruebas automatizadas no sustituyen la comprobación visual en dispositivos móviles, tabletas y computadores.
- Las comunicaciones entre pestañas deben verificarse también en el navegador real.
- El mapa requiere internet para cargar la cartografía de OpenStreetMap; la carga de mapas externos no se simula en jsdom.
- La autenticación y la persistencia funcionan solo como demostración local; no hay backend ni gestión de contraseñas reales.
- Los casos que dependen del servidor Nginx y de la imagen Docker se verifican en el flujo automatizado de GitHub cuando se ejecute la rama.
- El porcentaje de ramas puede aumentar al agregar casos de error, permisos, almacenamiento dañado y edición de perfil.

### 8. Interpretación

Una prueba aprobada confirma el resultado explícito de ese caso, no la ausencia de errores en toda la aplicación. La cobertura muestra ejecución del código, no validez de los datos ni seguridad productiva. Se recomienda demostrar en la defensa una prueba de validación, una de filtros, una de CRUD y una de orientación entre estudiante y orientador.
