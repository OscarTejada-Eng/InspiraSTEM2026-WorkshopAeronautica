# Aeronáutica para el futuro: Innovación y Diseño Aplicado

### ¿Qué aeronave puede aterrizar en tu planeta?

Un recorrido por las fases del Entry, Descent & Landing de la misión Mars Science Laboratory.

**InspiraSTEM 2026 · 3 días**

Instructores: Patricia Ortíz (NASA Armstrong Flight Research Center) y Oscar Tejada (SKY Airline)

---

## Resumen del taller

El 6 de agosto de 2012, un vehículo de más de tres toneladas entró en la atmósfera de Marte a casi 5,8 km/s y, siete minutos después, dejó el rover Curiosity apoyado suavemente sobre el suelo. Nadie lo pilotó: la señal desde la Tierra tardaba unos trece minutos en llegar. Todo estaba decidido de antemano.

Este taller toma esa secuencia como punto de partida. Cada equipo recibe un entorno planetario y una flota de cinco aeronaves, y trabaja sobre una pregunta concreta: cuál de las cinco puede aterrizar ahí. La respuesta se construye fase por fase —entrada atmosférica, descenso en paracaídas y aterrizaje propulsado— y se sostiene con números.

Los cinco entornos son distintos entre sí, así que cada equipo llega a una conclusión diferente. Comparar esas conclusiones es el contenido del cierre.

No es una clase expositiva. Cada módulo de 60 minutos alterna explicaciones cortas con trabajo en la computadora, y el taller cierra con una presentación de 3 a 4 minutos por equipo.

---

## Perfil del estudiante

El taller está dirigido a estudiantes universitarios de ingeniería mecánica, aeronáutica o aeroespacial, idealmente de tercer año en adelante. Un estudiante de otra área con interés en el tema puede seguirlo completo.

### Conocimiento previo esperado

- Física básica: leyes de Newton, cinemática y energía.
- Álgebra y trigonometría.
- Haber programado alguna vez, en cualquier lenguaje. No se requiere saber Python: se entrega un archivo de trabajo ya armado en el que solo se completan las partes marcadas.

### Qué se debe llevar

- Computadora portátil con navegador web y una cuenta de Google. No hay nada que instalar: se trabaja en un entorno de Python en línea que corre en el navegador y funciona igual en cualquier sistema operativo.
- Disposición para trabajar en equipo y presentar el resultado en público durante 3 o 4 minutos.

---

## Objetivos del taller

Al terminar el taller, el estudiante será capaz de:

1. Explicar las fases del Entry, Descent & Landing de una misión planetaria e identificar qué mecanismo frena el vehículo en cada una.
2. Construir y ajustar un modelo numérico de descenso, evaluando los parámetros de diseño que gobiernan cada fase.
3. Recomendar una configuración de vehículo para un entorno planetario dado y defenderla con evidencia numérica ante un público técnico.

---

## Descripción del proyecto

El proyecto es uno solo y avanza a lo largo de los cinco módulos. Cada equipo recibe un entorno planetario y la misma flota de cinco aeronaves, cada una con su escudo térmico, su paracaídas y su sistema propulsivo.

En cada módulo el equipo evalúa una fase del descenso y obtiene, para las cinco aeronaves, los indicadores que gobiernan esa fase. Al final consolida los tres conjuntos de resultados y recomienda una configuración.

El resultado final no es una única gráfica, sino una decisión sustentada: una tabla que compara las cinco aeronaves en los indicadores de las tres fases, respaldada por las gráficas obtenidas en los módulos.

### Los cinco entornos

Se asigna un entorno por equipo. Los cinco cubren un rango de gravedad de 1,35 a 18,5 m/s² y de densidad atmosférica de cuatro órdenes de magnitud, de modo que ninguna arquitectura de descenso resuelve los cinco casos.

| Equipo | Entorno asignado | Gravedad [m/s²] | Densidad [kg/m³] | Escala [m] |
|---|---|---|---|---|
| Equipo 1 | Exoplaneta Kepler-452b | 18,50 | 2,800 | 7 000 |
| Equipo 2 | Tierra | 9,81 | 1,225 | 8 500 |
| Equipo 3 | Titán | 1,35 | 5,430 | 20 000 |
| Equipo 4 | Venus | 8,87 | 65,000 | 15 900 |
| Equipo 5 | Marte (Monte Olimpo, 21 km de altitud) | 3,71 | 0,002 | 11 100 |

### Las cinco aeronaves

La misma flota para los cinco equipos. Va desde una etapa pesada de alto empuje hasta una sonda compacta que frena casi exclusivamente por arrastre, de modo que la elección no es evidente sin simular. La masa indicada es la estructural; la masa total en la entrada suma el propelente.

| Aeronave | Masa estructural [kg] | Área escudo [m²] | Área paracaídas [m²] | Empuje [kN] | Propelente [kg] |
|---|---|---|---|---|---|
| Clase Atlas | 6 000 | 12,0 | 80 | 150 | 2 000 |
| Clase Terran | 4 500 | 8,0 | 60 | 60 | 900 |
| Clase Huygens | 1 200 | 3,0 | 15 | 3 | 100 |
| Clase Venera | 5 500 | 2,5 | 5 | 1 | 50 |
| Clase Manta | 2 800 | 35,0 | 800 | 40 | 1 200 |

> **Sobre los datos.** Los valores de los entornos y de las aeronaves, así como los coeficientes de arrastre y el impulso específico que usa el modelo, tienen fines de entrenamiento: están construidos para que el ejercicio funcione y no corresponden necesariamente a los de la misión real ni a los de los cuerpos planetarios citados.

---

## Módulos

Los archivos de trabajo de cada día están en su carpeta correspondiente dentro de este repositorio, junto con las soluciones y las diapositivas. Se abren en Google Colab desde el navegador; no hay nada que descargar ni instalar.

**Módulo 1 — Fundamentos de vuelo y trabajo de investigación**
Las cuatro fuerzas del vuelo y su equilibrio en cada fase. El principio de Bernoulli, el perfil aerodinámico y el ángulo de ataque. Gestión de proyectos de investigación de vuelo en un centro de la NASA. Formación de equipos y entrega del entorno asignado.

**Módulo 2 — Entrada atmosférica**
Disipación de la energía cinética por arrastre hipersónico y significado del coeficiente balístico. Se exploran el área frontal del escudo, el ángulo de trayectoria de entrada y la masa del vehículo, y se obtienen el factor de carga de pico y la presión dinámica máxima.

**Módulo 3 — Descenso en paracaídas**
Dinámica de doseles supersónicos y magnitud de la carga de inflado. Se exploran el área del dosel, su coeficiente de arrastre y la masa liberada en la separación del escudo, y se obtienen la carga de apertura y la velocidad terminal.

**Módulo 4 — Aterrizaje propulsado**
Transición del arrastre al empuje. Se exploran el empuje total, el impulso específico y la masa de propelente, y se obtienen la relación empuje-peso y el margen de encendido disponible.

**Módulo 5 — Proyecto final y presentaciones**
Consolidación de los resultados de los tres módulos anteriores, selección de las gráficas que sostienen la recomendación y presentación por equipo.

---

## Entregable por equipo

Una ficha de decisión y una presentación de 3 a 4 minutos.

La ficha reúne lo producido en los tres módulos centrales:

| Aeronave | Carga de pico [g] | Presión dinámica [kPa] | Carga de apertura [kN] | Velocidad terminal [m/s] | Empuje-peso [–] | Margen de encendido [s] |
|---|---|---|---|---|---|---|
| Clase Atlas | | | | | | |
| Clase Terran | | | | | | |
| Clase Huygens | | | | | | |
| Clase Venera | | | | | | |
| Clase Manta | | | | | | |

Más dos gráficas tomadas de los módulos que respalden la recomendación: la trayectoria altitud-velocidad de la fase de entrada y el balance de la fase propulsada.

La presentación se organiza en tres partes:

- **Introducción:** qué entorno les tocó y por qué aterrizar ahí es difícil.
- **Metodología:** qué parámetros se variaron, qué se simplificó y qué supuestos se declaran.
- **Resultados y discusión:** qué aeronave recomiendan, con qué indicador la eligieron y qué criterio descartó a las demás.

---

## Material de estudio

El material previo suma alrededor de una hora y es intencionalmente ligero: el trabajo fuerte ocurre en el taller. Todos los recursos son gratuitos.

| Recurso [Buscar en Internet] |
|---|
| Introducción a los notebooks de Python en línea — Google Colab |
| Khan Academy — Fuerzas y leyes de Newton |
| NASA Glenn — Beginner's Guide to Aeronautics |
| NASA Glenn — FoilSim Student, simulador interactivo de perfil alar |
| NASA Glenn — Modelo de la atmósfera de Marte |
| NASA Glenn — AtmosModeler, simulador de atmósfera |
| NASA Glenn — Beginner's Guide to Rockets |
| Ecuación del cohete de Tsiolkovski — Wikipedia en español |
| NASA JPL — Video «Curiosity's Seven Minutes of Terror» |
| NASA Science — Mars Science Laboratory: Curiosity Rover |
| Way et al. — «MSL: Entry, Descent, and Landing System Performance», NTRS 20090007730 |

---

*Material preparado para InspiraSTEM 2026. Los datos son con fines educativos y pueden no coincidir con la misión real.*
