# Odoo repository template

Template público estilo OCA para repositorios Odoo de Dipleg-SA.

El repositorio combina dos capas claramente separadas:

- Gobernanza en `.github/` y `docs/`: Pull Requests, ownership y promoción `19.0-dev -> 19.0-stag -> 19.0`.
- Un módulo base en `module/`, con todos sus subdirectorios y sin código de negocio, secretos ni datos de producción.

## Inicio

1. Crear un repositorio usando este template.
2. Completar `module/` según el módulo real; si se requiere un nombre técnico distinto, renombrar el directorio manteniendo su estructura.
3. Ejecutar `bootstrap-odoo-repo.sh --repo OWNER/NAME` desde el repositorio de automatización.
4. Verificar el resultado con `verify-odoo-repo.sh --repo OWNER/NAME`.

La gobernanza preserva la cronología mediante Pull Requests y no exige aprobaciones de terceros para el modelo actual de un único desarrollador.
