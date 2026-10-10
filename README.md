# NeuroGuard — Autonomous ICU Biometric Sentinel & Gestural Perception Engine

> **Autonomous, Non-Invasive Multimodal Perception System for Motor-Impaired and Intubated ICU Bedside Surveillance**

---

## 🏥 Clinical Background & Problem Statement

In Intensive Care Units (ICUs), patients with tracheostomies, mechanical ventilators, acute paralysis, or extreme post-operative weakness face **total communicative deprivation**:
1. **Inability to Speak:** Intubated or dysphonic patients cannot vocalize distress or basic needs.
2. **Loss of Fine Motor Control:** Traditional physical nurse call buttons and handheld remotes fail when patients experience paresis, sudden syncope, or motor fatigue.
3. **ICU Alarm Fatigue & False Positives:** Many camera systems blast false alarms for benign movements (such as opening the mouth to yawn or breathe), leading to dangerous caregiver desensitization.

**NeuroGuard** resolves this through **Autonomous Multimodal Sensory Surveillance**: fusing real-time facial micro-geometry, dual-hand spatial proximity, head kinematics, and acoustic telemetry into a continuous, real-time perception state machine.

---

## ⚡ Technical Architecture

NeuroGuard runs **100% client-side** in any modern web browser with zero external backend dependencies or server latency:

- **Google MediaPipe Face Mesh:** 468 3D facial landmarks tracked at 30+ FPS for ocular aspect ratio (EAR), mouth aspect ratio (MAR), corrugator brow knit (grimace), and zygomatic smile elevation.
- **Google MediaPipe Hands:** 21 3D hand landmarks tracking palm, wrist, and fingertip coordinates relative to the patient's trachea and chin.
- **Temporal Kinematic Analysis:** Rolling FIFO buffers calculate pitch reversals (Nodding: Affirmative) and yaw reversals (Shaking: Negative) without rigid timers.
- **Acoustic Energy Analyzer:** HTML5 Web Audio API `AnalyserNode` monitoring decibel variance to detect vocal groans, gasps, and acute distress cries.
- **Empathetic AI Sentinel ("NeuroGuard Aura"):** Proactive Web Speech synthesis that verifies patient intent, logs clinical cortex rationale, and dispatches bedside orders.

---

## 🎯 Real-Time Gesture & Action Perception Matrix

NeuroGuard does **not** rely on pre-written static text. Every quadrant updates dynamically with live behavioral descriptions:

| Patient Action / Gesture | Biometric Trigger | Dominant Quadrant | Clinical AI Response & Triage |
| :--- | :--- | :--- | :--- |
| **Catch Neck & Hold Tight** | Hands clutching trachea/chin bounding box | **Quad 01: Cardiac & Airway** | 🚨 **ALARM ACTIVATED!** Strobe engages. AI alerts: *"Code Blue! Patient clutching neck! Acute airway obstruction!"* |
| **Laugh / Smile** | Mouth width > 0.44 & zygomatic lift | **Quad 03: Wong-Baker Scale** | Displays `"Laugh"`. AI confirms positive emotional state and comfort. |
| **Feel Dizzy** | Head roll tilt > 16° or lateral sway | **Quad 04: Social Expression** | Displays `"Dizzy / Head Tilted"`. AI advises: *"Please lean back and steady your head."* |
| **Close Eyes (> 2.5s)** | Ocular ratio (EAR) < 0.20 sustained | **Quad 04: Social Expression** | 🚨 **ALARM ACTIVATED!** Displays `"Eyes Closed (Unresponsive)"`. Glasgow Coma Scale drops to 3/15. |
| **Become Statue (Frozen)** | Motion variance < 0.0016 for > 2.5s | **Quad 01: Cardiac & Airway** | 🚨 **ALARM ACTIVATED!** Displays `"Statue / Motionless"`. Catatonia / tonic immobility alert dispatched. |
| **Nod Head (Yes)** | Vertical pitch reversals (+18°) | **Quad 04: Social Expression** | Displays `"Nodding (Yes)"`. Confirms pending nursing order (e.g. Bedside Water). |
| **Shake Head (No)** | Horizontal yaw reversals | **Quad 04: Social Expression** | Displays `"Shaking Head (No)"`. Cancels pending order gracefully. |
| **Open Mouth (Thirsty)** | MAR > 0.26 (Normal posture) | **Quad 02: Nutrition & Water** | **NO ALARM.** Plays gentle chime. AI asks: *"Do you need water? Nod for Yes, shake for No."* |

---

## 🩺 The 4 Dynamic Multimodal Quadrants

The interface features 4 clinical quadrants that dynamically update in real time:

1. **Quadrant 01: CARDIAC & AIRWAY (Code Red)**
   - Monitors respiratory rhythm, choking obstruction, dyspnea, and respiratory arrest.
2. **Quadrant 02: NUTRITION & WATER (Basic Need)**
   - Monitors oral hydration, thirst, aspiration risk, and oral care requests.
3. **Quadrant 03: WONG-BAKER SCALE (Pain Triage)**
   - Continuous 0–10 facial grimace score evaluating eyebrow furrowing and orbital squinting.
4. **Quadrant 04: SOCIAL EXPRESSION (Neuro-Gestural Response)**
   - Tracks affirmative nods, negative shakes, dizziness, eye closure, and responsiveness.

---

## 🚀 Quickstart Guide

### Prerequisites
- Modern web browser: **Google Chrome** or **Microsoft Edge** (recommended for WebGL and MediaPipe performance).
- Standard USB or built-in Webcam and Microphone.

### Running the Project
1. Open the file directly in your browser: