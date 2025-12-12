---
layout: default
title: 2. Entorno de desarrollo en PC
nav_order: 3
---

# 2. Entorno de desarrollo en PC (Windows)

Objetivo: tener un entorno estable para compilar a Quest (Android) y desarrollar en Unity sin pelearte con dependencias.

---

## 1) Versiones elegidas (decisión técnica)

### Unity
- ✅ Se recomienda usar **Unity 2022.3 LTS** para esta fase de setup y proyectos iniciales.
- Instalado: **Unity 2022.3.62f3 (LTS)**

> Nota: aunque tengas Unity 6 instalado, para “base Quest + SDKs + estabilidad”, esta documentación usa Unity 2022.3 LTS.

### IDE
- ✅ **Visual Studio Community 2022**
- Workload requerido:
  - **Game development with Unity**

---

## 2) Instalación: Unity Hub + Unity Editor

1. Instala **Unity Hub**.
2. En Unity Hub → **Installs** → instala **Unity 2022.3 LTS**.
3. En la pantalla de módulos marca:

### Módulos obligatorios
- ✅ **Android Build Support**
  - ✅ Android SDK & NDK Tools
  - ✅ OpenJDK
- ✅ **Windows Build Support (IL2CPP)**

### Módulos opcionales
- ⬜ macOS Build Support (solo si planeas compilar o mover proyectos a Mac)

---

## 3) Visual Studio 2022 (configuración recomendada)

En el **Visual Studio Installer**:

1. Selecciona Visual Studio 2022 → **Modificar**
2. Marca:
   - ✅ **Game development with Unity**
3. (Opcional) marca:
   - ⬜ **.NET desktop development**

✅ Resultado esperado:
- Unity detecta Visual Studio como editor externo y el autocompletado funciona.

---

## 4) Ajustes clave dentro de Unity (cuando abras un proyecto)

En Unity Editor:

1. **Edit → Preferences → External Tools**
2. Verifica:
   - External Script Editor: **Visual Studio 2022**
3. (En Android) Unity suele traer SDK/NDK/JDK “embedded”.
   - Recomendación: usa el toolchain que instala Unity con el módulo Android (menos conflictos).

---

## 5) Primera prueba de sanity check (antes de XR)

Crea un proyecto base:

1. Unity Hub → Projects → New Project
2. Editor: **Unity 2022.3.62f3**
3. Template: **3D (Core)**
4. Nombre: `Quest3_HolaMundo`

Dentro del proyecto:

5. File → Build Settings…
6. Plataforma: **Android**
7. Switch Platform

✅ Resultado esperado:
- No hay errores rojos.
- Android aparece como plataforma activa.

---

## 6) Problemas comunes y tips

### “Android module not installed”
- Te faltó marcar **Android Build Support** o no instalaste SDK/NDK/OpenJDK.

### “Unity no detecta Visual Studio”
- Revisa el workload “Game development with Unity”.
- Revisa Unity → Preferences → External Tools.

### “Tengo Unity 6 y Unity 2022”
- Usa **2022** para esta documentación.
- Unity 6 lo puedes dejar para más adelante cuando todo lo base esté estable.

---

## 7) Qué sigue después de este documento

Con Quest en Developer Mode + Unity 2022.3 con Android listo:

- Crear el primer proyecto orientado a Quest
- Montar una UI simple (Canvas + botón)
- “Hola mundo” en `Debug.Log`
- Luego: enviar “Hola mundo” a la PC por red (HTTP) como prueba de comunicación base (primer paso a gemelo digital)
