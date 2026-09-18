# Control de Consumibles

**Sistema web local para control y recuperación de consumibles en operaciones de almacén.**

**Autor:** César Medina  
**Año:** 2026  
**Repositorio:** Cmedina19/control-consumibles-almacen

## ¿Qué es?

Este proyecto nació de una necesidad operativa real: llevar un control auxiliar sobre consumibles que salen del almacén y dar seguimiento a la recuperación física de envases, recipientes o unidades.

La aplicación está pensada como una capa auxiliar al ERP. El ERP continúa siendo el sistema de registro de las órdenes de trabajo y las emisiones; esta aplicación facilita el seguimiento operativo, los pendientes y la recuperación.

## Funciones del demo

- Dashboard de emisiones, OT MTO, entregas, recuperaciones y pendientes.
- Catálogo maestro de consumibles.
- Importación de reportes ERP en CSV.
- Seguimiento por OT y número de parte.
- Registro de recuperaciones físicas.
- Reporte exportable a CSV.
- Revisión básica de calidad de datos.
- Respaldo local mediante JSON y LocalStorage.

## Reglas principales

Solo se procesan registros que cumplan:

1. Tipo = STK-MTL.
2. La OT comienza con MTO.
3. El número de parte existe y está activo.
4. La cantidad es mayor a cero.
5. La transacción Trans. no está duplicada.

Las OT de tipo SRV y otros registros fuera de las reglas se ignoran.

## Recuperación física

El balance se calcula como:

Pendiente = Entregado - Recuperado

La recuperación representa la unidad física, envase o recipiente que debe regresar al almacén.

## Uso

Abre index.html en un navegador moderno. No requiere servidor ni instalación para ejecutar el demo.

## Importante

Esta versión pública es un demo de portafolio y utiliza números de parte y datos ficticios. No incluye reportes ERP reales ni información confidencial de una empresa.

La versión operativa utilizada en un entorno empresarial puede contener reglas, catálogos y datos diferentes.

## Tecnologías

HTML5, CSS3, JavaScript, LocalStorage, CSV y JSON.

## Autor

**César Medina**

Proyecto desarrollado como parte de mi portafolio de programación y automatización de procesos operativos.

## Licencia

MIT License. Consulta LICENSE para los términos completos.
