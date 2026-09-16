# Sistema de diseño · Ontikos

Sitio estático. Se publica con GitHub Pages en **sistema.ontikos.com**.

| Ruta | Documento |
|---|---|
| `/` | portada |
| `/ds/` | **Ontikos · Sistema de funcionamiento** — 28 reglas, cada una con su verificación y sus láminas |
| `/dsr/` | **RetiCash · Sistema · v5** — secciones 00 a 14 |
| `/erp/` | **insurance.ontikos** — el wireframe vigente del Director y la aplicación |

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
