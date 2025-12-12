---
layout: default
title: 1. Configuración de desarrollador en Meta Quest 3S
nav_order: 2
---

# 1. Configuración de desarrollador en Meta Quest 3S

Objetivo: dejar el visor listo para **instalar apps propias** (sideload) y desarrollar con Unity, sin depender de la tienda.

---

## 1) Requisitos (antes de tocar Unity)

- Cuenta Meta/Horizon iniciada en el visor.
- App móvil de Meta instalada:
  - Android/iOS (la app puede verse como **Meta Horizon** o **Meta Quest** según región/versión).
- Visor emparejado con la app (debe aparecer en **Dispositivos** y mostrar batería/Wi-Fi).

---

## 2) Alta como desarrollador (Web)

1. En PC, entra al panel de desarrolladores de Meta Horizon.
2. Inicia sesión con la **misma cuenta** que usas en el visor.
3. Crea una **organización / team** (ej. `SebasXR`).
4. Verifica la cuenta:
   - Activando **2FA**, o
   - agregando método de verificación solicitado por Meta.

✅ Resultado esperado:
- En el panel web debe aparecer que **tu cuenta de desarrollador está verificada**.

---

## 3) Activar Developer Mode (App del teléfono)

En la app:

1. Menú → **Dispositivos** → selecciona tu **Meta Quest 3S**
2. Entra a **Configuración del visor**
3. Busca **Configuración para desarrolladores** / **Developer settings**
4. Activa **Modo desarrollador** (switch ON)

✅ Resultado esperado:
- Debe existir un **interruptor**, no un botón de “Empezar”.

---

## 4) Conectar a PC y aceptar USB Debugging (recomendado)

Aunque no siempre es obligatorio para todo, es muy útil para debug:

1. Conecta Quest 3S a la PC con USB-C.
2. Ponte el visor.
3. Acepta:
   - “Permitir depuración USB”  
   - (si aparece) marca “Confiar siempre en este equipo”

✅ Resultado esperado:
- El visor permite instalación/debug desde PC sin pedir permiso cada vez.

---

## 5) Troubleshooting real: cuando NO aparece el switch (solo sale “Empezar”)

Síntoma:
- En la app, en “Configuración para desarrolladores”, no hay switch.
- Solo hay un botón **“Empezar”** que te manda a un link aunque “según tú” ya eres developer.

Causas típicas:
- La app no se actualizó (caché).
- El visor quedó emparejado con un estado “viejo”.
- Verificación incompleta o el team no se reflejó en la app.

### Solución recomendada (de menor a mayor impacto)

#### A) Forzar actualización de la app (Android)
1. Cierra la app (que no quede en segundo plano).
2. Ajustes del teléfono → Apps → Meta Horizon/Quest → **Forzar detención**.
3. **Borrar caché** (no datos, si se puede evitar).
4. Abre la app y revisa otra vez.

#### B) Re-emparejar
1. En la app → Dispositivos → visor → “Olvidar / Desvincular”.
2. Vuelve a emparejar el visor desde cero.

#### C) Solución definitiva (la que destrabó el caso)
✅ **Factory Reset del visor + re-emparejar**:

- Apaga el visor.
- Mantén **Power + Volumen abajo** hasta que salga el menú de arranque.
- Selecciona **Factory Reset**.
- Configura el visor como nuevo en la app.

Resultado:
- Después del reset + re-emparejar, el **Modo desarrollador** ya apareció como switch y quedó funcional.

---

## 6) Checklist final (si ya quedó bien)

- [ ] En la app aparece el switch de **Modo desarrollador**.
- [ ] El visor se conecta y sincroniza con la app (muestra batería/Wi-Fi).
- [ ] En conexión USB, aceptaste **USB debugging**.
- [ ] Ya estás listo para Unity (siguiente documento).
