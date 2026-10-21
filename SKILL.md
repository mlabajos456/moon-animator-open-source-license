---
name: roblox-r15-moon-animator
description: Diseña, genera, revisa y corrige animaciones corporales R15 para Moon Animator 2 y produce JSON compatible con el importador AI Fight Animator de este repositorio. Úsalo para poses, locomoción, combate, acting, ciclos y diagnóstico visual R15; no lo trates como guía universal para R6 o rigs personalizados.
metadata:
  short-description: Animación R15 para Moon Animator
---

# Animación R15 para Moon Animator

Genera movimiento claro y utilizable en el rig objetivo. Mantén separados los hechos confirmados por el código, la calibración observada en el avatar y las decisiones artísticas. No presentes valores estimados como reglas universales.

## Flujo

1. Determina la acción, intención, rig, duración, loop, cámara y si el movimiento es in-place o debe trasladar físicamente al personaje. Si falta un detalle menor, asume R15 blocky, 60 FPS, frame inicial 0 e in-place y dilo brevemente.
2. Diseña poses clave legibles: preparación, acción, impacto o contacto, y recuperación. Coordina pelvis, torso y cadena de extremidad; no intentes resolver un gesto solo con la mano o el pie.
3. Produce JSON según el contrato de `references/animation-guide.md`. En particular, `joint` es el nombre de la pieza animada, `frame` es un offset desde el cursor de Moon Animator, los ángulos van en grados XYZ y las posiciones en studs.
4. Revisa estructura, pares joint/frame duplicados, límites de frames, pose inicial/final y supuestos de signo. Para un archivo JSON, ejecuta `python scripts/validate_animation_json.py archivo.json`; añade `--loop` cuando el clip deba repetirse. Corrige todos los errores y atiende las advertencias de joints que el rig R15 estándar no reconoce. No declares easing, prioridad, loop o root motion como propiedades del JSON.
5. Cuando haya visor o evidencia visual, compara el resultado desde frente, perfil y perspectiva en los frames clave; cambia de vista sin mover la pose. Distingue una pose realmente incorrecta de una extremidad acortada por perspectiva. Corrige la silueta y conserva como patrón aprendido solo lo que el usuario confirme. Registra aprobado, rechazado o pendiente en la tabla de aprendizaje de `references/animation-guide.md`; no infieras aprobación por silencio. Si no puedes ver el resultado, etiqueta los números como primera pasada. En el visor de este repositorio puedes cargar una muestra con `?sample=nombre_del_json_sin_extension`.
6. Al insertar en Moon Animator, confirma rig objetivo, cursor, largo de timeline y FPS activo. El importador suma el offset de frame al cursor y no configura easing ni duración por los metadatos del JSON.

## Límites técnicos que afectan decisiones

- Anima offsets de pose del rig; no cambies `Motor6D.C0` o `C1` para crear una animación.
- Un giro visual de `LowerTorso` no equivale a girar el `HumanoidRootPart` ni garantiza desplazamiento físico en gameplay.
- Los signos de rotación dependen del rig, sus pivotes y del adaptador/visor. Calibra en el objetivo en vez de deducirlos solo del nombre del eje.
- Si un signo no está confirmado, usa el panel «Crear prueba de calibración» del visor o `python scripts/create_joint_calibration.py --joint LeftUpperArm --axis z`; deja la cámara fija y observa las secciones positiva y negativa antes de usar el eje en una acción completa. Para traslación usa el canal `position`.
- La extensión de este repositorio resuelve `joint` por nombre de track/pieza y omite joints desconocidos. No asumas compatibilidad con `AnimationConstraint` sin comprobarla.
- El visor local es una aproximación útil para iterar; Studio y el rig final son la validación definitiva.

## Relación con el generador IA del plugin

Esta skill guía a Codex cuando diseña o corrige JSON; el cliente Lua del plugin no la adjunta a la petición. Según `lua-src/Animator/Windows/AIFightAnimator.lua`, la ventana envía `prompt`, `duration`, `intensity` y `target_name` a `http://localhost:8000/generate`, y espera una respuesta con `success: true` y un objeto `animation`. No afirmes que el servidor genera conforme a esta skill mientras su código no cargue estas instrucciones. El contrato observado y sus implicaciones están en `references/animation-guide.md`.

El prompt de sistema listo para incorporar en el backend está en [references/server-generation-prompt.md](references/server-generation-prompt.md). Su interpretación de `duration` es provisional porque la unidad no está definida por el cliente Lua.

## Referencia detallada

Lee [references/animation-guide.md](references/animation-guide.md) cuando necesites el esquema completo, semántica de Motor6D/Pose, convenciones locales calibradas, recetas de movimiento, diagnóstico, protocolo de revisión o fuentes verificadas.
