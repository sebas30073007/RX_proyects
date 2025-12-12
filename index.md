---
title: Home
layout: home
---

This is a *bare-minimum* template to create a Jekyll site that uses the [Just the Docs] theme. You can easi---
layout: default
title: Inicio
nav_order: 1
---

# Laboratorio XR · Meta Quest 3S + Unity (Base)

Este repo documenta los **primeros pasos** para desarrollar en **Meta Quest 3S** con **Unity (LTS)**, desde cero y con enfoque práctico.

La meta a mediano plazo es llegar a **gemelos digitales** (digital twins) para robots/plataformas, pero aquí se cubre primero lo esencial: cuentas, instalación, configuración base y pruebas mínimas que confirman que el entorno funciona.

---

## Qué sí cubre este repo (por ahora)

- ✅ Alta y verificación de **cuenta de desarrollador** en Meta Horizon.
- ✅ Activación de **Modo Desarrollador** en el visor.
- ✅ Instalación base en PC: **Unity Hub + Unity 2022.3 LTS + módulos Android + Visual Studio**.
- ✅ Primeras pruebas “sanity check” (proyecto Unity en blanco, plataforma Android, etc.).

---

## Qué NO cubre (todavía)

- ❌ Integración completa de **Meta XR All-in-One SDK / OpenXR**.
- ❌ Passthrough, hand tracking, guardian, etc.
- ❌ Arquitecturas de gemelo digital (sincronización, teleoperación, streams, ROS2, Vicon, etc.).
- ❌ Protocolos avanzados (WebSockets/UDP/OSC/MQTT) — se documentará después.

> Nota: Estos temas se documentarán en páginas futuras y/o en ramas `proj/*` cuando cada proyecto ya tenga forma.

---

## Convenciones del repo

- **Rama `main`**: documentación estable y reutilizable.
- **Ramas `lab/*`**: experimentos y pruebas rápidas.
- **Ramas `proj/*`**: proyectos grandes (gemelos digitales, teleoperación, integración con robots).

Ejemplos:
- `lab/quest-basics`
- `proj/ur3-digital-twin`
- `proj/qcar-digital-twin`

---

## Checklist rápido (si quieres validar que ya estás “listo”)

- [ ] Cuenta Meta **verificada** como developer (2FA o tarjeta / verificación completada).
- [ ] **Developer Mode** ON en el visor (desde la app).
- [ ] Unity Hub instalado.
- [ ] Unity **2022.3 LTS** instalado con **Android Build Support (SDK/NDK + OpenJDK)**.
- [ ] Visual Studio 2022 con workload **Game development with Unity**.
- [ ] Proyecto Unity creado y plataforma **Android** seleccionada sin errores.

---

## Roadmap corto (por fases)

**Fase 1 — Setup y pruebas base**
- Cuenta developer + dev mode
- Unity + módulos Android
- Proyecto base y build settings OK

**Fase 2 — XR básico**
- OpenXR + Meta XR SDK
- XR Rig + Interacción simple
- UI en VR (botón) funcionando

**Fase 3 — Primer pipeline de gemelo digital**
- Quest → PC (comandos)
- PC → robot (API/SDK)
- Robot → PC (estado/pose)
- PC → Quest (visualización del gemelo)

---

## Dónde empezar

1) 👉 [1. Configuración de desarrollador en Meta Quest 3S](./01_quest_setup)  
2) 👉 [2. Entorno de desarrollo en PC](./02_dev_env_pc)

---

## Notas personales / mantenimiento

- Mantén esta documentación “mínima pero útil”: pasos + checklists + problemas reales + soluciones.
- Lo que ya no uses, mándalo al apéndice de troubleshooting.
- Si un paso te tomó 2 horas por un bug, **va aquí**. Eso es lo que vale oro después.
ly set the created site to be published on [GitHub Pages] – the [README] file explains how to do that, along with other details.
