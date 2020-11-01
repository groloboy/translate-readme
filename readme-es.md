# Traducir la acción Léame

**Acción de GitHub para traducir Readme a cualquier idioma**

Esta es una acción de GitHub que traduce automáticamente el archivo Léame en su repositorio a un idioma específico.

_Una sumisión para el[DEV: ¡Acciones de GitHub para código abierto!](https://dev.to/devteam/announcing-the-github-actions-hackathon-on-dev-3ljn)hackathon_

## Preparar

1.  **Agregar un archivo de flujo de trabajo**a su proyecto (p. ej.`.github/workflows/readme.yml`):

    ```yml
    name: Translate Readme

    on:
      push:
        branches:
          - main
          - master

    jobs:
      build:
        runs-on: ubuntu-latest
        steps:
          - uses: actions/checkout@v2
          - name: Setup Node.js
            uses: actions/setup-node@v1
            with:
              node-version: 12.x
          - name: Adding License
            uses: dephraiim/translate-readme@v1
            with:
              LANG: la
              # ISO Langusge Code.
              # Supported Languages below
    ```

## Configuración

### Opciones

Puede configurar la acción aún más con las siguientes opciones:

-   `LANG`: El idioma al que desea traducir su archivo Léame. El predeterminado es chino simplificado. (Soy ghanés) Los idiomas admitidos se pueden encontrar a continuación.
    (defecto:`zh-CH`) (requerido:`false`)

## Idiomas admitidos

Los idiomas admitidos se pueden encontrar aquí<https://cloud.google.com/translate/docs/languages>

### Cuestiones

Cheque[aquí](https://github.com/dephraiim/translate-readme/issues/1)para problemas relacionados con esta acción.

### Desarrollo

¡Las sugerencias y contribuciones siempre son bienvenidas!

### LICENCIA

[CON](./LICENSE)
