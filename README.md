# Impagos

Prediccion de impagos utilizando machine learning con el dataset [default of credit card clients Data Set](https://archive.ics.uci.edu/ml/datasets/default+of+credit+card+clients)

Para crear la imagen del contenedor con el software necesario ejecute lo siguiente:

```bash
docker build -f docker/Dockerfile -t jorgelojam/impagos:latest .
```

Para ejecutar el contenedor creado ejecute lo siguiente:

```bash
docker run -p 8888:8888 jorgelojam/impagos start.sh jupyter lab
```

Posterior al arranque en la terminal va a salir un mensaje con la url que se tiene que abrir en el navegador, dentro del navegador ingresar al directorio src y abrir el notebook prediccion.ipynb