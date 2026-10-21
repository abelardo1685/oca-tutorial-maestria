# OCA en Python

Implementación didáctica en Python, en un solo cuaderno, de la técnica de agrupamiento basada en optimización (Optimization-based Clustering Approach, OCA) para seleccionar realizaciones representativas en la delineación probabilística de zonas de protección de pozos.

Rodríguez-Pretelín, A., Nowak, W. y Morales-Casique, E. (2022). Optimization-based clustering of random fields for computationally efficient and goal-oriented uncertainty quantification. Concept and demonstration for delineation of wellhead protection areas in transient aquifers. *Advances in Water Resources*. [doi 10.1016/j.advwatres.2022.104146](https://doi.org/10.1016/j.advwatres.2022.104146)

## Contenido

| Archivo | Qué es |
|---|---|
| `OCA.ipynb` | El cuaderno completo, ya ejecutado. Simula el ensamble con `rrwpt`, calcula las envolventes convexas y el mapa probabilístico, extrae las características, define la función de costo, implementa OMOPSO función por función, elige la solución de mejor compromiso y verifica la delineación. |

## Cómo correrlo

```
pip install numpy scipy matplotlib jupyter
pip install git+https://github.com/abelardo1685/rrwpt.git
jupyter notebook OCA.ipynb
```

La primera vez el cuaderno simula 200 realizaciones en una malla de 100 por 100 celdas, lo que toma cerca de minuto y medio, y las guarda en `datos_oca.npz`. OMOPSO con los parámetros del script MATLAB (1 000 iteraciones y 100 partículas) toma poco más de un minuto. Tiempos medidos en una laptop con un solo núcleo.

## Licencia

MIT. Autor Abelardo Rodríguez-Pretelín, incluida la implementación de OMOPSO para la OCA.
