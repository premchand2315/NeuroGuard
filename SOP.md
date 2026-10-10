================================================================================
STANDARD OPERATING PROCEDURE (SOP)
NEUROGUARD AUTONOMOUS ICU SENTINEL & GESTURAL PERCEPTION SYSTEM
================================================================================
Document ID:     SOP-ICU-NG-004
Effective Date:  October 2026
Department:      Critical Care Medicine & Biomedical Informatics
Target Users:    ICU Staff, Critical Care Nurses, Attending Physicians, Evaluators
Review Cycle:    Annual
================================================================================

1. PURPOSE & CLINICAL SCOPE
--------------------------------------------------------------------------------
This Standard Operating Procedure (SOP) defines the operational guidelines, 
biometric verification steps, emergency escalation paths, and alarm management 
protocols for NeuroGuard Bedside Sentinel #04.

NeuroGuard is deployed to monitor intubated, quadriplegic, postoperative, or 
speech-deprived patients who cannot use physical call buttons.

2. PRE-OPERATION SAFETY & CALIBRATION CHECKLIST
--------------------------------------------------------------------------------
Before arming NeuroGuard at the bedside, verify:
[ ] 1. Camera Positioning: Mount the optical sensor 45–65 cm from patient's 
       face at an angle of 15°–30° downward.
[ ] 2. Field of View (FOV): Ensure the patient's face, neck, and upper chest 
       are fully visible without occluding blankets.
[ ] 3. Lighting: Maintain minimum ambient clinical illumination (> 250 lux).
[ ] 4. Audio Clearance: Ensure the bedside microphone is unobstructed by 
       ventilator tubing or medical tape.
[ ] 5. Initial Baseline: Confirm telemetry displays "PATIENT CONSCIOUS & STABLE" 
       and EAR reads between 0.28 and 0.38.

3. STANDARD OPERATING PROTOCOLS
--------------------------------------------------------------------------------

3.1 ROUTINE MONITORING (BASELINE STATE)
- Status Display: Green dot pulsing, "PATIENT CONSCIOUS & STABLE", Triage: "NORMAL".
- Quadrants Display:
  - Quad 01: "Normal Breathing"
  - Quad 02: "Mouth Closed"
  - Quad 03: "Relaxed (0/10)"
  - Quad 04: "Head Centered"
- Action Required: No clinical intervention required. Continue routine rounds.

3.2 PROTOCOL: HYDRATION & BASIC CARE REQUEST (MOUTH OPEN)
- Trigger: Patient calmly parts lips or opens mouth (MAR > 0.26).
- System Response:
  - Quad 02 highlights cyan: "Mouth Open (Thirsty)".
  - A 3-tone bedside chime plays (NO SIREN).
  - AI Sentinel speaks: "I notice your mouth is open. Do you need water? Nod for Yes, shake for No."
- Nurse Action:
  1. Look at patient for gestural verification (Head Nod or Shake).
  2. If patient nods (Quad 04: "Nodding (Yes)"), provide oral swab, suction, or water.
  3. If patient shakes head (Quad 04: "Shaking Head (No)"), cancel request.

3.3 PROTOCOL: UNIVERSAL CHOKING & AIRWAY OBSTRUCTION (CATCHING NECK)
- Trigger: Patient catches neck with hand(s) and clutches throat tightly.
- System Response:
  - Quad 01 flashes red: "Catching Neck / Choking".
  - Code Blue Siren activates immediately (alternating 960 Hz / 620 Hz).
  - Screen strobes red/blue. Red "SILENCE ALARM" button appears in header.
  - AI Sentinel announces: "Emergency Code Blue! Patient is clutching their neck! Acute airway obstruction detected!"
- Clinical Nurse Action (STAT EMERGENCY):
  1. IMMEDIATELY verify tracheal airway patency.
  2. Perform emergency endotracheal / oral suction.
  3. Inspect for mucous plug, cuff deflation, or tube kinking.
  4. Once airway is secure, press "SILENCE ALARM" (or key 'S') to clear siren.

3.4 PROTOCOL: UNRESPONSIVENESS / SYNCOPE (EYES CLOSED > 2.5s)
- Trigger: Ocular ratio (EAR) < 0.20 continuously for > 2.5 seconds.
- System Response:
  - Quad 04 displays: "Eyes Closed (Unresponsive)".
  - Glasgow Coma Scale (GCS) telemetry drops from 15/15 to 3/15.
  - Emergency alarm sounds. AI announces loss of consciousness.
- Clinical Nurse Action:
  1. Attempt verbal and physical tactile stimulation (sternal rub / shoulder tap).
  2. Verify pulse and SpO2 plethysmograph waveform.
  3. Prepare emergency neurological and metabolic evaluation.

3.5 PROTOCOL: IMMOBILITY CRISIS / STATUE STATE (> 2.5s)
- Trigger: Zero facial or ocular movement detected (motion variance < 0.0016).
- System Response:
  - Quad 01 displays: "Statue / Motionless".
  - Emergency alarm engages. AI alerts bedside caregiver.
- Clinical Nurse Action:
  1. Differentiate catatonic stupor, tonic seizure, or sudden cardiac standstill.
  2. Check ECG cardiac leads and breathing rhythm immediately.

3.6 PROTOCOL: VESTIBULAR DIZZINESS (HEAD TILT)
- Trigger: Head roll tilt > 16° or rapid lateral swaying.
- System Response:
  - Quad 04 displays: "Dizzy / Head Tilted".
  - AI advises patient to lean back.
- Clinical Nurse Action:
  1. Elevate head of bed to 30° to stabilize orthostatic balance.
  2. Check blood pressure for orthostatic hypotension.

4. ALARM SILENCING & SYSTEM RECOVERY
--------------------------------------------------------------------------------
To silence an active emergency alarm:
Method A (Bedside Screen): Click the bright red "SILENCE ALARM" button in header.
Method B (Clinical Keyboard): Press the hotkey 'S'.
Post-Silencing Step: Confirm that telemetry resets to "PATIENT CONSCIOUS & STABLE".

5. SYSTEM FAIL-SAFES & CONTINGENCIES
--------------------------------------------------------------------------------
- Camera Loss: If video feed drops, telemetry alerts "CAMERA PERMISSION REQUIRED". 
  Staff must immediately rely on bedside hardware telemetry (ECG/SpO2 monitors).
- Ambient Noise: The Web Audio acoustic filter isolates room noise; groans > 55% 
  sustained for > 1.4s trigger attendant summon alerts.

================================================================================
END OF STANDARD OPERATING PROCEDURE — NEUROGUARD BEDSIDE SENTINEL
================================================================================