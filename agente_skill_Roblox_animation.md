🧠 Moon Animator R15 AI Skill (v0.1)
🎯 Objetivo

Generar animaciones R15 en JSON para Moon Animator de forma:

coherente

reutilizable

basada en poses

sin errores de eje o simetría

📦 1. Estructura JSON (Contrato Oficial)
{
  "animation_name": "string",
  "description": "string",
  "total_frames": 30,
  "fps": 60,
  "intensity": 0.7,
  "keyframes": [
    {
      "joint": "RightUpperArm",
      "frame": 0,
      "rotation": { "x": 0, "y": 0, "z": 0 },
      "position": { "x": 0, "y": 0, "z": 0 }
    }
  ]
}
🦴 2. Joints válidos (R15)
LowerTorso
UpperTorso
Head
RightUpperArm
RightLowerArm
RightHand
LeftUpperArm
LeftLowerArm
LeftHand
RightUpperLeg
RightLowerLeg
RightFoot
LeftUpperLeg
LeftLowerLeg
LeftFoot
🧱 3. Regla de Frames (CRÍTICA)
Frame 0

✅ DEBE incluir los 15 joints

✅ Pose base obligatoria

✅ Resetea estado del personaje

Frames 1..N

✅ Solo joints que cambian

❌ No repetir todo el cuerpo

🧭 4. Sistema de ejes
Rotación
X → arriba / abajo
Y → hacia adentro / hacia afuera
Z → lateral
Dirección
NEGATIVO → hacia el rostro (adelante)
POSITIVO → hacia la espalda (atrás)
⚠️ 5. Regla CRÍTICA de simetría
RightUpperArm y LeftUpperArm NO son espejo directo
Comportamiento real
RightUpperArm

X negativo → sube hacia adelante

Y negativo → mete hacia el pecho

Y positivo → saca hacia afuera

Z negativo → abre lateralmente

LeftUpperArm

X → igual que derecha

❗ Y → invertido

❗ Z → comportamiento invertido

👉 CONCLUSIÓN:

NO copiar valores entre izquierda y derecha
DEBE haber lógica espejo manual
🧠 6. Reglas biomecánicas base

toda animación inicia con pose base

ataques usan valores negativos (hacia adelante)

debe existir:

anticipación

acción

recuperación

la pierna de apoyo estabiliza

el torso acompaña el movimiento

evitar cambios bruscos entre frames

🧩 7. Pipeline del Skill
input → acción → plantilla → fases → poses clave → interpolación → validación → JSON
🧱 8. Fases estándar
1. Base
2. Anticipación
3. Preparación
4. Ejecución
5. Impacto
6. Retorno
7. Recuperación
🧪 9. Problemas detectados (resueltos)
❌ Brazos hacia atrás

✔ causa: eje invertido

❌ Pose rígida

✔ causa: falta de torso y piernas activas

❌ Mano fuera de guardia

✔ causa: LowerArm sin calibrar

❌ Izquierda ≠ derecha

✔ causa: ejes invertidos por joint

🔥 10. Estado actual
✔ JSON definido
✔ joints definidos
✔ reglas de frame definidas
✔ sistema de ejes definido
✔ asimetría detectada
⏳ falta: calibración LowerArm
⏳ falta: pose base final perfecta
⏳ falta: primera animación real
🚀 SIGUIENTE PASO

Continuamos desde aquí:

[INFO-15]
Calibrar RightLowerArm y LeftLowerArm