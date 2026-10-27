# Guía de trabajo de Ritwornz en EduBío 360 EP2

## Punto de partida

La base es la rama `ep2/react-vite-typescript`, commit `9ac6f8e`. El proyecto ya tiene React, Vite, TypeScript, CRUD, rutas, 78 pruebas aprobadas e informe de cobertura. La rama **`ritwornz/proyecto-completo`** contiene todo el proyecto React y TypeScript junto con esta guía. Es un espacio de trabajo y no una evidencia de contribuciones anteriores de Ritwornz. No se ha quitado ningún archivo del proyecto base.

Conservar el historial de autores. Solo hacer commits cuando exista un cambio o una comprobación documentada realmente realizada. No copiar archivos idénticos para simular avances.

## Preparación

1. Clonar `https://github.com/Nicricht/Edubio360.git`.
2. Abrir la única rama de trabajo: `git switch --track origin/ritwornz/proyecto-completo`.
3. En la carpeta `ep2`, ejecutar `npm ci`, `npm run test:run` y `npm run build`.
4. Revisar los archivos asignados, realizar correcciones o agregar pruebas relevantes.
5. Registrar los cambios propios y abrir un Pull Request hacia `ep2/react-vite-typescript`.
6. No modificar `main` ni forzar cambios en la rama final. Si cambia la cantidad de pruebas o la cobertura, actualizar también el informe.

## Áreas de trabajo contenidas en esta rama

### 1. Páginas públicas

**Archivos:** `ep2/src/pages/Inicio.tsx`, `Nosotros.tsx`, `Novedades.tsx`, `NovedadDetalle.tsx`, `Contacto.tsx`.

**Trabajo:** contrastar contenido, enlaces e imágenes con EP1; revisar navegación desde las vistas públicas; corregir problemas detectados. Verificar que las novedades y sus detalles correspondan a los datos esperados.

**Evidencia:** descripción de las diferencias encontradas y capturas antes/después de las correcciones, cuando existan.

### 2. Componentes

**Archivos:** `ep2/src/components/atoms/`, `molecules/` y `organisms/`.

**Trabajo:** revisar reutilización y propiedades tipadas, accesos del encabezado, tarjetas, estados vacíos y consistencia visual. Si hace cambios funcionales, comprobarlos con pruebas.

**Evidencia:** componentes revisados, motivo de cada ajuste y resultados de pruebas relacionadas.

### 3. Catálogo

**Archivos:** `ep2/src/data/seed.ts`, `ep2/src/utils/filters.ts`, `ep2/src/pages/Catalogo.tsx`, `DetalleOferta.tsx`, `ep2/src/components/molecules/OfertaCard.tsx`.

**Trabajo:** verificar las 21 ofertas originales, búsquedas sin tildes, filtros combinados, estados vacíos y páginas de detalle con identificador inválido. Corregir datos o condiciones que no correspondan.

**Evidencia:** casos revisados, problemas encontrados y pruebas ejecutadas.

### 4. Responsividad

**Archivos:** `ep2/src/components/organisms/SiteHeader.tsx`, `ep2/src/pages/Registro.tsx`, `Catalogo.tsx`, `AdminOfertaForm.tsx` y estilos relacionados.

**Trabajo:** verificar visualmente a 360 px, 768 px y 1366 px. Revisar navegación, desbordes, tablas, botones y formularios; corregir los defectos observados.

**Evidencia:** capturas reales por ancho de pantalla y resultados después de los cambios.

### 5. Pruebas

**Archivos:** `ep2/src/pages/*.test.tsx`, `ep2/src/components/**/*.test.tsx` y pruebas nuevas cuando sean necesarias.

**Trabajo:** aumentar la verificación de `NovedadDetalle`, `Perfil`, `Notificaciones` y `Registro`, que tienen rutas o situaciones menos recorridas. Cada caso nuevo debe tener acción y resultado esperado claros.

**Evidencia:** reporte de Vitest, pruebas aprobadas y explicación de qué error detectan.

### 6. Documentación

**Archivos:** `ep2/docs/TESTING_EP2.md`, `ERS_EP2.md` y evidencias del proyecto.

**Trabajo:** contrastar el informe con los resultados vigentes, incorporar evidencias visuales auténticas, mantener una lista de casos pendientes y actualizar requisitos solo cuando cambien funcionalidades.

**Evidencia:** fuentes de capturas, resultados reproducibles y cambios documentales comprobables.

### 7. Accesibilidad

**Archivos:** formularios públicos, `SiteHeader.tsx`, `OfertaCard.tsx`, `Contacto.tsx` y `Registro.tsx`.

**Trabajo adicional:** verificar textos alternativos, etiquetas, navegación por teclado, foco visible y mensajes accesibles. Corregir problemas observados; agregar pruebas cuando corresponda.

**Evidencia:** lista de comprobaciones y comportamiento corregido.

### 8. Rutas y estados

**Archivos:** `ep2/src/App.tsx`, `DetalleOferta.tsx`, `NoEncontrada.tsx`, `Login.tsx`, `Perfil.tsx` y vistas protegidas.

**Trabajo adicional:** verificar rutas públicas, parámetros incorrectos, acceso sin sesión y redirecciones por perfil. Agregar pruebas de casos negativos que no estén cubiertos.

**Evidencia:** rutas verificadas, respuestas esperadas y resultados de las pruebas.

## Integración

Trabajar en las ocho áreas desde `ritwornz/proyecto-completo`, sin repetir cambios artificialmente. Abrir un Pull Request por conjunto de cambios reales. Antes de integrar, ejecutar las pruebas y la compilación. Nicolás revisa la integración a EP2 y ambos deben comprender el proyecto completo para la presentación individual.

## Entrega y atribución

Los commits de EP1 de Ritwornz permanecen en el historial original. Los commits nuevos de EP2 deben representar las modificaciones que efectivamente realice. Las ramas creadas como punto de partida no cuentan por sí mismas como trabajo desarrollado.
