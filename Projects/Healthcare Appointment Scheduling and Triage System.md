Patient-Centric Multi-Modal Appointment Scheduling & Triage System

Streamlining real-time availability, insurance validation, and WCAG accessibility.

# 🏥 Patient-Centric Multi-Modal Appointment Scheduling & Triage System

An end-to-end UI/UX case study and product design system designed to simplify medical appointment booking, reduce patient drop-off, and decrease healthcare facility no-show rates through accessible, real-time interface design.

> **Product & UX Vision:**
> Focusing on real-time provider availability, insurance pre-validation, and reducing no-shows through intuitive UX and accessible design (WCAG). Having a strong grasp of technical delivery and business strategy gives you a massive advantage in product design. Adding formal UI/UX training closes the loop, allowing you to bridge the gap between business viability, technical feasibility, and human-centered design.

---

### 🎯 Key Design & Functional Objectives
* **Real-Time Availability & Triage:** Designing intuitive selection flows for in-person, video, and phone consultations based on urgency and provider schedules.
* **Streamlined Insurance Pre-Validation:** Creating clear, low-friction micro-interactions for capturing and verifying coverage upfront.
* **Accessible & Inclusive Interface (WCAG 2.1 AA):** Designing for high-contrast visibility, screen reader support, and simple touch targets across multi-generational patient demographics.
* **Automated Engagement & No-Show Reduction:** Constructing smart notification flows and seamless calendar sync interactions to improve attendance.

### 🛠 UI/UX Artifacts Included
1. **User Research & Personas:** Patient journey mapping and clinical friction-point analysis.
2. **Information Architecture:** User flows, sitemaps, and booking interaction logic.
3. **Wireframes & Interactive Prototypes:** Low-fidelity sketches to high-fidelity Figma components.
4. **Design System & Component Library:** Typography, color palettes, accessibility specs, and layout grids.
5. **Developer Handoff Specs:** Microservice API mapping, error-state guidelines, and technical handoff documentation.


# Screen 1: Smart Triage & Consultation Mode Selector

```text
+-------------------------------------------------------+
|  [< Back]               Book Appointment              |
+-------------------------------------------------------+
|                                                       |
|  STEP 1: Select Consultation Type                     |
|                                                       |
|  +-------------------------------------------------+  |
|  |  (o) 🏥 In-Person Visit                         |  |
|  |      Best for physical exams & urgent care      |  |
|  +-------------------------------------------------+  |
|  |  ( ) 💻 Video Consultation                      |  |
|  |      Fastest availability for follow-ups        |  |
|  +-------------------------------------------------+  |
|  |  ( ) 📞 Phone Consultation                      |  |
|  |      Quick doctor check-in                      |  |
|  +-------------------------------------------------+  |
|                                                       |
|  SYMPTOM CHECK & TRIAGE (Optional)                    |
|  Describe what you are experiencing:                  |
|  +-------------------------------------------------+  |
|  |  [ e.g., Headaches for 2 days, mild fever... ]  |  |
|  +-------------------------------------------------+  |
|  [!] Triage Priority: ROUTINE CARE                    |
|                                                       |
|  [ CANCEL ]                               [ NEXT > ]  |
+-------------------------------------------------------+

<br>

# Screen 2: Real-Time Availability & Insurance Validation

+-------------------------------------------------------+
|  [< Back]               Select Provider               |
+-------------------------------------------------------+
|                                                       |
|  STEP 2: Provider & Slot Selection                    |
|                                                       |
|  Dr. Sarah Jenkins, MD                                |
|  Cardiology • 4.9 ★ (120 reviews)                     |
|                                                       |
|  INSURANCE STATUS                                     |
|  +-------------------------------------------------+  |
|  |  [✓] UnitedHealthcare Choice Plus               |  |
|  |  Verified Real-Time • Est. Copay: $30.00         |  |
|  +-------------------------------------------------+  |
|                                                       |
|  AVAILABLE SLOTS (Earliest Available)                 |
|  +------------------+  +------------------+           |
|  |  Thu, Oct 12     |  |  Fri, Oct 13     |           |
|  |  [ 09:00 AM ]    |  |  [ 10:30 AM ]    |           |
|  |  [ 02:15 PM ]    |  |  [ 01:00 PM ]    |           |
|  +------------------+  +------------------+           |
|                                                       |
|  [ CANCEL ]                     [ CONFIRM BOOKING > ] |
+-------------------------------------------------------+



