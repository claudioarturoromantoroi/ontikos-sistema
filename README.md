# Sistema de diseño · Ontikos

Sitio estático. Se publica con GitHub Pages en **sistema.ontikos.com**.

| Ruta | Documento |
|---|---|
| `/` | portada |
| `/ds/` | **Ontikos · Sistema de funcionamiento** — 28 reglas, cada una con su verificación y sus láminas |
| `/dsr/` | **RetiCash · Sistema · v5** — secciones 00 a 14 |
| `/erp/` | **insurance.ontikos** — el wireframe vigente del Director y la aplicación |
| `/erp/wireframes/` | los wireframes 01–04 de Dirección, copia de `ERP-CRM/wireframes/` · **01–03 abren sin estilos**: piden `assets/carbon.css` y el favicon, que no se publicaron |
| `/carbondesign/` | **Ontikos · el marco** — El Futuro armado sobre el marco (`index.html` = `marco.html`) |
| `/estado/` | **Estado medido · Ontikos** |
| `/futuro/` · `/panel-actos/` · `/panel-lista/` · `/panel-patron/` · `/pulso/` | sondas de El Futuro (22–23 sep): card 1, el panel de Colocación, la lista de auditoría, el patrón a nivel CEO, las formas del Pulso |
| `/anatomia/` · `/cruda/` · `/escala/` · `/repertorio/` | sondas del 21 sep: zonas de la tarjeta, Carbon contra «simplón y crudo», el hueco, el repertorio |
| `/ontikos/` | **Ontikos — Mi Semana** · no pertenece a `ERP-CRM/` |

Las sondas son bancos para elegir sobre el render, no pantallas del producto. Tabla
puesta al día el 24-sep-2026, contra `ls` y el `<title>` de cada ruta.

## Esto no se edita aquí

Los dos documentos viven en el repositorio **RetiCash**, en `sistema/`, y de ahí
se derivan con `sistema/publicar.py`. Editar los archivos de este repositorio
crea una segunda copia que se separa de la primera sin que nadie lo note — que
es exactamente la deuda que el sistema quiere evitar.

Para actualizar: se cambia el documento en RetiCash, se corre `publicar.py`, y
se copia el resultado aquí.

## `/erp/` sigue la misma regla

Sus dos archivos tampoco se editan aquí. Las fuentes viven en el monorepo
**Ontikos**, en `ERP-CRM/`:

| Aquí | Fuente |
|---|---|
| `/erp/polizario.html` | `ERP-CRM/producto/app/`, con `vite build` y las hojas en línea |

Los dos son **autocontenidos**: la tipografía —DM Sans e IBM Plex Mono—, la marca
y `@carbon/charts` viajan dentro del archivo, así que abren sin red y sin depender
de ningún tercero.

Están aquí y no en Pages del repositorio `Ontikos` porque **`Ontikos` es privado**,
y GitHub Pages desde un repositorio privado exige plan de pago. Éste es público, que
es exactamente por lo que el sistema se publica desde aquí.

## Qué le quita `publicar.py` al documento de RetiCash

Dos bloques que no deben salir a un sitio público:

- **Pendientes abiertos, del maestro** — enumera pendientes de seguridad con su
  ubicación en la base de datos y en el código.
- **Deriva detectada · entorno** — publica las rutas de despliegue del servidor.

El script verifica la salida contra diez términos de servidor y se niega a
terminar si encuentra alguno.

## Lo que no está

Las tres muestras vivas del vendedor eran iframes a la aplicación en
producción. Aquí aparecen como un recuadro rotulado: no se pueden servir fuera
de ese host.
