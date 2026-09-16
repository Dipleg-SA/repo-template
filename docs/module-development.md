# Desarrollo de módulos Odoo

## Estructura

El módulo canónico vive únicamente bajo `module/`, siguiendo una estructura simple y reconocible:

```text
module/
├── __init__.py
├── __manifest__.py
├── models/
├── security/
├── tests/
└── views/
```

## Primeros pasos

1. Completar `module/`; si se requiere un nombre técnico distinto, renombrar el directorio conservando todos sus subdirectorios.
2. Reemplazar nombre, resumen, descripción y dependencias en `module/__manifest__.py`.
3. Definir modelos en `module/models/` e importarlos desde `models/__init__.py`.
4. Agregar vistas y datos de seguridad en `module/views/` y `module/security/`.
5. Agregar pruebas en `module/tests/` e importarlas cuando existan casos verificables.
6. Mantener la gobernanza del repositorio en `.github/` y el flujo de ramas documentado en `docs/branch-flow.md`.

El scaffold no contiene modelos de negocio, datos de clientes, credenciales ni configuraciones de producción.
