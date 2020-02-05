# 2-ej-cond-est-feb-2020

Instrucciones:

1. Misma persona que aceptó invitación a la tarea de github classroom pasada debe aceptar la invitación a esta tarea. Recuerden que sólo una persona integrante de cada equipo debe aceptar.

2. Invitar a sus integrantes de su equipo al repo.

3. Resuelvan por equipos los ejercicios de programación de la nota de condición y estabilidad [1.3.Condicion_de_un_problema_y_estabilidad_de_un_algoritmo.ipynb](1.3.Condicion_de_un_problema_y_estabilidad_de_un_algoritmo.ipynb).

4. Aprovechen esta tarea para construir su botón de [binder](https://mybinder.org/). Para esto apóyense de lo siguiente:

a. `Admin` debe crear un repo público y añadir el siguiente archivo con nombre `Dockerfile` a la raíz de éste repo:


```
FROM palmoreck/jupyterlab_binder:1.1.0
ARG NB_USER=jovyan
ARG NB_UID=1000
ENV USER ${NB_USER}
ENV NB_UID ${NB_UID}
ENV HOME /home/${NB_USER}
COPY . ${HOME}
USER root
RUN chown -R ${NB_UID} ${HOME}
USER ${NB_USER}
```

b. Coloquen en el `README.md` la siguiente línea haciendo los cambios correspondientes con el nombre de su organización y de su repo:

```
[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/<aquí colocar user de github>/<aquí colocar nombre de mi repo>/master?urlpath=lab)
```


Prueben su botón dando click en él y resuelvan lo descrito en 3. de arriba para los ejercicios nota. Deben hacer `commit`'s, `add`'s, `pull`'s y `push`'s al repo privado donde se encuentra la nota.
