# Flujo de ramas por entorno

Este repositorio usa tres ramas persistentes:

| Rama | Entorno | Entrada permitida |
| --- | --- | --- |
| `19.0-dev` | Desarrollo | Ramas de trabajo mediante Pull Request |
| `19.0-stag` | Staging | Pull Request desde `19.0-dev` |
| `19.0` | Producción | Pull Request desde `19.0-stag` |

Las ramas de entorno requieren Pull Request, no permiten force-push ni eliminación y exigen que las conversaciones estén resueltas. El workflow `validate-promotion` comprueba el origen y destino del Pull Request.

La protección de ramas o el ruleset y el status check deben habilitarse después de que el workflow exista en las tres ramas. No se incluyen credenciales, secretos, bases de datos ni operaciones sobre servidores.
