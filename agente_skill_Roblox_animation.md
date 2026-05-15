

---

# README — Protocolo oficial de biomecánica universal R15 para Moon Animator

Documento maestro del estado actual y de la arquitectura funcional del sistema biomecánico universal del rig R15.

## Objetivo general

Construir un **skill universal de animación corporal R15** capaz de generar poses, transiciones y animaciones completas de forma biomecánicamente coherente, reutilizable y compatible con Moon Animator.

Este sistema debe entender con precisión:

- qué hace cada joint
- qué hace cada eje
- qué rangos son naturales
- qué rangos son forzados
- qué rangos son inválidos
- cómo combinar joints de forma biomecánicamente humana
- cómo construir poses base reutilizables
- cómo expandir poses a animaciones completas
- cómo generar JSON consistente y confiable

## Alcance universal del sistema

Este skill está diseñado para funcionar como un **motor universal de animación corporal**, aplicable a cualquier familia de movimiento del rig R15, incluyendo:

- idle
- caminata
- carrera
- giro
- salto
- caída
- aterrizaje
- empuje
- jalón
- levantamiento
- interacción con objetos
- saludo
- señalamiento
- baile
- combate
- bloqueos
- golpes
- patadas
- transiciones expresivas
- acting corporal
- movimientos estilizados

El sistema no se organiza por animaciones aisladas, sino por **lógica biomecánica universal reutilizable**.

---

# Filosofía oficial del sistema

La lógica oficial del skill debe funcionar así:

**intención -> primitive base -> pose clave -> validación visual -> expansión -> timing -> JSON final**

El sistema no debe pensar primero en animaciones completas, sino en:

1. biomecánica aislada
2. lectura real de ejes
3. pose base
4. primitivas reutilizables
5. combinaciones biomecánicas
6. timing animatorio
7. salida JSON robusta

---

# Regla de oro del protocolo

Toda calibración y toda construcción animatoria deben respetar este principio:

- primero entender el cuerpo
- luego construir la pose
- luego validar la pose
- recién después expandir a animación completa

Nunca se debe construir una animación completa sin haber validado antes:

1. efecto real del joint
2. dirección real del eje
3. rango usable
4. rango forzado
5. rango inválido
6. combinación mínima funcional
7. lectura visual de pose clave

---

# Estado oficial del sistema

## Fase cerrada: biomecánica aislada confirmada

A la fecha, el sistema ya tiene calibrados y documentados:

- LowerTorso
- UpperTorso
- Head
- RightUpperLeg
- LeftUpperLeg
- RightLowerLeg
- LeftLowerLeg
- RightFoot
- LeftFoot
- RightUpperArm
- LeftUpperArm
- RightLowerArm
- LeftLowerArm
- RightHand
- LeftHand

Esto significa que ya está confirmada la base biomecánica del rig a nivel de joints, ejes, rangos naturales y restricciones principales.

---

# Principios biomecánicos universales confirmados

## Regla 1 — UpperLeg conduce la pierna

La dirección principal de la pierna nace en `UpperLeg`.

## Regla 2 — LowerLeg acompaña la pierna

`LowerLeg` sirve para:

- plegado
- chamber
- neutral funcional
- microajuste
- refinamiento de trayectoria

No debe liderar la pierna como driver principal.

## Regla 3 — Foot refina el contacto final

`Foot` no conduce la pierna. Refina:

- empeine
- punta
- planta
- orientación final del apoyo o impacto

## Regla 4 — UpperArm conduce el brazo

La dirección principal del brazo nace en `UpperArm`.

## Regla 5 — LowerArm acompaña el brazo

`LowerArm` sirve para:

- extensión
- recogida
- ajuste
- refinamiento de línea
- chamber secundario
- acompañamiento del gesto

## Regla 6 — Hand refina el contacto final

`Hand` no debe liderar el brazo. Refina:

- orientación del contacto
- lectura de muñeca
- limpieza de pose
- cierre visual del gesto

## Regla 7 — El espejo no se asume; se valida

La lógica funcional puede espejarse, pero los signos y topes deben respetar lo validado por cada lado.

## Regla 8 — Un eje puede verse mal aislado y ser útil en combinación

Un eje no se juzga solo por aislamiento absoluto. También debe evaluarse en contexto biomecánico compensado.

## Regla 9 — El rig puede permitir movimientos inválidos

Si un movimiento se ve biomecánicamente imposible, se clasifica como inválido aunque el rig técnicamente lo permita.

## Regla 10 — La validación visual manda

La lectura biomecánica final siempre debe confirmarse visualmente en pose real, no solo en teoría numérica.

---

# Nueva arquitectura oficial del sistema

A partir de este punto, el skill entra oficialmente en una arquitectura universal de animación compuesta por seis capas:

## 1. Biomecánica aislada

Qué hace cada joint, qué hace cada eje, qué rangos sirven, qué rangos deben evitarse.

## 2. Pose base neutra universal

Postura madre general del sistema, reutilizable como punto de inicio, equilibrio, transición y recuperación.

## 3. Biblioteca de primitivas universales

Bloques biomecánicos reutilizables que sirven como piezas base del movimiento.

## 4. Acciones completas

Construcción de movimientos funcionales a partir de primitivas.

## 5. Timing animatorio

Anticipación, impulso, impacto, follow-through, recuperación, spacing y ritmo.

## 6. JSON final robusto

Salida final compatible con Moon Animator, consistente entre frame inicial, intermedios y final.

La fórmula oficial del sistema queda así:

**biomecánica aislada -> pose base neutra -> primitivas universales -> acciones completas -> timing -> JSON final**

---

# Pose base neutra universal

## Definición

La **pose base neutra universal** será la postura madre general del sistema R15.

Debe servir como:

- punto de inicio
- punto de reposo
- punto de transición
- punto de recuperación
- punto de equilibrio corporal

## Características obligatorias

La pose base neutra universal debe sentirse:

- equilibrada
- viva
- natural
- funcional
- reutilizable
- estable
- preparada para movimiento

## Reglas de construcción

### 1. Peso estable

El cuerpo debe sentirse apoyado de forma limpia.

### 2. Rodillas funcionales

No deben quedar muertas ni bloqueadas.

### 3. Cadera estable

La pelvis debe sostener el cuerpo sin rigidez artificial.

### 4. Torso neutral funcional

Sin dramatización innecesaria, pero con vida corporal.

### 5. Brazos vivos

Los brazos no deben quedar ni rígidos ni colgados sin intención biomecánica.

### 6. Manos neutrales

Deben refinar la pose, no dominarla.

### 7. Pies limpios

Deben reforzar el apoyo y la lectura de equilibrio.

### 8. Cabeza centrada

Debe acompañar el eje general del cuerpo.

---

# Biblioteca oficial de primitivas universales

El skill debe pensar en **primitives biomecánicas reutilizables**, no en animaciones rígidas.

## A. Primitivas de soporte corporal

- pose base neutra
- apoyo estable
- apoyo cargado izquierda
- apoyo cargado derecha
- apertura leve
- cierre leve
- caída de peso
- recuperación a neutro

## B. Primitivas de torso

- inclinación adelante
- inclinación atrás
- inclinación lateral
- giro suave
- compensación de torso
- compresión
- extensión

## C. Primitivas de brazo

- elevación
- descenso
- extensión
- recogida
- apertura lateral
- cierre corporal
- chamber de brazo
- bloqueo alto
- bloqueo medio
- empuje de brazo
- martillazo

## D. Primitivas de pierna

- chamber de pierna
- proyección frontal
- proyección lateral
- elevación de rodilla
- extensión de pierna
- recogida
- apoyo unilateral
- contacto de pie
- aterrizaje

## E. Primitivas globales

- impulso vertical
- salto
- caída
- giro corporal
- follow-through
- recuperación
- transición

---

# Reglas oficiales de combinación

Toda acción completa debe construirse respetando una jerarquía clara de joints.

## Cadena de pierna

- `UpperLeg` conduce
- `LowerLeg` acompaña
- `Foot` refina

## Cadena de brazo

- `UpperArm` conduce
- `LowerArm` acompaña
- `Hand` refina

## Cadena axial

- `LowerTorso` estabiliza y desplaza masa
- `UpperTorso` compensa, dirige y amplifica
- `Head` acompaña la lectura final

## Regla de soporte

Todo movimiento dominante debe tener compensación corporal suficiente para no romper equilibrio visual.

## Regla de lectura limpia

Una pose no debe depender de demasiados microajustes contradictorios.
Debe existir un joint dominante legible por acción.

## Regla de compensación

Toda proyección importante de brazo o pierna puede exigir compensaciones de:

- torso
- pelvis
- apoyo
- pie contrario
- brazo opuesto
- cabeza

## Regla de exclusión

Se deben evitar combinaciones que:

- rompan anatomía visual
- anulen la intención principal
- mezclen drivers contradictorios
- usen articulaciones refinadoras como líderes absolutos

## Regla axial para rotación corporal completa

En acciones de rotación corporal completa sobre el eje sagital, como el **salto mortal hacia atrás**, `LowerTorso.rotation.x` actúa como **driver principal del giro global del cuerpo**.

En estas acciones:

- `LowerTorso.rotation.x` conduce la rotación completa
- `UpperTorso.rotation.x` acompaña, compensa y da forma al arco del tronco
- `Head.rotation.x` acompaña la lectura del giro
- brazos y piernas controlan la velocidad de rotación, el tuck, la apertura y el aterrizaje

## Regla contextual de altura en acciones invertidas

La lectura de `LowerTorso.position.y` no debe tratarse como una regla rígida e inmutable durante acciones con **inversión corporal completa**.

En poses erguidas o saltos normales:

- `LowerTorso.position.y` negativo suele elevar el cuerpo
- `LowerTorso.position.y` positivo suele bajarlo

Pero en acciones donde el cuerpo entra en fase invertida o casi invertida, como el salto mortal hacia atrás, la altura debe interpretarse **contextualmente según la orientación corporal real durante el giro**.

Por tanto:

- en fase erguida, el signo puede seguir la lógica normal ya validada
- en fase invertida, `position.y` puede necesitar cambiar de signo para seguir elevando visualmente el cuerpo y evitar que se entierre en el suelo
- la validación visual manda sobre una regla fija de signo cuando la acción entra en inversión completa

## Regla axial contextual de desplazamiento horizontal

La lectura de `LowerTorso.position.z` debe fijarse según la validación visual real del rig activo, no por suposición teórica.

En este rig R15 validado:

- `LowerTorso.position.z` negativo desplaza visualmente el cuerpo hacia atrás
- `LowerTorso.position.z` positivo desplaza visualmente el cuerpo hacia adelante

Por tanto:

- en acciones de retroceso, salto hacia atrás o desplazamiento hacia atrás, el skill debe usar `position.z` negativo
- en acciones de avance, salto hacia adelante o desplazamiento hacia adelante, el skill debe usar `position.z` positivo
- si otro rig leyera el eje de forma distinta, prevalece siempre la validación visual del rig real

## Regla práctica para mortales hacia atrás

En un mortal hacia atrás, la lógica oficial del sistema queda así:

- `LowerTorso.rotation.x` = driver principal del giro global
- `LowerTorso.position.y` = driver principal de la altura
- `UpperTorso.rotation.x` y `Head.rotation.x` = acompañamiento axial
- `UpperLeg` y `LowerLeg` = control de tuck, apertura y aterrizaje

Durante la fase invertida, la altura se debe resolver con **altura contextual**, no con una regla estática de signo.

---

# Reglas oficiales de timing

El skill no solo debe construir poses, sino movimiento.

Toda acción completa debe entender estas fases:

## 1. Anticipación

Preparación del cuerpo antes de la acción principal.

## 2. Impulso o proyección

Inicio energético del movimiento.

## 3. Punto clave

Momento de máxima lectura de la acción.

## 4. Impacto o máxima extensión

Momento principal del gesto.

## 5. Follow-through

Continuidad física posterior al punto clave.

## 6. Recuperación

Regreso controlado a una base funcional.

## 7. Spacing

Distribución coherente entre keyframes.

## 8. Ritmo

Duración interna del gesto según intención física y emocional.

---

# Reglas oficiales para generación JSON

El skill universal R15 para Moon Animator debe producir una salida JSON robusta, consistente y segura.

La salida oficial del skill representa una animación completa como un objeto con metadatos generales y una lista de keyframes por joint.

## Estructura raíz oficial

```json
{
  "animation_name": "nombre_de_la_animacion",
  "description": "descripcion_de_la_animacion",
  "total_frames": 40,
  "fps": 60,
  "intensity": 0.9,
  "keyframes": []
}
```

## Significado de cada campo

- `animation_name`: nombre técnico de la animación
- `description`: descripción breve del movimiento
- `total_frames`: frame final de la animación
- `fps`: fotogramas por segundo
- `intensity`: intensidad general del movimiento
- `keyframes`: lista completa de poses parciales o completas por joint y frame

## Estructura oficial de cada keyframe

Cada keyframe debe tener esta forma:

```json
{
  "joint": "LowerTorso",
  "frame": 0,
  "rotation": { "x": 0, "y": 0, "z": 0 },
  "position": { "x": 0, "y": 0, "z": 0 }
}
```

## Campos obligatorios por keyframe

- `joint`: nombre exacto del joint
- `frame`: número de frame
- `rotation.x`
- `rotation.y`
- `rotation.z`
- `position.x`
- `position.y`
- `position.z`

## Regla estructural obligatoria

Aunque un joint no use desplazamiento, el campo `position` debe existir igual con valores `0`.

## Joints oficiales admitidos

El skill solo debe emitir estos joints:

- `LowerTorso`
- `UpperTorso`
- `Head`
- `RightUpperArm`
- `RightLowerArm`
- `RightHand`
- `LeftUpperArm`
- `LeftLowerArm`
- `LeftHand`
- `RightUpperLeg`
- `RightLowerLeg`
- `RightFoot`
- `LeftUpperLeg`
- `LeftLowerLeg`
- `LeftFoot`

## Reglas oficiales de construcción del JSON

### Regla 1 — El frame 0 debe estar completo

El frame `0` debe incluir **todos los joints oficiales**, aunque estén en cero o en pose base neutra.

Esto define la pose inicial del sistema y evita ambigüedad en Moon Animator.

### Regla 2 — Los frames intermedios pueden ser parciales

En los frames intermedios, el skill puede incluir **solo los joints que cambian** en ese momento.

Esto reduce ruido y hace el JSON más limpio.

### Regla 3 — El frame final debe quedar explícito

El último frame debe quedar definido de forma clara.

Lo recomendable es que el frame final también incluya **todos los joints**, para cerrar correctamente la animación y evitar residuos de interpolación.

### Regla 4 — No duplicar el mismo joint en el mismo frame

No debe existir más de una entrada con el mismo `joint` y el mismo `frame`.

### Regla 5 — El orden debe ser estable

Las entradas deben ir ordenadas así:

1. por `frame` ascendente
2. dentro de cada frame, por orden fijo de joints

### Regla 6 — El nombre del joint debe ser exacto

No se permiten aliases ni variantes.

### Regla 7 — Toda rotación y posición debe ser numérica

No deben existir strings ni nulls.

## Convención oficial de total_frames

En este sistema, `total_frames` representa el **último índice de frame** de la animación.

Ejemplo:

```json
"total_frames": 40
```

significa que la animación va de:

- frame `0`
- hasta frame `40`

Por tanto, el skill debe entender `total_frames` como **frame final**, no como conteo bruto de entradas ni como cantidad matemática estricta de frames renderizados.

## Convención oficial de frames

### Frame 0

Pose inicial completa.

### Frames intermedios

Poses parciales o completas según necesidad biomecánica.

### Frame final

Pose final explícita, idealmente completa.

## Reglas de consistencia animatoria

El JSON no debe ser solo válido sintácticamente.
También debe ser coherente biomecánicamente.

### El skill debe garantizar

- estructura JSON exacta
- joints correctamente nombrados
- consistencia entre frame 0, intermedios y final
- detección de joints faltantes
- coherencia entre intención y keyframes
- compatibilidad limpia con Moon Animator
- estabilidad de interpolación
- continuidad entre poses
- progresión lógica entre frames
- compensación corporal suficiente
- retorno limpio cuando corresponda

### El skill debe evitar

- joints omitidos sin criterio
- cambios incoherentes entre frames
- poses rotas por falta de compensación
- usar refinadores como drivers absolutos
- contradicciones biomecánicas entre un keyframe y otro
- saltos bruscos sin intención
- frames incompletos en inicio o cierre
- duplicación conflictiva de joints

## Regla de consistencia

Toda animación debe mantener coherencia entre:

- pose inicial
- pose de desarrollo
- pose de impacto
- pose de recuperación
- pose final

## Política oficial de emisión

- **frame 0:** todos los joints obligatorios
- **frames intermedios:** solo joints que cambian
- **frame final:** todos los joints obligatorios

## Plantilla oficial de JSON universal

```json
{
  "animation_name": "nombre_de_la_animacion",
  "description": "descripcion_de_la_animacion",
  "total_frames": 40,
  "fps": 60,
  "intensity": 0.9,
  "keyframes": [
    {
      "joint": "LowerTorso",
      "frame": 0,
      "rotation": { "x": 0, "y": 0, "z": 0 },
      "position": { "x": 0, "y": 0, "z": 0 }
    }
  ]
}
```

## Ejemplo de lógica correcta

Una animación completa puede seguir esta estructura:

- frame 0: pose inicial completa
- frame 6: anticipación
- frame 12: impulso
- frame 20: pose clave principal
- frame 22: hold o impacto
- frame 32: recuperación
- frame 40: pose final completa

Ese patrón es válido para:

- salto
- golpe
- caída
- empuje
- baile
- locomoción
- interacción

## Ejemplo reducido de animación completa

```json
{
  "animation_name": "flying_kick_left",
  "description": "Patada voladora izquierda con salto real - estilo anime",
  "total_frames": 40,
  "fps": 60,
  "intensity": 0.9,
  "keyframes": [
    {
      "joint": "LowerTorso",
      "frame": 0,
      "rotation": { "x": 0, "y": 0, "z": 0 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },
    {
      "joint": "UpperTorso",
      "frame": 0,
      "rotation": { "x": 0, "y": 0, "z": 0 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },
    {
      "joint": "Head",
      "frame": 0,
      "rotation": { "x": 0, "y": 0, "z": 0 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },

    {
      "joint": "LowerTorso",
      "frame": 6,
      "rotation": { "x": -5, "y": 0, "z": 0 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },
    {
      "joint": "UpperTorso",
      "frame": 6,
      "rotation": { "x": -5, "y": 0, "z": 0 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },

    {
      "joint": "LowerTorso",
      "frame": 20,
      "rotation": { "x": -10, "y": 10, "z": 0 },
      "position": { "x": 0, "y": -1.2, "z": 0 }
    },
    {
      "joint": "UpperTorso",
      "frame": 20,
      "rotation": { "x": 13, "y": 15, "z": 0 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },
    {
      "joint": "RightUpperLeg",
      "frame": 20,
      "rotation": { "x": -79, "y": 65, "z": 30 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },
    {
      "joint": "LeftUpperLeg",
      "frame": 20,
      "rotation": { "x": -90, "y": -5, "z": -50 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },

    {
      "joint": "LowerTorso",
      "frame": 40,
      "rotation": { "x": 0, "y": 0, "z": 0 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },
    {
      "joint": "UpperTorso",
      "frame": 40,
      "rotation": { "x": 0, "y": 0, "z": 0 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },
    {
      "joint": "Head",
      "frame": 40,
      "rotation": { "x": 0, "y": 0, "z": 0 },
      "position": { "x": 0, "y": 0, "z": 0 }
    }
  ]
}
```

## Regla oficial del skill

El skill universal no entrega solamente poses sueltas.
Entrega una **animación completa en JSON**, con:

- metadatos
- estructura fija
- keyframes válidos
- continuidad corporal
- compatibilidad con Moon Animator

---

# Plantilla universal de construcción animatoria

Toda acción del sistema debe construirse con esta secuencia:

## Paso 1 — Intención

Qué quiere hacer el cuerpo.

## Paso 2 — Primitive base

Qué bloque biomecánico madre se usa.

## Paso 3 — Pose clave

Cuál es la lectura principal del movimiento.

## Paso 4 — Validación visual

Confirmar que la pose se ve humana o estilísticamente coherente.

## Paso 5 — Expansión

Añadir joints de soporte y refinamiento.

## Paso 6 — Timing

Definir anticipación, impacto, spacing y recuperación.

## Paso 7 — JSON final

Construir salida válida y consistente.

---

# Familias universales de animación del sistema

El motor universal debe poder organizar acciones en familias funcionales como:

## Locomoción

- idle
- caminar
- correr
- frenado
- giro

## Verticalidad

- salto
- caída
- aterrizaje
- rebote

## Interacción

- empujar
- jalar
- levantar
- agarrar
- soltar
- tocar

## Expresión corporal

- saludar
- apuntar
- sorpresa
- cansancio
- miedo
- celebración

## Ritmo

- baile
- groove
- sway
- bounce

## Acción física

- golpe recto
- bloqueo
- martillazo
- patada lateral
- esquiva

---

# Primitives oficiales cerradas hasta la fecha

Las siguientes primitives ya quedaron formalizadas como bloques técnicos reutilizables del sistema. Todas siguen la jerarquía biomecánica oficial del skill y respetan el contrato JSON definido en este README.

## 1. `POSE_BASE_NEUTRA_UNIVERSAL_V1`

### Definición funcional

Pose madre general del sistema. Debe servir como punto de inicio, reposo, transición, recuperación y equilibrio corporal.

### Lectura esperada

- equilibrada
- viva
- estable
- neutra
- lista para transicionar a cualquier acción

### Bloque técnico

```txt
POSE_BASE_NEUTRA_UNIVERSAL_V1

LowerTorso:
rotation {x: 0, y: 0, z: 0}
position {x: 0, y: 0, z: 0}

UpperTorso:
rotation {x: -6.205, y: 0, z: 0}
position {x: 0, y: 0, z: 0}

Head:
rotation {x: 0, y: 0, z: 0}
position {x: 0, y: 0, z: 0}

RightUpperArm:
rotation {x: -12.001, y: 5, z: -10.001}
position {x: 0, y: 0, z: 0}

RightLowerArm:
rotation {x: 0, y: 0, z: 0}
position {x: 0, y: 0, z: 0}

RightHand:
rotation {x: 0, y: 0, z: 0}
position {x: 0, y: 0, z: 0}

LeftUpperArm:
rotation {x: -12.001, y: 5, z: 10}
position {x: 0, y: 0, z: 0}

LeftLowerArm:
rotation {x: 0, y: 0, z: 0}
position {x: 0, y: 0, z: 0}

LeftHand:
rotation {x: 0, y: 0, z: 0}
position {x: 0, y: 0, z: 0}

RightUpperLeg:
rotation {x: -3.242, y: 3, z: -8.001}
position {x: 0, y: 0, z: -0.001}

RightLowerLeg:
rotation {x: 0, y: 0, z: 0}
position {x: 0, y: 0, z: 0}

RightFoot:
rotation {x: 0, y: 0, z: 0}
position {x: 0, y: 0, z: 0}

LeftUpperLeg:
rotation {x: -3.073, y: -3.001, z: 8}
position {x: 0, y: 0, z: -0.001}

LeftLowerLeg:
rotation {x: 0, y: 0, z: 0}
position {x: 0, y: 0, z: 0}

LeftFoot:
rotation {x: 0, y: 0, z: 0}
position {x: 0, y: 0, z: 0}
```

### JSON oficial

```json
{
  "animation_name": "pose_base_neutra_universal_v1",
  "description": "Pose base neutra universal del sistema R15, equilibrada, viva, estable y reutilizable como punto de inicio, transicion y recuperacion",
  "total_frames": 60,
  "fps": 60,
  "intensity": 1,
  "keyframes": [
    {
      "joint": "Head",
      "frame": 0,
      "rotation": { "y": 0, "x": 0, "z": 0 },
      "position": { "y": 0, "x": 0, "z": 0 }
    },
    {
      "joint": "LeftFoot",
      "frame": 0,
      "rotation": { "y": 0, "x": 0, "z": 0 },
      "position": { "y": 0, "x": 0, "z": 0 }
    },
    {
      "joint": "LeftHand",
      "frame": 0,
      "rotation": { "y": 0, "x": 0, "z": 0 },
      "position": { "y": 0, "x": 0, "z": 0 }
    },
    {
      "joint": "LeftLowerArm",
      "frame": 0,
      "rotation": { "y": 0, "x": 0, "z": 0 },
      "position": { "y": 0, "x": 0, "z": 0 }
    },
    {
      "joint": "LeftLowerLeg",
      "frame": 0,
      "rotation": { "y": 0, "x": 0, "z": 0 },
      "position": { "y": 0, "x": 0, "z": 0 }
    },
    {
      "joint": "LeftUpperArm",
      "frame": 0,
      "rotation": { "y": 5, "x": -12.001, "z": 10 },
      "position": { "y": 0, "x": 0, "z": 0 }
    },
    {
      "joint": "LeftUpperLeg",
      "frame": 0,
      "rotation": { "y": -3.001, "x": -3.073, "z": 8 },
      "position": { "y": 0, "x": 0, "z": -0.001 }
    },
    {
      "joint": "LowerTorso",
      "frame": 0,
      "rotation": { "y": 0, "x": 0, "z": 0 },
      "position": { "y": 0, "x": 0, "z": 0 }
    },
    {
      "joint": "RightFoot",
      "frame": 0,
      "rotation": { "y": 0, "x": 0, "z": 0 },
      "position": { "y": 0, "x": 0, "z": 0 }
    },
    {
      "joint": "RightHand",
      "frame": 0,
      "rotation": { "y": 0, "x": 0, "z": 0 },
      "position": { "y": 0, "x": 0, "z": 0 }
    },
    {
      "joint": "RightLowerArm",
      "frame": 0,
      "rotation": { "y": 0, "x": 0, "z": 0 },
      "position": { "y": 0, "x": 0, "z": 0 }
    },
    {
      "joint": "RightLowerLeg",
      "frame": 0,
      "rotation": { "y": 0, "x": 0, "z": 0 },
      "position": { "y": 0, "x": 0, "z": 0 }
    },
    {
      "joint": "RightUpperArm",
      "frame": 0,
      "rotation": { "y": 5, "x": -12.001, "z": -10.001 },
      "position": { "y": 0, "x": 0, "z": 0 }
    },
    {
      "joint": "RightUpperLeg",
      "frame": 0,
      "rotation": { "y": 3, "x": -3.242, "z": -8.001 },
      "position": { "y": 0, "x": 0, "z": -0.001 }
    },
    {
      "joint": "UpperTorso",
      "frame": 0,
      "rotation": { "y": 0, "x": -6.205, "z": 0 },
      "position": { "y": 0, "x": 0, "z": 0 }
    }
  ]
}
```

---

## 2. `APOYO_ESTABLE_V1.1`

### Definición funcional

Primitive universal de apoyo bilateral estable, más natural y relajada que la V1. Sirve como base para idle, recuperación, aterrizaje suave y transiciones.

### Estado

**Validado visualmente** como versión más orgánica que la V1 original.

### Bloque técnico

```txt
APOYO_ESTABLE_V1_1

LowerTorso:
rotation {x: 1, y: 0, z: 0}
position {x: 0, y: 0, z: 0}

UpperTorso:
rotation {x: -1, y: 0, z: 0}

Head:
rotation {x: 0, y: 0, z: 0}

RightUpperArm:
rotation {x: -6, y: 2, z: -7}

RightLowerArm:
rotation {x: 6, y: 0, z: 0}

RightHand:
rotation {x: 8, y: 0, z: 0}

LeftUpperArm:
rotation {x: -6, y: 2, z: 7}

LeftLowerArm:
rotation {x: 6, y: 0, z: 0}

LeftHand:
rotation {x: 8, y: 0, z: 0}

RightUpperLeg:
rotation {x: 3, y: 2, z: -9}

RightLowerLeg:
rotation {x: 10, y: 0, z: 0}

RightFoot:
rotation {x: -5, y: 3, z: 0}

LeftUpperLeg:
rotation {x: 3, y: -2, z: 9}

LeftLowerLeg:
rotation {x: 10, y: 0, z: 0}

LeftFoot:
rotation {x: -5, y: -3, z: 0}
```

### JSON oficial

```json
{
  "animation_name": "apoyo_estable_v1_1",
  "description": "Primitive universal de apoyo bilateral estable, mas natural y relajada que la V1, util como base para idle, recuperacion, aterrizaje suave y transiciones",
  "total_frames": 0,
  "fps": 60,
  "intensity": 0.22,
  "keyframes": [
    {
      "joint": "LowerTorso",
      "frame": 0,
      "rotation": { "x": 1, "y": 0, "z": 0 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },
    {
      "joint": "UpperTorso",
      "frame": 0,
      "rotation": { "x": -1, "y": 0, "z": 0 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },
    {
      "joint": "Head",
      "frame": 0,
      "rotation": { "x": 0, "y": 0, "z": 0 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },

    {
      "joint": "RightUpperArm",
      "frame": 0,
      "rotation": { "x": -6, "y": 2, "z": -7 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },
    {
      "joint": "RightLowerArm",
      "frame": 0,
      "rotation": { "x": 6, "y": 0, "z": 0 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },
    {
      "joint": "RightHand",
      "frame": 0,
      "rotation": { "x": 8, "y": 0, "z": 0 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },

    {
      "joint": "LeftUpperArm",
      "frame": 0,
      "rotation": { "x": -6, "y": 2, "z": 7 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },
    {
      "joint": "LeftLowerArm",
      "frame": 0,
      "rotation": { "x": 6, "y": 0, "z": 0 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },
    {
      "joint": "LeftHand",
      "frame": 0,
      "rotation": { "x": 8, "y": 0, "z": 0 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },

    {
      "joint": "RightUpperLeg",
      "frame": 0,
      "rotation": { "x": 3, "y": 2, "z": -9 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },
    {
      "joint": "RightLowerLeg",
      "frame": 0,
      "rotation": { "x": 10, "y": 0, "z": 0 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },
    {
      "joint": "RightFoot",
      "frame": 0,
      "rotation": { "x": -5, "y": 3, "z": 0 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },

    {
      "joint": "LeftUpperLeg",
      "frame": 0,
      "rotation": { "x": 3, "y": -2, "z": 9 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },
    {
      "joint": "LeftLowerLeg",
      "frame": 0,
      "rotation": { "x": 10, "y": 0, "z": 0 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },
    {
      "joint": "LeftFoot",
      "frame": 0,
      "rotation": { "x": -5, "y": -3, "z": 0 },
      "position": { "x": 0, "y": 0, "z": 0 }
    }
  ]
}
```

---

## 3. `APOYO_CARGADO_IZQUIERDA_V1`

### Definición funcional

Primitive universal de transferencia de peso hacia la pierna izquierda. Útil para preparar pasos, giros, impulsos y transiciones laterales.

### Bloque técnico

```txt
APOYO_CARGADO_IZQUIERDA_V1

LowerTorso:
rotation {x: 1, y: 0, z: -4}
position {x: 0, y: 0, z: 0}

UpperTorso:
rotation {x: -1, y: 0, z: 2}

Head:
rotation {x: 0, y: 0, z: 1}

RightUpperArm:
rotation {x: -5, y: 2, z: -8}

RightLowerArm:
rotation {x: 7, y: 0, z: 0}

RightHand:
rotation {x: 8, y: 0, z: 0}

LeftUpperArm:
rotation {x: -7, y: 2, z: 6}

LeftLowerArm:
rotation {x: 5, y: 0, z: 0}

LeftHand:
rotation {x: 7, y: 0, z: 0}

RightUpperLeg:
rotation {x: 5, y: 3, z: -12}

RightLowerLeg:
rotation {x: 14, y: 0, z: 0}

RightFoot:
rotation {x: -7, y: 4, z: 0}

LeftUpperLeg:
rotation {x: 2, y: -1, z: 7}

LeftLowerLeg:
rotation {x: 8, y: 0, z: 0}

LeftFoot:
rotation {x: -3, y: -2, z: 0}
```

### JSON oficial

```json
{
  "animation_name": "apoyo_cargado_izquierda_v1",
  "description": "Primitive universal de transferencia de peso hacia la pierna izquierda, util para preparar pasos, giros, impulsos y transiciones laterales",
  "total_frames": 0,
  "fps": 60,
  "intensity": 0.28,
  "keyframes": [
    {
      "joint": "LowerTorso",
      "frame": 0,
      "rotation": { "x": 1, "y": 0, "z": -4 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },
    {
      "joint": "UpperTorso",
      "frame": 0,
      "rotation": { "x": -1, "y": 0, "z": 2 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },
    {
      "joint": "Head",
      "frame": 0,
      "rotation": { "x": 0, "y": 0, "z": 1 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },

    {
      "joint": "RightUpperArm",
      "frame": 0,
      "rotation": { "x": -5, "y": 2, "z": -8 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },
    {
      "joint": "RightLowerArm",
      "frame": 0,
      "rotation": { "x": 7, "y": 0, "z": 0 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },
    {
      "joint": "RightHand",
      "frame": 0,
      "rotation": { "x": 8, "y": 0, "z": 0 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },

    {
      "joint": "LeftUpperArm",
      "frame": 0,
      "rotation": { "x": -7, "y": 2, "z": 6 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },
    {
      "joint": "LeftLowerArm",
      "frame": 0,
      "rotation": { "x": 5, "y": 0, "z": 0 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },
    {
      "joint": "LeftHand",
      "frame": 0,
      "rotation": { "x": 7, "y": 0, "z": 0 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },

    {
      "joint": "RightUpperLeg",
      "frame": 0,
      "rotation": { "x": 5, "y": 3, "z": -12 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },
    {
      "joint": "RightLowerLeg",
      "frame": 0,
      "rotation": { "x": 14, "y": 0, "z": 0 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },
    {
      "joint": "RightFoot",
      "frame": 0,
      "rotation": { "x": -7, "y": 4, "z": 0 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },

    {
      "joint": "LeftUpperLeg",
      "frame": 0,
      "rotation": { "x": 2, "y": -1, "z": 7 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },
    {
      "joint": "LeftLowerLeg",
      "frame": 0,
      "rotation": { "x": 8, "y": 0, "z": 0 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },
    {
      "joint": "LeftFoot",
      "frame": 0,
      "rotation": { "x": -3, "y": -2, "z": 0 },
      "position": { "x": 0, "y": 0, "z": 0 }
    }
  ]
}
```

---

## 4. `APOYO_CARGADO_DERECHA_V1`

### Definición funcional

Primitive universal de transferencia de peso hacia la pierna derecha. Útil para preparar pasos, giros, impulsos y transiciones laterales.

### Bloque técnico

```txt
APOYO_CARGADO_DERECHA_V1

LowerTorso:
rotation {x: 1, y: 0, z: 4}
position {x: 0, y: 0, z: 0}

UpperTorso:
rotation {x: -1, y: 0, z: -2}

Head:
rotation {x: 0, y: 0, z: -1}

RightUpperArm:
rotation {x: -7, y: 2, z: -6}

RightLowerArm:
rotation {x: 5, y: 0, z: 0}

RightHand:
rotation {x: 7, y: 0, z: 0}

LeftUpperArm:
rotation {x: -5, y: 2, z: 8}

LeftLowerArm:
rotation {x: 7, y: 0, z: 0}

LeftHand:
rotation {x: 8, y: 0, z: 0}

RightUpperLeg:
rotation {x: 2, y: 1, z: -7}

RightLowerLeg:
rotation {x: 8, y: 0, z: 0}

RightFoot:
rotation {x: -3, y: 2, z: 0}

LeftUpperLeg:
rotation {x: 5, y: -3, z: 12}

LeftLowerLeg:
rotation {x: 14, y: 0, z: 0}

LeftFoot:
rotation {x: -7, y: -4, z: 0}
```

### JSON oficial

```json
{
  "animation_name": "apoyo_cargado_derecha_v1",
  "description": "Primitive universal de transferencia de peso hacia la pierna derecha, util para preparar pasos, giros, impulsos y transiciones laterales",
  "total_frames": 0,
  "fps": 60,
  "intensity": 0.28,
  "keyframes": [
    {
      "joint": "LowerTorso",
      "frame": 0,
      "rotation": { "x": 1, "y": 0, "z": 4 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },
    {
      "joint": "UpperTorso",
      "frame": 0,
      "rotation": { "x": -1, "y": 0, "z": -2 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },
    {
      "joint": "Head",
      "frame": 0,
      "rotation": { "x": 0, "y": 0, "z": -1 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },

    {
      "joint": "RightUpperArm",
      "frame": 0,
      "rotation": { "x": -7, "y": 2, "z": -6 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },
    {
      "joint": "RightLowerArm",
      "frame": 0,
      "rotation": { "x": 5, "y": 0, "z": 0 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },
    {
      "joint": "RightHand",
      "frame": 0,
      "rotation": { "x": 7, "y": 0, "z": 0 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },

    {
      "joint": "LeftUpperArm",
      "frame": 0,
      "rotation": { "x": -5, "y": 2, "z": 8 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },
    {
      "joint": "LeftLowerArm",
      "frame": 0,
      "rotation": { "x": 7, "y": 0, "z": 0 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },
    {
      "joint": "LeftHand",
      "frame": 0,
      "rotation": { "x": 8, "y": 0, "z": 0 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },

    {
      "joint": "RightUpperLeg",
      "frame": 0,
      "rotation": { "x": 2, "y": 1, "z": -7 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },
    {
      "joint": "RightLowerLeg",
      "frame": 0,
      "rotation": { "x": 8, "y": 0, "z": 0 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },
    {
      "joint": "RightFoot",
      "frame": 0,
      "rotation": { "x": -3, "y": 2, "z": 0 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },

    {
      "joint": "LeftUpperLeg",
      "frame": 0,
      "rotation": { "x": 5, "y": -3, "z": 12 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },
    {
      "joint": "LeftLowerLeg",
      "frame": 0,
      "rotation": { "x": 14, "y": 0, "z": 0 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },
    {
      "joint": "LeftFoot",
      "frame": 0,
      "rotation": { "x": -7, "y": -4, "z": 0 },
      "position": { "x": 0, "y": 0, "z": 0 }
    }
  ]
}
```

---

## 5. `APERTURA_LEVE_V1`

### Definición funcional

Primitive universal de separación corporal suave. Útil para idle vivo, preparación de paso, salto, giro y transiciones expresivas.

### Bloque técnico

```txt
APERTURA_LEVE_V1

LowerTorso:
rotation {x: 1, y: 0, z: 0}
position {x: 0, y: 0, z: 0}

UpperTorso:
rotation {x: -1, y: 0, z: 0}

Head:
rotation {x: 0, y: 0, z: 0}

RightUpperArm:
rotation {x: -8, y: 3, z: -12}

RightLowerArm:
rotation {x: 5, y: 0, z: 0}

RightHand:
rotation {x: 8, y: 0, z: 0}

LeftUpperArm:
rotation {x: -8, y: 3, z: 12}

LeftLowerArm:
rotation {x: 5, y: 0, z: 0}

LeftHand:
rotation {x: 8, y: 0, z: 0}

RightUpperLeg:
rotation {x: 4, y: 2, z: -14}

RightLowerLeg:
rotation {x: 10, y: 0, z: 0}

RightFoot:
rotation {x: -5, y: 4, z: 0}

LeftUpperLeg:
rotation {x: 4, y: -2, z: 14}

LeftLowerLeg:
rotation {x: 10, y: 0, z: 0}

LeftFoot:
rotation {x: -5, y: -4, z: 0}
```

### JSON oficial

```json
{
  "animation_name": "apertura_leve_v1",
  "description": "Primitive universal de separacion corporal suave, util para idle vivo, preparacion de paso, salto, giro y transiciones expresivas",
  "total_frames": 0,
  "fps": 60,
  "intensity": 0.24,
  "keyframes": [
    {
      "joint": "LowerTorso",
      "frame": 0,
      "rotation": { "x": 1, "y": 0, "z": 0 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },
    {
      "joint": "UpperTorso",
      "frame": 0,
      "rotation": { "x": -1, "y": 0, "z": 0 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },
    {
      "joint": "Head",
      "frame": 0,
      "rotation": { "x": 0, "y": 0, "z": 0 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },

    {
      "joint": "RightUpperArm",
      "frame": 0,
      "rotation": { "x": -8, "y": 3, "z": -12 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },
    {
      "joint": "RightLowerArm",
      "frame": 0,
      "rotation": { "x": 5, "y": 0, "z": 0 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },
    {
      "joint": "RightHand",
      "frame": 0,
      "rotation": { "x": 8, "y": 0, "z": 0 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },

    {
      "joint": "LeftUpperArm",
      "frame": 0,
      "rotation": { "x": -8, "y": 3, "z": 12 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },
    {
      "joint": "LeftLowerArm",
      "frame": 0,
      "rotation": { "x": 5, "y": 0, "z": 0 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },
    {
      "joint": "LeftHand",
      "frame": 0,
      "rotation": { "x": 8, "y": 0, "z": 0 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },

    {
      "joint": "RightUpperLeg",
      "frame": 0,
      "rotation": { "x": 4, "y": 2, "z": -14 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },
    {
      "joint": "RightLowerLeg",
      "frame": 0,
      "rotation": { "x": 10, "y": 0, "z": 0 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },
    {
      "joint": "RightFoot",
      "frame": 0,
      "rotation": { "x": -5, "y": 4, "z": 0 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },

    {
      "joint": "LeftUpperLeg",
      "frame": 0,
      "rotation": { "x": 4, "y": -2, "z": 14 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },
    {
      "joint": "LeftLowerLeg",
      "frame": 0,
      "rotation": { "x": 10, "y": 0, "z": 0 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },
    {
      "joint": "LeftFoot",
      "frame": 0,
      "rotation": { "x": -5, "y": -4, "z": 0 },
      "position": { "x": 0, "y": 0, "z": 0 }
    }
  ]
}
```

---

## 6. `CIERRE_LEVE_V1`

### Definición funcional

Primitive universal de compactación corporal suave. Útil para reposo contenido, pausa corporal, recuperación y transiciones internas del sistema.

### Bloque técnico

```txt
CIERRE_LEVE_V1

LowerTorso:
rotation {x: 1, y: 0, z: 0}
position {x: 0, y: 0, z: 0}

UpperTorso:
rotation {x: -1, y: 0, z: 0}

Head:
rotation {x: 0, y: 0, z: 0}

RightUpperArm:
rotation {x: -5, y: 2, z: -4}

RightLowerArm:
rotation {x: 7, y: 0, z: 0}

RightHand:
rotation {x: 8, y: 0, z: 0}

LeftUpperArm:
rotation {x: -5, y: 2, z: 4}

LeftLowerArm:
rotation {x: 7, y: 0, z: 0}

LeftHand:
rotation {x: 8, y: 0, z: 0}

RightUpperLeg:
rotation {x: 3, y: 1, z: -5}

RightLowerLeg:
rotation {x: 10, y: 0, z: 0}

RightFoot:
rotation {x: -4, y: 2, z: 0}

LeftUpperLeg:
rotation {x: 3, y: -1, z: 5}

LeftLowerLeg:
rotation {x: 10, y: 0, z: 0}

LeftFoot:
rotation {x: -4, y: -2, z: 0}
```

### JSON oficial

```json
{
  "animation_name": "cierre_leve_v1",
  "description": "Primitive universal de compactacion corporal suave, util para reposo contenido, pausa corporal, recuperacion y transiciones internas del sistema R15",
  "total_frames": 0,
  "fps": 60,
  "intensity": 0.22,
  "keyframes": [
    {
      "joint": "LowerTorso",
      "frame": 0,
      "rotation": { "x": 1, "y": 0, "z": 0 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },
    {
      "joint": "UpperTorso",
      "frame": 0,
      "rotation": { "x": -1, "y": 0, "z": 0 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },
    {
      "joint": "Head",
      "frame": 0,
      "rotation": { "x": 0, "y": 0, "z": 0 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },

    {
      "joint": "RightUpperArm",
      "frame": 0,
      "rotation": { "x": -5, "y": 2, "z": -4 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },
    {
      "joint": "RightLowerArm",
      "frame": 0,
      "rotation": { "x": 7, "y": 0, "z": 0 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },
    {
      "joint": "RightHand",
      "frame": 0,
      "rotation": { "x": 8, "y": 0, "z": 0 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },

    {
      "joint": "LeftUpperArm",
      "frame": 0,
      "rotation": { "x": -5, "y": 2, "z": 4 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },
    {
      "joint": "LeftLowerArm",
      "frame": 0,
      "rotation": { "x": 7, "y": 0, "z": 0 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },
    {
      "joint": "LeftHand",
      "frame": 0,
      "rotation": { "x": 8, "y": 0, "z": 0 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },

    {
      "joint": "RightUpperLeg",
      "frame": 0,
      "rotation": { "x": 3, "y": 1, "z": -5 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },
    {
      "joint": "RightLowerLeg",
      "frame": 0,
      "rotation": { "x": 10, "y": 0, "z": 0 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },
    {
      "joint": "RightFoot",
      "frame": 0,
      "rotation": { "x": -4, "y": 2, "z": 0 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },

    {
      "joint": "LeftUpperLeg",
      "frame": 0,
      "rotation": { "x": 3, "y": -1, "z": 5 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },
    {
      "joint": "LeftLowerLeg",
      "frame": 0,
      "rotation": { "x": 10, "y": 0, "z": 0 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },
    {
      "joint": "LeftFoot",
      "frame": 0,
      "rotation": { "x": -4, "y": -2, "z": 0 },
      "position": { "x": 0, "y": 0, "z": 0 }
    }
  ]
}
```

---

## 7. `RECUPERACION_A_NEUTRO_V1`

### Definición funcional

Primitive universal de retorno limpio hacia la pose base neutra del sistema. Útil para cerrar aperturas, cierres, cargas y pequeñas acciones con equilibrio corporal.

### Bloque técnico

```txt
RECUPERACION_A_NEUTRO_V1

LowerTorso:
rotation {x: 0, y: 0, z: 0}
position {x: 0, y: 0, z: 0}

UpperTorso:
rotation {x: 0, y: 0, z: 0}

Head:
rotation {x: 0, y: 0, z: 0}

RightUpperArm:
rotation {x: -10, y: 4, z: -9}

RightLowerArm:
rotation {x: 2, y: 0, z: 0}

RightHand:
rotation {x: 6, y: 0, z: 0}

LeftUpperArm:
rotation {x: -10, y: 4, z: 9}

LeftLowerArm:
rotation {x: 2, y: 0, z: 0}

LeftHand:
rotation {x: 6, y: 0, z: 0}

RightUpperLeg:
rotation {x: 5, y: 2, z: -7}

RightLowerLeg:
rotation {x: 9, y: 0, z: 0}

RightFoot:
rotation {x: -4, y: 3, z: 0}

LeftUpperLeg:
rotation {x: 5, y: -2, z: 7}

LeftLowerLeg:
rotation {x: 9, y: 0, z: 0}

LeftFoot:
rotation {x: -4, y: -3, z: 0}
```

### JSON oficial

```json
{
  "animation_name": "recuperacion_a_neutro_v1",
  "description": "Primitive universal de retorno limpio hacia la pose base neutra del sistema R15, util para cerrar aperturas, cierres, cargas y pequenas acciones con equilibrio corporal",
  "total_frames": 0,
  "fps": 60,
  "intensity": 0.2,
  "keyframes": [
    {
      "joint": "LowerTorso",
      "frame": 0,
      "rotation": { "x": 0, "y": 0, "z": 0 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },
    {
      "joint": "UpperTorso",
      "frame": 0,
      "rotation": { "x": 0, "y": 0, "z": 0 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },
    {
      "joint": "Head",
      "frame": 0,
      "rotation": { "x": 0, "y": 0, "z": 0 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },

    {
      "joint": "RightUpperArm",
      "frame": 0,
      "rotation": { "x": -10, "y": 4, "z": -9 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },
    {
      "joint": "RightLowerArm",
      "frame": 0,
      "rotation": { "x": 2, "y": 0, "z": 0 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },
    {
      "joint": "RightHand",
      "frame": 0,
      "rotation": { "x": 6, "y": 0, "z": 0 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },

    {
      "joint": "LeftUpperArm",
      "frame": 0,
      "rotation": { "x": -10, "y": 4, "z": 9 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },
    {
      "joint": "LeftLowerArm",
      "frame": 0,
      "rotation": { "x": 2, "y": 0, "z": 0 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },
    {
      "joint": "LeftHand",
      "frame": 0,
      "rotation": { "x": 6, "y": 0, "z": 0 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },

    {
      "joint": "RightUpperLeg",
      "frame": 0,
      "rotation": { "x": 5, "y": 2, "z": -7 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },
    {
      "joint": "RightLowerLeg",
      "frame": 0,
      "rotation": { "x": 9, "y": 0, "z": 0 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },
    {
      "joint": "RightFoot",
      "frame": 0,
      "rotation": { "x": -4, "y": 3, "z": 0 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },

    {
      "joint": "LeftUpperLeg",
      "frame": 0,
      "rotation": { "x": 5, "y": -2, "z": 7 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },
    {
      "joint": "LeftLowerLeg",
      "frame": 0,
      "rotation": { "x": 9, "y": 0, "z": 0 },
      "position": { "x": 0, "y": 0, "z": 0 }
    },
    {
      "joint": "LeftFoot",
      "frame": 0,
      "rotation": { "x": -4, "y": -3, "z": 0 },
      "position": { "x": 0, "y": 0, "z": 0 }
    }
  ]
}
```

---

# Estado de madurez del sistema

## Cerrado

- biomecánica aislada principal del rig
- jerarquía funcional de joints
- principios biomecánicos universales
- arquitectura general del sistema
- `POSE_BASE_NEUTRA_UNIVERSAL_V1`
- `APOYO_ESTABLE_V1.1`
- `APOYO_CARGADO_IZQUIERDA_V1`
- `APOYO_CARGADO_DERECHA_V1`
- `APERTURA_LEVE_V1`
- `CIERRE_LEVE_V1`
- `RECUPERACION_A_NEUTRO_V1`
- `GOLPE_RECTO_DERECHO_ROBLOX_V1`

## En construcción

- caída de peso
- impulso vertical
- biblioteca formal restante de primitivas
- reglas explícitas de combinación por familia
- timing universal por tipo de acción
- validador JSON final
- pruebas combinadas oficiales

---

# Siguiente fase oficial

El siguiente bloque de trabajo del sistema es:

## Fase 1

Consolidar las primitives base ya cerradas dentro del README maestro y mantenerlas como canon oficial.

## Fase 2

Formalizar la siguiente capa inmediata de primitivas universales:

- chamber de brazo
- extensión de brazo
- chamber de pierna
- extensión de pierna
- impulso vertical
- caída de peso

## Fase 3

Pasar a pruebas combinadas universales con poses reales:

- idle
- caminata base
- salto base
- caída base
- empuje
- martillazo
- patada lateral
- baile

## Fase 4

Formalizar timing universal y salida JSON confiable

---

# Meta final del sistema

Construir un skill universal capaz de animar correctamente cualquier acción del rig R15 entendiendo:

- qué hace cada joint
- qué hace cada eje
- qué rangos son naturales
- cuáles son forzados
- cuáles son inválidos
- cómo combinar joints de forma biomecánicamente coherente
- cómo validar poses antes de animar
- cómo expandir poses a secuencias reales
- cómo generar JSON final limpio para Moon Animator

---

# Cierre oficial

Este README ya no es solo una guía de pruebas.
Es la base estructural del **motor biomecánico universal R15 para Moon Animator**.

Su propósito no es describir animaciones sueltas, sino construir una inteligencia corporal reutilizable, coherente y escalable para cualquier movimiento del rig.

---

---

## CONTACTO_DOS_MANOS_CENTRO_V1

### Definición funcional

Primitive universal para **cerrar ambas manos sobre un mismo eje central visual** delante del torso.
Sirve como base para:

- sostener espada vertical
- sostener bastón
- guardia cerrada
- agarre compacto de arma larga
- bloqueo central a dos manos

Esta primitive extiende la lógica biomecánica actual del skill, manteniendo:
- `UpperArm` conduce
- `LowerArm` acompaña
- `Hand` refina

y añade una regla nueva de **convergencia visual real**.

### Lectura esperada

La pose debe sentirse:

- compacta
- centrada
- funcional
- estable
- con ambas manos convergiendo al mismo punto visual
- útil para sostener un objeto vertical imaginario al centro del torso

No debe leerse como:

- aplauso
- abrazo
- brazos abiertos
- guardia rota
- manos cerca pero sin contacto visual común

### Regla oficial nueva — convergencia a dos manos

Cuando dos manos deban sostener un mismo objeto o cerrar sobre un mismo eje central:

- no basta con simetría biomecánica
- debe existir **convergencia visual explícita**
- `UpperArm` conduce el acercamiento general
- `LowerArm` cierra el contacto
- `Hand` refina el agarre final
- si la rotación no basta, se permite **microajuste de `UpperArm.position`**
- la validación final depende del **cierre visual real**, no de la simetría numérica pura

### Regla de mano líder y mano secundaria

Para evitar ambigüedad, esta primitive trabaja así:

- una mano actúa como **líder**
- la otra actúa como **secundaria**
- la mano líder define primero el eje principal del agarre
- la mano secundaria se corrige para cerrar sobre ese mismo eje

En la versión base V1:

- **RightHand / RightArm = líder**
- **LeftHand / LeftArm = secundaria**

Luego se podrá hacer versión espejada.

### Regla de construcción

Orden obligatorio:

1. definir eje central del objeto imaginario
2. acomodar `RightUpperArm`
3. corregir `RightUpperArm.position` si hace falta
4. cerrar `RightLowerArm`
5. refinar `RightHand`
6. acomodar `LeftUpperArm`
7. corregir `LeftUpperArm.position` si hace falta
8. cerrar `LeftLowerArm`
9. refinar `LeftHand`
10. validar convergencia visual de ambas manos
11. añadir torso mínimo de soporte

### Reglas de validación

La primitive se considera válida si:

- ambas manos leen un mismo centro visual
- los brazos no quedan excesivamente abiertos
- los codos no se rompen
- el torso sigue limpio
- la pose se siente como agarre y no como cruce arbitrario de brazos

La primitive se considera inválida si:

- las manos no cierran visualmente
- cada brazo parece apuntar a un centro distinto
- el contacto depende de un forzado anatómico evidente
- la pose se lee como abrazo o bloqueo roto
- el cierre solo existe numéricamente pero no visualmente

### Hallazgo oficial incorporado

Para contacto central a dos manos en R15:

- `UpperArm` puede requerir **microajustes de `position.y` y `position.z`**
- `LowerArm` puede quedar inicialmente neutro en una fase exploratoria
- `Hand` puede refinar después
- la validación visual manda

### Bloque técnico

```txt
CONTACTO_DOS_MANOS_CENTRO_V1

Head:
rotation {x: 0, y: 0, z: 0}
position {x: 0, y: 0, z: 0}

LowerTorso:
rotation {x: 4.61, y: 0, z: 0}
position {x: 0, y: 0, z: 0}

UpperTorso:
rotation {x: 0, y: 0, z: 0}
position {x: 0, y: 0, z: 0}

RightUpperArm:
rotation {x: -66.465, y: -38.242, z: -1.998}
position {x: -0.006, y: 0.469, z: -0.208}

RightLowerArm:
rotation {x: 0, y: 0, z: 0}
position {x: 0, y: 0, z: 0}

RightHand:
rotation {x: 0, y: 0, z: 0}
position {x: 0, y: 0, z: 0}

LeftUpperArm:
rotation {x: -55.001, y: 42, z: -1.901}
position {x: -0.001, y: 0.406, z: -0.114}

LeftLowerArm:
rotation {x: 0, y: 0, z: 0}
position {x: 0, y: 0, z: 0}

LeftHand:
rotation {x: 0, y: 0, z: 0}
position {x: 0, y: 0, z: 0}

RightUpperLeg:
rotation {x: 0, y: 0, z: -12.656}
position {x: 0, y: 0, z: -0.031}

RightLowerLeg:
rotation {x: 0, y: 0, z: 0}
position {x: 0, y: 0, z: 0}

RightFoot:
rotation {x: 0, y: 0, z: 0}
position {x: 0, y: 0, z: 0}

LeftUpperLeg:
rotation {x: -2.094, y: 0.512, z: 8.829}
position {x: 0.002, y: -0.001, z: 0.028}

LeftLowerLeg:
rotation {x: 0, y: 0, z: 0}
position {x: 0, y: 0, z: 0}

LeftFoot:
rotation {x: 0, y: 0, z: 0}
position {x: 0, y: 0, z: 0}
```

### JSON oficial

```json
{
  "animation_name": "contacto_dos_manos_centro_v1",
  "description": "Primitive oficial de contacto a dos manos al centro del torso, util para agarre compacto de espada vertical o arma larga",
  "total_frames": 0,
  "fps": 60,
  "intensity": 1,
  "keyframes": [
    {
      "joint": "Head",
      "frame": 0,
      "rotation": { "y": 0, "x": 0, "z": 0 },
      "position": { "y": 0, "x": 0, "z": 0 }
    },
    {
      "joint": "LeftFoot",
      "frame": 0,
      "rotation": { "y": 0, "x": 0, "z": 0 },
      "position": { "y": 0, "x": 0, "z": 0 }
    },
    {
      "joint": "LeftHand",
      "frame": 0,
      "rotation": { "y": 0, "x": 0, "z": 0 },
      "position": { "y": 0, "x": 0, "z": 0 }
    },
    {
      "joint": "LeftLowerArm",
      "frame": 0,
      "rotation": { "y": 0, "x": 0, "z": 0 },
      "position": { "y": 0, "x": 0, "z": 0 }
    },
    {
      "joint": "LeftLowerLeg",
      "frame": 0,
      "rotation": { "y": 0, "x": 0, "z": 0 },
      "position": { "y": 0, "x": 0, "z": 0 }
    },
    {
      "joint": "LeftUpperArm",
      "frame": 0,
      "rotation": { "y": 42, "x": -55.001, "z": -1.901 },
      "position": { "y": 0.406, "x": -0.001, "z": -0.114 }
    },
    {
      "joint": "LeftUpperLeg",
      "frame": 0,
      "rotation": { "y": 0.512, "x": -2.094, "z": 8.829 },
      "position": { "y": -0.001, "x": 0.002, "z": 0.028 }
    },
    {
      "joint": "LowerTorso",
      "frame": 0,
      "rotation": { "y": 0, "x": 4.61, "z": 0 },
      "position": { "y": 0, "x": 0, "z": 0 }
    },
    {
      "joint": "RightFoot",
      "frame": 0,
      "rotation": { "y": 0, "x": 0, "z": 0 },
      "position": { "y": 0, "x": 0, "z": 0 }
    },
    {
      "joint": "RightHand",
      "frame": 0,
      "rotation": { "y": 0, "x": 0, "z": 0 },
      "position": { "y": 0, "x": 0, "z": 0 }
    },
    {
      "joint": "RightLowerArm",
      "frame": 0,
      "rotation": { "y": 0, "x": 0, "z": 0 },
      "position": { "y": 0, "x": 0, "z": 0 }
    },
    {
      "joint": "RightLowerLeg",
      "frame": 0,
      "rotation": { "y": 0, "x": 0, "z": 0 },
      "position": { "y": 0, "x": 0, "z": 0 }
    },
    {
      "joint": "RightUpperArm",
      "frame": 0,
      "rotation": { "y": -38.242, "x": -66.465, "z": -1.998 },
      "position": { "y": 0.469, "x": -0.006, "z": -0.208 }
    },
    {
      "joint": "RightUpperLeg",
      "frame": 0,
      "rotation": { "y": 0, "x": 0, "z": -12.656 },
      "position": { "y": 0, "x": 0, "z": -0.031 }
    },
    {
      "joint": "UpperTorso",
      "frame": 0,
      "rotation": { "y": 0, "x": 0, "z": 0 },
      "position": { "y": 0, "x": 0, "z": 0 }
    }
  ]
}
```

### Estado oficial de la primitive

**Estado actual:** válida como primitive oficial V1 de contacto central compacto.
**Observación:** prioriza convergencia visual real por encima de simetría numérica perfecta.
**Uso recomendado:** espadas verticales, agarres compactos, guardias cerradas.

---

# Actualización oficial — Golpe recto derecho Roblox R15 validado

## `GOLPE_RECTO_DERECHO_ROBLOX_V1`

### Estado

**Validado por corrección visual del usuario** como base funcional para el golpe derecho.

Esta acción queda incorporada como referencia oficial para futuros golpes rectos del brazo derecho, especialmente cuando se busca una lectura más **Roblox**, rígida, directa y menos anatómica.

### Corrección importante del skill

Antes se asumió que `RightLowerArm` debía mantenerse completamente neutro durante todo el impacto.  
La corrección visual muestra que esa regla era incompleta.

La regla ajustada queda así:

- `RightUpperArm` sigue siendo el driver principal del golpe.
- `RightLowerArm.x` debe mantenerse en `0` para evitar que el antebrazo se doble hacia abajo.
- `RightLowerArm.y` debe mantenerse en `0` durante este golpe.
- `RightLowerArm.z` sí puede usarse como corrección Roblox del antebrazo durante el impacto.
- `RightHand` no lidera; solo refina con microajuste.
- `RightUpperArm.position.x` negativo ayuda a proyectar/alinear el brazo hacia el golpe.
- `RightUpperArm.position.z` negativo ayuda a colocar el brazo hacia atrás/profundidad sin romper la lectura.
- `RightUpperArm.position.y` debe usarse con cuidado; valores muy altos o muy negativos pueden deformar la lectura.

### Regla específica para `RightLowerArm` en golpe derecho

Para golpe recto derecho estilo Roblox:

```txt
RightLowerArm:
rotation.x = 0
rotation.y = 0
rotation.z = 0 en guardia, anticipación y recuperación
rotation.z ≈ 23 a 54 durante pre-impacto, impacto y hold
```

Lectura validada:

- `RightLowerArm.x` positivo dobla el antebrazo hacia abajo y debe evitarse para golpe recto.
- `RightLowerArm.z` positivo fue útil para alinear el antebrazo en el impacto del golpe derecho.
- La mano no debe corregir el error del antebrazo.

### Timing oficial validado

La acción validada usa estos momentos:

```txt
frame 41: guardia/base inicial
frame 46: anticipación/carga atrás
frame 51: salida/proyección del golpe
frame 56: pre-impacto
frame 59: impacto principal
frame 61: hold corto
frame 65: recoil/recogida inicial
frame 71: recuperación
frame 77: cierre a guardia/base
```

Para generar nuevas animaciones desde cero, el skill puede normalizar esta secuencia a:

```txt
frame 0: guardia/base inicial
frame 5: anticipación/carga atrás
frame 10: salida/proyección
frame 15: pre-impacto
frame 18: impacto
frame 20: hold corto
frame 24: recoil
frame 30: recuperación
frame 36: cierre
```

### Poses clave del brazo derecho

#### Guardia / base

```txt
RightUpperArm:
rotation {y: 8, x: -18.003, z: -16.003}
position {y: 0, x: 0, z: 0}

RightLowerArm:
rotation {y: 0, x: 0, z: 0}
position {y: 0, x: 0, z: 0}

RightHand:
rotation {y: -2.003, x: 0, z: 1}
position {y: 0, x: 0, z: 0}
```

#### Anticipación

```txt
RightUpperArm:
rotation {y: 10, x: -28.002, z: -13.002}
position {y: 0, x: 0, z: -0.02}

RightLowerArm:
rotation {y: 0, x: 0, z: 0}
```

#### Salida del golpe

```txt
RightUpperArm:
rotation {y: -10.002, x: -64.002, z: -16.002}
position {y: -0.082, x: 0, z: -0.04}

RightLowerArm:
rotation {y: 0, x: 0, z: 0}
```

#### Pre-impacto

```txt
RightUpperArm:
rotation {y: 14.672, x: -88.545, z: -22.384}
position {y: -0.134, x: -0.093, z: -0.06}

RightLowerArm:
rotation {y: 0, x: 0, z: 23.666}
```

#### Impacto principal

```txt
RightUpperArm:
rotation {y: 76.281, x: -86.884, z: -25.137}
position {y: 0.028, x: -0.18, z: -0.064}

RightLowerArm:
rotation {y: 0, x: 0, z: 51.985}

RightHand:
rotation {y: -4.002, x: 0, z: 1}
```

#### Hold corto

```txt
RightUpperArm:
rotation {y: 60.715, x: -88.106, z: -23.63}
position {y: -0.022, x: -0.161, z: -0.062}

RightLowerArm:
rotation {y: 0, x: 0, z: 53.14}
```

#### Recoil

```txt
RightUpperArm:
rotation {y: -26.484, x: -101.079, z: -22.585}
position {y: 0.16, x: 0.022, z: -0.01}

RightLowerArm:
rotation {y: 0, x: 0, z: 0}
```

### Reglas de uso para futuros golpes derechos

1. No generar golpe recto derecho usando `RightLowerArm.x` como extensión.
2. No corregir el golpe desde `RightHand`.
3. Usar `RightUpperArm` como driver principal del recorrido.
4. Usar `RightLowerArm.z` solo en la fase de impacto si el brazo necesita lectura Roblox rígida.
5. Usar `LowerTorso` y `UpperTorso` para dar potencia, pero sin romper la dirección del brazo.
6. Conservar un hold corto después del impacto.
7. Añadir recoil antes de volver a guardia.
8. Mantener frame inicial y final completos.

### JSON oficial validado

```json
{
  "keyframes": [
    {
      "joint": "Head",
      "frame": 41,
      "rotation": {
        "y": 0,
        "x": 0,
        "z": 0
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "LeftFoot",
      "frame": 41,
      "rotation": {
        "y": -3.003,
        "x": -4.003,
        "z": 0
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "LeftHand",
      "frame": 41,
      "rotation": {
        "y": 2,
        "x": 2,
        "z": -1.003
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "LeftLowerArm",
      "frame": 41,
      "rotation": {
        "y": 0,
        "x": 8,
        "z": -2.003
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "LeftLowerLeg",
      "frame": 41,
      "rotation": {
        "y": 0,
        "x": 10,
        "z": 0
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "LeftUpperArm",
      "frame": 41,
      "rotation": {
        "y": 8,
        "x": -18.003,
        "z": 16
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "LeftUpperLeg",
      "frame": 41,
      "rotation": {
        "y": -2.003,
        "x": 3,
        "z": 9
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "LowerTorso",
      "frame": 41,
      "rotation": {
        "y": 0,
        "x": 1,
        "z": 0
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "RightFoot",
      "frame": 41,
      "rotation": {
        "y": 3,
        "x": -4.003,
        "z": 0
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "RightHand",
      "frame": 41,
      "rotation": {
        "y": -2.003,
        "x": 0,
        "z": 1
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "RightLowerArm",
      "frame": 41,
      "rotation": {
        "y": 0,
        "x": 0,
        "z": 0
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "RightLowerLeg",
      "frame": 41,
      "rotation": {
        "y": 0,
        "x": 10,
        "z": 0
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "RightUpperArm",
      "frame": 41,
      "rotation": {
        "y": 8,
        "x": -18.003,
        "z": -16.003
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "RightUpperLeg",
      "frame": 41,
      "rotation": {
        "y": 2,
        "x": 3,
        "z": -9.003
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "UpperTorso",
      "frame": 41,
      "rotation": {
        "y": 0,
        "x": -2.003,
        "z": 0
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "Head",
      "frame": 46,
      "rotation": {
        "y": -2.002,
        "x": 0,
        "z": 0
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "LeftFoot",
      "frame": 46,
      "rotation": {
        "y": -3.003,
        "x": -4.003,
        "z": 0
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "LeftHand",
      "frame": 46,
      "rotation": {
        "y": 2,
        "x": 2,
        "z": -1.003
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "LeftLowerArm",
      "frame": 46,
      "rotation": {
        "y": 0,
        "x": 10,
        "z": -3.002
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "LeftLowerLeg",
      "frame": 46,
      "rotation": {
        "y": 0,
        "x": 10,
        "z": 0
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "LeftUpperArm",
      "frame": 46,
      "rotation": {
        "y": 7,
        "x": -15.002,
        "z": 20
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "LeftUpperLeg",
      "frame": 46,
      "rotation": {
        "y": -3.002,
        "x": 5,
        "z": 10
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "LowerTorso",
      "frame": 46,
      "rotation": {
        "y": -7.002,
        "x": 0,
        "z": -2.002
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": -0.014
      }
    },
    {
      "joint": "RightFoot",
      "frame": 46,
      "rotation": {
        "y": 3,
        "x": -4.003,
        "z": 0
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "RightHand",
      "frame": 46,
      "rotation": {
        "y": -3.002,
        "x": 0,
        "z": 1
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "RightLowerArm",
      "frame": 46,
      "rotation": {
        "y": 0,
        "x": 0,
        "z": 0
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "RightLowerLeg",
      "frame": 46,
      "rotation": {
        "y": 0,
        "x": 10,
        "z": 0
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "RightUpperArm",
      "frame": 46,
      "rotation": {
        "y": 10,
        "x": -28.002,
        "z": -13.002
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": -0.02
      }
    },
    {
      "joint": "RightUpperLeg",
      "frame": 46,
      "rotation": {
        "y": 3,
        "x": 4,
        "z": -10.002
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "UpperTorso",
      "frame": 46,
      "rotation": {
        "y": -10.002,
        "x": -4.002,
        "z": 2
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "Head",
      "frame": 51,
      "rotation": {
        "y": 2,
        "x": 0,
        "z": 0
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "LeftFoot",
      "frame": 51,
      "rotation": {
        "y": -4.002,
        "x": -7.002,
        "z": 0
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "LeftHand",
      "frame": 51,
      "rotation": {
        "y": 2,
        "x": 2,
        "z": -1.003
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "LeftLowerArm",
      "frame": 51,
      "rotation": {
        "y": 0,
        "x": 12,
        "z": -4.002
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "LeftLowerLeg",
      "frame": 51,
      "rotation": {
        "y": 0,
        "x": 15,
        "z": 0
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "LeftUpperArm",
      "frame": 51,
      "rotation": {
        "y": 8,
        "x": -23.002,
        "z": 21
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "LeftUpperLeg",
      "frame": 51,
      "rotation": {
        "y": -4.002,
        "x": 7,
        "z": 12
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "LowerTorso",
      "frame": 51,
      "rotation": {
        "y": 4,
        "x": -1.002,
        "z": 1
      },
      "position": {
        "y": -0.008,
        "x": 0,
        "z": 0.015
      }
    },
    {
      "joint": "RightFoot",
      "frame": 51,
      "rotation": {
        "y": 3,
        "x": -4.003,
        "z": 0
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "RightHand",
      "frame": 51,
      "rotation": {
        "y": -4.002,
        "x": 0,
        "z": 1
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "RightLowerArm",
      "frame": 51,
      "rotation": {
        "y": 0,
        "x": 0,
        "z": 0
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "RightLowerLeg",
      "frame": 51,
      "rotation": {
        "y": 0,
        "x": 10,
        "z": 0
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "RightUpperArm",
      "frame": 51,
      "rotation": {
        "y": -10.002,
        "x": -64.002,
        "z": -16.002
      },
      "position": {
        "y": -0.082,
        "x": 0,
        "z": -0.04
      }
    },
    {
      "joint": "RightUpperLeg",
      "frame": 51,
      "rotation": {
        "y": 2,
        "x": 2,
        "z": -9.002
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "UpperTorso",
      "frame": 51,
      "rotation": {
        "y": 10,
        "x": 0,
        "z": -1.002
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "Head",
      "frame": 56,
      "rotation": {
        "y": 5,
        "x": -1.002,
        "z": 0
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "LeftFoot",
      "frame": 56,
      "rotation": {
        "y": -5.002,
        "x": -8.002,
        "z": 0
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "LeftHand",
      "frame": 56,
      "rotation": {
        "y": 2,
        "x": 3,
        "z": -1.002
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "LeftLowerArm",
      "frame": 56,
      "rotation": {
        "y": 0,
        "x": 14,
        "z": -4.002
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "LeftLowerLeg",
      "frame": 56,
      "rotation": {
        "y": 0,
        "x": 17,
        "z": 0
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "LeftUpperArm",
      "frame": 56,
      "rotation": {
        "y": 10,
        "x": -30.002,
        "z": 22
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "LeftUpperLeg",
      "frame": 56,
      "rotation": {
        "y": -5.002,
        "x": 8,
        "z": 13
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "LowerTorso",
      "frame": 56,
      "rotation": {
        "y": 13,
        "x": -2.002,
        "z": 1
      },
      "position": {
        "y": -0.014,
        "x": 0,
        "z": 0.035
      }
    },
    {
      "joint": "RightFoot",
      "frame": 56,
      "rotation": {
        "y": 3,
        "x": -4.003,
        "z": 0
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "RightHand",
      "frame": 56,
      "rotation": {
        "y": -4.002,
        "x": 0,
        "z": 1
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "RightLowerArm",
      "frame": 56,
      "rotation": {
        "y": 0,
        "x": 0,
        "z": 23.666
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "RightLowerLeg",
      "frame": 56,
      "rotation": {
        "y": 0,
        "x": 8,
        "z": 0
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "RightUpperArm",
      "frame": 56,
      "rotation": {
        "y": 14.672,
        "x": -88.545,
        "z": -22.384
      },
      "position": {
        "y": -0.134,
        "x": -0.093,
        "z": -0.06
      }
    },
    {
      "joint": "RightUpperLeg",
      "frame": 56,
      "rotation": {
        "y": 2,
        "x": 2,
        "z": -9.002
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "UpperTorso",
      "frame": 56,
      "rotation": {
        "y": 18,
        "x": 3,
        "z": -2.002
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "Head",
      "frame": 59,
      "rotation": {
        "y": 5,
        "x": -1.002,
        "z": 0
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "LeftFoot",
      "frame": 59,
      "rotation": {
        "y": -5.002,
        "x": -8.002,
        "z": 0
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "LeftHand",
      "frame": 59,
      "rotation": {
        "y": 2,
        "x": 3,
        "z": -1.002
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "LeftLowerArm",
      "frame": 59,
      "rotation": {
        "y": 0,
        "x": 14,
        "z": -4.002
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "LeftLowerLeg",
      "frame": 59,
      "rotation": {
        "y": 0,
        "x": 17,
        "z": 0
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "LeftUpperArm",
      "frame": 59,
      "rotation": {
        "y": 10,
        "x": -31.002,
        "z": 22
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "LeftUpperLeg",
      "frame": 59,
      "rotation": {
        "y": -5.002,
        "x": 8,
        "z": 13
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "LowerTorso",
      "frame": 59,
      "rotation": {
        "y": 15,
        "x": -2.002,
        "z": 1
      },
      "position": {
        "y": -0.016,
        "x": 0,
        "z": 0.045
      }
    },
    {
      "joint": "RightFoot",
      "frame": 59,
      "rotation": {
        "y": 3,
        "x": -4.003,
        "z": 0
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "RightHand",
      "frame": 59,
      "rotation": {
        "y": -4.002,
        "x": 0,
        "z": 1
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "RightLowerArm",
      "frame": 59,
      "rotation": {
        "y": 0,
        "x": 0,
        "z": 51.985
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "RightLowerLeg",
      "frame": 59,
      "rotation": {
        "y": 0,
        "x": 8,
        "z": 0
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "RightUpperArm",
      "frame": 59,
      "rotation": {
        "y": 76.281,
        "x": -86.884,
        "z": -25.137
      },
      "position": {
        "y": 0.028,
        "x": -0.18,
        "z": -0.064
      }
    },
    {
      "joint": "RightUpperLeg",
      "frame": 59,
      "rotation": {
        "y": 2,
        "x": 2,
        "z": -9.002
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "UpperTorso",
      "frame": 59,
      "rotation": {
        "y": 21,
        "x": 4,
        "z": -2.002
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "Head",
      "frame": 61,
      "rotation": {
        "y": 5,
        "x": -1.002,
        "z": 0
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "LeftFoot",
      "frame": 61,
      "rotation": {
        "y": -5.002,
        "x": -8.002,
        "z": 0
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "LeftHand",
      "frame": 61,
      "rotation": {
        "y": 2,
        "x": 3,
        "z": -1.002
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "LeftLowerArm",
      "frame": 61,
      "rotation": {
        "y": 0,
        "x": 14,
        "z": -4.002
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "LeftLowerLeg",
      "frame": 61,
      "rotation": {
        "y": 0,
        "x": 17,
        "z": 0
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "LeftUpperArm",
      "frame": 61,
      "rotation": {
        "y": 10,
        "x": -30.002,
        "z": 22
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "LeftUpperLeg",
      "frame": 61,
      "rotation": {
        "y": -5.002,
        "x": 8,
        "z": 13
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "LowerTorso",
      "frame": 61,
      "rotation": {
        "y": 14,
        "x": -1.002,
        "z": 1
      },
      "position": {
        "y": -0.014,
        "x": 0,
        "z": 0.04
      }
    },
    {
      "joint": "RightFoot",
      "frame": 61,
      "rotation": {
        "y": 3,
        "x": -4.003,
        "z": 0
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "RightHand",
      "frame": 61,
      "rotation": {
        "y": -4.002,
        "x": 0,
        "z": 1
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "RightLowerArm",
      "frame": 61,
      "rotation": {
        "y": 0,
        "x": 0,
        "z": 53.14
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "RightLowerLeg",
      "frame": 61,
      "rotation": {
        "y": 0,
        "x": 8,
        "z": 0
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "RightUpperArm",
      "frame": 61,
      "rotation": {
        "y": 60.715,
        "x": -88.106,
        "z": -23.63
      },
      "position": {
        "y": -0.022,
        "x": -0.161,
        "z": -0.062
      }
    },
    {
      "joint": "RightUpperLeg",
      "frame": 61,
      "rotation": {
        "y": 2,
        "x": 3,
        "z": -9.003
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "UpperTorso",
      "frame": 61,
      "rotation": {
        "y": 19,
        "x": 3,
        "z": -2.002
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "Head",
      "frame": 65,
      "rotation": {
        "y": 2,
        "x": 0,
        "z": 0
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "LeftFoot",
      "frame": 65,
      "rotation": {
        "y": -4.002,
        "x": -5.002,
        "z": 0
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "LeftHand",
      "frame": 65,
      "rotation": {
        "y": 2,
        "x": 2,
        "z": -1.003
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "LeftLowerArm",
      "frame": 65,
      "rotation": {
        "y": 0,
        "x": 11,
        "z": -3.002
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "LeftLowerLeg",
      "frame": 65,
      "rotation": {
        "y": 0,
        "x": 12,
        "z": 0
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "LeftUpperArm",
      "frame": 65,
      "rotation": {
        "y": 9,
        "x": -22.002,
        "z": 20
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "LeftUpperLeg",
      "frame": 65,
      "rotation": {
        "y": -3.002,
        "x": 5,
        "z": 10
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "LowerTorso",
      "frame": 65,
      "rotation": {
        "y": 5,
        "x": -1.002,
        "z": 0
      },
      "position": {
        "y": -0.006,
        "x": 0,
        "z": 0.015
      }
    },
    {
      "joint": "RightFoot",
      "frame": 65,
      "rotation": {
        "y": 3,
        "x": -4.003,
        "z": 0
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "RightHand",
      "frame": 65,
      "rotation": {
        "y": -3.002,
        "x": 0,
        "z": 1
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "RightLowerArm",
      "frame": 65,
      "rotation": {
        "y": 0,
        "x": 0,
        "z": 0
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "RightLowerLeg",
      "frame": 65,
      "rotation": {
        "y": 0,
        "x": 10,
        "z": 0
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "RightUpperArm",
      "frame": 65,
      "rotation": {
        "y": -26.484,
        "x": -101.079,
        "z": -22.585
      },
      "position": {
        "y": 0.16,
        "x": 0.022,
        "z": -0.01
      }
    },
    {
      "joint": "RightUpperLeg",
      "frame": 65,
      "rotation": {
        "y": 2,
        "x": 3,
        "z": -9.003
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "UpperTorso",
      "frame": 65,
      "rotation": {
        "y": 7,
        "x": 0,
        "z": -1.002
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "Head",
      "frame": 71,
      "rotation": {
        "y": -1.002,
        "x": 0,
        "z": 0
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "LeftFoot",
      "frame": 71,
      "rotation": {
        "y": -3.003,
        "x": -4.003,
        "z": 0
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "LeftHand",
      "frame": 71,
      "rotation": {
        "y": 2,
        "x": 2,
        "z": -1.003
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "LeftLowerArm",
      "frame": 71,
      "rotation": {
        "y": 0,
        "x": 9,
        "z": -3.002
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "LeftLowerLeg",
      "frame": 71,
      "rotation": {
        "y": 0,
        "x": 10,
        "z": 0
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "LeftUpperArm",
      "frame": 71,
      "rotation": {
        "y": 8,
        "x": -18.002,
        "z": 18
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "LeftUpperLeg",
      "frame": 71,
      "rotation": {
        "y": -2.003,
        "x": 3,
        "z": 9
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "LowerTorso",
      "frame": 71,
      "rotation": {
        "y": -2.002,
        "x": 0,
        "z": -1.002
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "RightFoot",
      "frame": 71,
      "rotation": {
        "y": 3,
        "x": -4.003,
        "z": 0
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "RightHand",
      "frame": 71,
      "rotation": {
        "y": -3.002,
        "x": 0,
        "z": 1
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "RightLowerArm",
      "frame": 71,
      "rotation": {
        "y": 0,
        "x": 0,
        "z": 0
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "RightLowerLeg",
      "frame": 71,
      "rotation": {
        "y": 0,
        "x": 10,
        "z": 0
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "RightUpperArm",
      "frame": 71,
      "rotation": {
        "y": 7,
        "x": -30.002,
        "z": -12.002
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": -0.017
      }
    },
    {
      "joint": "RightUpperLeg",
      "frame": 71,
      "rotation": {
        "y": 2,
        "x": 3,
        "z": -9.003
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "UpperTorso",
      "frame": 71,
      "rotation": {
        "y": -4.002,
        "x": -2.002,
        "z": 1
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "Head",
      "frame": 77,
      "rotation": {
        "y": 0,
        "x": 0,
        "z": 0
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "LeftFoot",
      "frame": 77,
      "rotation": {
        "y": -3.003,
        "x": -4.003,
        "z": 0
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "LeftHand",
      "frame": 77,
      "rotation": {
        "y": 2,
        "x": 2,
        "z": -1.003
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "LeftLowerArm",
      "frame": 77,
      "rotation": {
        "y": 0,
        "x": 8,
        "z": -2.003
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "LeftLowerLeg",
      "frame": 77,
      "rotation": {
        "y": 0,
        "x": 10,
        "z": 0
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "LeftUpperArm",
      "frame": 77,
      "rotation": {
        "y": 8,
        "x": -18.003,
        "z": 16
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "LeftUpperLeg",
      "frame": 77,
      "rotation": {
        "y": -2.003,
        "x": 3,
        "z": 9
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "LowerTorso",
      "frame": 77,
      "rotation": {
        "y": 0,
        "x": 1,
        "z": 0
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "RightFoot",
      "frame": 77,
      "rotation": {
        "y": 3,
        "x": -4.003,
        "z": 0
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "RightHand",
      "frame": 77,
      "rotation": {
        "y": -2.003,
        "x": 0,
        "z": 1
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "RightLowerArm",
      "frame": 77,
      "rotation": {
        "y": 0,
        "x": 0,
        "z": 0
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "RightLowerLeg",
      "frame": 77,
      "rotation": {
        "y": 0,
        "x": 10,
        "z": 0
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "RightUpperArm",
      "frame": 77,
      "rotation": {
        "y": 8,
        "x": -18.003,
        "z": -16.003
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "RightUpperLeg",
      "frame": 77,
      "rotation": {
        "y": 2,
        "x": 3,
        "z": -9.003
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    },
    {
      "joint": "UpperTorso",
      "frame": 77,
      "rotation": {
        "y": 0,
        "x": -2.003,
        "z": 0
      },
      "position": {
        "y": 0,
        "x": 0,
        "z": 0
      }
    }
  ],
  "animation_name": "TemplateR15",
  "target_name": "TemplateR15",
  "intensity": 1,
  "fps": 24,
  "description": "description_814692",
  "total_frames": 300
}
```

### Estado oficial de la acción

**Estado actual:** válida como acción oficial V1 para golpe recto derecho estilo Roblox.  
**Uso recomendado:** puñete recto derecho, jab derecho estilizado, ataque frontal corto, animaciones de combate R15 con estética Roblox.  
**Regla crítica aprendida:** `RightLowerArm.z` positivo puede ser útil en impacto; `RightLowerArm.x` positivo debe evitarse porque dobla el antebrazo hacia abajo.

