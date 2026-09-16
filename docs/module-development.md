# Desarrollo de módulos Odoo

## Estructura

Cada addon vive bajo `addons/<nombre_tecnico>/`, siguiendo una estructura simple y reconocible:

```text
addons/<nombre_tecnico>/
├── __init__.py
├── __manifest__.py
├── models/
├── security/
├── tests/
└── views/
```

## Primeros pasos

1. Renombrar `addons/example_module/` con el nombre técnico definitivo.
2. Reemplazar nombre, resumen, descripción y dependencias en `__manifest__.py`.
3. Definir modelos en `models/` e importarlos desde `models/__init__.py`.
4. Agregar vistas y datos de seguridad en `views/` y `security/`.
5. Agregar pruebas en `tests/` e importarlas cuando existan casos verificables.
6. Mantener la gobernanza del repositorio en `.github/` y el flujo de ramas documentado en `docs/branch-flow.md`.

El scaffold no contiene modelos de negocio, datos de clientes, credenciales ni configuraciones de producción.
