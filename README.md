# Aeronáutica para el futuro: Innovación y Diseño Aplicado

### ¿Qué aeronave puede aterrizar en tu planeta?

Un recorrido por las fases del Entry, Descent & Landing de la misión Mars Science Laboratory.

**InspiraSTEM 2026 · 5 módulos de 60 minutos · 3 días**
Instructores: **Patricia Ortíz** (NASA Armstrong Flight Research Center) y **Oscar Tejada** (SKY Airline)

---

El 6 de agosto de 2012, un vehículo de más de tres toneladas entró en la atmósfera de Marte a casi 5,8 km/s y, siete minutos después, dejó el rover Curiosity apoyado suavemente sobre el suelo. Nadie lo pilotó: la señal desde la Tierra tardaba unos trece minutos en llegar. Todo estaba decidido de antemano.

Este taller toma esa secuencia como punto de partida. **Cada equipo recibe un entorno planetario y una flota de cinco aeronaves**, y trabaja sobre una pregunta concreta: cuál de las cinco puede aterrizar ahí. La respuesta se construye fase por fase —entrada atmosférica, descenso en paracaídas y aterrizaje propulsado— y se sostiene con números.

Los cinco entornos son distintos entre sí, así que cada equipo llega a una conclusión diferente. Comparar esas conclusiones es el contenido del cierre.

---

## Empezar

1. **Ten una cuenta de Google.** Es todo lo que se necesita. No hay nada que instalar.
2. **Abre el módulo que corresponda** con el botón de la tabla de abajo. Se abre en el navegador.
3. **En Colab: `Archivo → Guardar una copia en Drive`.** Trabaja sobre tu copia.
4. **Ejecuta la primera celda.** Si imprime el nombre de tu entorno asignado, ya está todo listo.

---

## Módulos

| Módulo | Contenido | Abrir | Solución |
|---|---|---|---|
| **1 — Fundamentos de vuelo** | Las cuatro fuerzas, Bernoulli, perfil y ángulo de ataque. Trabajo de investigación en vuelo | [slides](modulo1-fundamentos/slides_modulo1.pdf) | — |
| **2 — Entrada atmosférica** | Arrastre hipersónico, coeficiente balístico, cargas límite | [Abrir en Colab](https://colab.research.google.com/github/USUARIO/InspiraSTEM2026-Aeronautica/blob/main/modulo2-entrada/entrada.ipynb) | [ver](modulo2-entrada/entrada_SOLUCION.ipynb) |
| **3 — Descenso en paracaídas** | Doseles supersónicos, carga de apertura, velocidad terminal | [Abrir en Colab](https://colab.research.google.com/github/USUARIO/InspiraSTEM2026-Aeronautica/blob/main/modulo3-descenso/descenso.ipynb) | [ver](modulo3-descenso/descenso_SOLUCION.ipynb) |
| **4 — Aterrizaje propulsado** | Relación empuje-peso, Tsiolkovsky, presupuesto de propelente | [Abrir en Colab](https://colab.research.google.com/github/USUARIO/InspiraSTEM2026-Aeronautica/blob/main/modulo4-aterrizaje/aterrizaje.ipynb) | [ver](modulo4-aterrizaje/aterrizaje_SOLUCION.ipynb) |
| **5 — Proyecto final** | Consolidación de resultados y presentaciones | [plantilla de la ficha](modulo5-proyecto/) | — |

Cada notebook es independiente: se abre y se ejecuta por su cuenta, sin necesidad de haber terminado el anterior.

---

## Qué se evalúa en cada módulo

Los tres módulos centrales exploran tres parámetros de diseño por fase, cada uno con dos gráficas de contraste.

| Módulo | Parámetro 1 | Parámetro 2 | Parámetro 3 |
|---|---|---|---|
| **Entrada** | Área frontal del escudo | Ángulo de trayectoria de entrada | Masa de entrada |
| **Descenso** | Área del dosel | Coeficiente de arrastre del dosel | Masa liberada en la separación |
| **Aterrizaje** | Empuje total | Impulso específico | Masa de propelente |

---

## Los cinco entornos

Se asigna un entorno por equipo. Los cinco cubren un rango de gravedad de 1,35 a 18,5 m/s² y de densidad atmosférica de cuatro órdenes de magnitud, de modo que ninguna arquitectura de descenso resuelve los cinco casos.

| Equipo | Entorno asignado | Gravedad [m/s²] | Densidad [kg/m³] | Escala [m] |
|---|---|---|---|---|
| Equipo 1 | Exoplaneta Kepler-452b | 18,50 | 2,800 | 7 000 |
| Equipo 2 | Tierra | 9,81 | 1,225 | 8 500 |
| Equipo 3 | Titán | 1,35 | 5,430 | 20 000 |
| Equipo 4 | Venus | 8,87 | 65,000 | 15 900 |
| Equipo 5 | Marte (Monte Olimpo, 21 km de altitud) | 3,71 | 0,002 | 11 100 |

Datos en [`datos/planetas.csv`](datos/planetas.csv).

---

## Las cinco aeronaves

La misma flota para los cinco equipos. Va desde una etapa pesada de alto empuje hasta una sonda compacta que frena casi exclusivamente por arrastre, de modo que la elección no es evidente sin simular. La masa indicada es la estructural; la masa total en la entrada suma el propelente.

| Aeronave | Masa estructural [kg] | Área escudo [m²] | Área paracaídas [m²] | Empuje [kN] | Propelente [kg] |
|---|---|---|---|---|---|
| Clase Atlas | 6 000 | 12,0 | 80 | 150 | 2 000 |
| Clase Terran | 4 500 | 8,0 | 60 | 60 | 900 |
| Clase Huygens | 1 200 | 3,0 | 15 | 3 | 100 |
| Clase Venera | 5 500 | 2,5 | 5 | 1 | 50 |
| Clase Manta | 2 800 | 35,0 | 800 | 40 | 1 200 |

Datos en [`datos/aeronaves.csv`](datos/aeronaves.csv).

> Para que las cinco configuraciones sean comparables entre sí, el modelo adopta los mismos coeficientes de arrastre e impulso específico y una misma condición de llegada a la interfaz atmosférica. Estos valores se declaran de forma explícita en el archivo de trabajo y son supuestos del taller, no datos de vuelo.

---

## Entregable por equipo

Una ficha de decisión y una presentación de 3 a 4 minutos.

**La ficha** reúne lo producido en los tres módulos centrales:

| Aeronave | Carga de pico [g] | Presión dinámica [kPa] | Carga de apertura [kN] | Velocidad terminal [m/s] | Empuje-peso [–] | Margen de encendido [s] |
|---|---|---|---|---|---|---|
| Clase Atlas | | | | | | |
| Clase Terran | | | | | | |
| Clase Huygens | | | | | | |
| Clase Venera | | | | | | |
| Clase Manta | | | | | | |

Más **dos gráficas** tomadas de los módulos que respalden la recomendación: la trayectoria altitud-velocidad de la fase de entrada y el balance de la fase propulsada.

**La presentación** se organiza en tres partes:

- **Introducción:** qué entorno les tocó y por qué aterrizar ahí es difícil.
- **Metodología:** qué parámetros se variaron, qué se simplificó y qué supuestos se declaran.
- **Resultados y discusión:** qué aeronave recomiendan, con qué indicador la eligieron y qué criterio descartó a las demás.

---

## Objetivos del taller

Al terminar el taller, el estudiante será capaz de:

1. Explicar las fases del Entry, Descent & Landing de una misión planetaria e identificar qué mecanismo frena el vehículo en cada una.
2. Construir y ajustar un modelo numérico de descenso, evaluando los parámetros de diseño que gobiernan cada fase.
3. Recomendar una configuración de vehículo para un entorno planetario dado y defenderla con evidencia numérica ante un público técnico.

---

## Perfil del estudiante

El taller está dirigido a estudiantes universitarios de ingeniería mecánica, aeronáutica o aeroespacial, idealmente de tercer año en adelante. Un estudiante de otra área con interés en el tema puede seguirlo completo.

**Conocimiento previo esperado**

- Física básica: leyes de Newton, cinemática y energía.
- Álgebra y trigonometría.
- Haber programado alguna vez, en cualquier lenguaje. No se requiere saber Python: se entrega un archivo de trabajo ya armado en el que solo se completan las partes marcadas.

**Qué se debe llevar**

- Computadora portátil con navegador web y una cuenta de Google. No hay nada que instalar: se trabaja en un entorno de Python en línea que corre en el navegador y funciona igual en cualquier sistema operativo.
- Disposición para trabajar en equipo y presentar el resultado en público durante 3 o 4 minutos.

---

## Material de estudio

El material previo suma alrededor de una hora y es intencionalmente ligero: el trabajo fuerte ocurre en el taller. Todos los recursos son gratuitos.

| Tema | Recurso |
|---|---|
| Entorno de trabajo | [Introducción a los notebooks de Python en línea — Google Colab](https://colab.research.google.com/notebooks/intro.ipynb) |
| Física | [Khan Academy — Fuerzas y leyes de Newton (en español)](https://es.khanacademy.org/science/physics/forces-newtons-laws) |
| Aerodinámica | [NASA Glenn — Beginner's Guide to Aeronautics](https://www1.grc.nasa.gov/beginners-guide-to-aeronautics/) |
| Aerodinámica | [NASA Glenn — FoilSim Student, simulador interactivo de perfil alar](https://www1.grc.nasa.gov/beginners-guide-to-aeronautics/foilsimstudent/) |
| Atmósferas | [NASA Glenn — Modelo de la atmósfera de Marte](https://www.grc.nasa.gov/www/k-12/airplane/atmosmrm.html) |
| Atmósferas | [NASA Glenn — AtmosModeler, simulador de atmósfera](https://www.grc.nasa.gov/www/k-12/airplane/atmosi.html) |
| Propulsión | [NASA Glenn — Beginner's Guide to Rockets](https://www.grc.nasa.gov/www/k-12/rocket/) |
| Propulsión | [Ecuación del cohete de Tsiolkovski — Wikipedia en español](https://es.wikipedia.org/wiki/Ecuaci%C3%B3n_del_cohete_de_Tsiolkovski) |
| La misión | [NASA JPL — Video «Curiosity's Seven Minutes of Terror»](https://www.jpl.nasa.gov/videos/curiositys-seven-minutes-of-terror/) |
| La misión | [NASA Science — Mars Science Laboratory: Curiosity Rover](https://science.nasa.gov/mission/msl-curiosity/) |
| La misión | [Way et al. — «MSL: Entry, Descent, and Landing System Performance», NTRS 20090007730](https://ntrs.nasa.gov/citations/20090007730) |

---

## Estructura del repositorio

```
├── README.md
├── syllabus.pdf
├── datos/
│   ├── planetas.csv                 Los cinco entornos
│   ├── aeronaves.csv                Las cinco aeronaves
│   ├── msl_edl_referencia.csv       Valores de referencia de la misión
│   └── fuentes.md                   Procedencia de cada dato
├── modulo1-fundamentos/
│   └── slides_modulo1.pdf
├── modulo2-entrada/
│   ├── entrada.ipynb
│   ├── entrada_SOLUCION.ipynb
│   └── slides_modulo2.pdf
├── modulo3-descenso/
│   ├── descenso.ipynb
│   ├── descenso_SOLUCION.ipynb
│   └── slides_modulo3.pdf
├── modulo4-aterrizaje/
│   ├── aterrizaje.ipynb
│   ├── aterrizaje_SOLUCION.ipynb
│   └── slides_modulo4.pdf
└── modulo5-proyecto/
    ├── ficha_decision.xlsx          Plantilla de la tabla comparativa
    └── entrega_diapositivas.txt     Enlace del formulario de entrega
```

---

## Datos

Los valores de la misión provienen de artículos primarios de NASA/JPL y NASA Langley, listados en [`datos/fuentes.md`](datos/fuentes.md). Fijan las condiciones de entrada del modelo y aportan los valores de referencia marcados en las gráficas: ventana de despliegue del dosel, desaceleración de pico y velocidad de entrega a la fase propulsada.

Los coeficientes de arrastre, el impulso específico y las características de las cinco aeronaves son supuestos didácticos del taller y están declarados como tales.

---

*Material preparado para InspiraSTEM 2026. Los datos de la misión Mars Science Laboratory son de dominio público (NASA/JPL).*
