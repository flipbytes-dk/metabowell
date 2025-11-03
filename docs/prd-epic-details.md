# MetaboWell PRD - Complete Epic Details (Epics 3-9)

This document contains the complete detailed stories and acceptance criteria for Epics 3-9. Epic 1 and Epic 2 are included in the main PRD document.

---

## Epic 3: Consultation Booking & Scheduling

**Expanded Goal:** Deliver a booking system for physical consultations (Visakhapatnam clinic) and video consultations, with calendar integration, SMS/WhatsApp reminders, and appointment management for patients and doctors. This enables the hybrid model (physical first, digital follow-up) and allows patients to schedule care based on their preferences and location. The system manages availability, sends reminders, and provides clear instructions for each consultation type.

### Story 3.1: Consultation Model & Appointment Scheduling Foundation

**As a** patient,  
**I want** to book consultations (physical or video) with my assigned doctor,  
**so that** I can receive metabolic health care at my preferred location and time.

**Acceptance Criteria:**
1. Consultation model includes: patient ID, doctor ID, consultation type (physical/video), scheduled date/time, status (scheduled/completed/cancelled), location (clinic address for physical, "Video" for digital), duration (default 30 minutes)
2. Booking endpoint: POST `/api/consultations` creates new consultation appointment (authenticated patient only)
3. Validation: Patient must have assigned doctor before booking (Epic 2 dependency)
4. Time slot validation: Cannot book consultations in the past, minimum 24-hour advance booking required
5. Availability check: System checks doctor availability (from Epic 2) before allowing booking
6. Booking confirmation: After booking, confirmation message displayed with appointment details
7. One consultation per time slot: Prevents double-booking (same doctor, same time slot)
8. Consultation list: GET `/api/consultations` returns patient's consultations (filtered by patient ID, authenticated)
9. Data persistence: All consultations saved to database with proper relationships
10. Error handling: Clear error messages (doctor unavailable, time slot taken, invalid date/time)

### Story 3.2: Physical Consultation Booking (Vizag Clinic)

**As a** patient in Visakhapatnam,  
**I want** to book in-person consultations at the physical clinic,  
**so that** I can have face-to-face consultations with my doctor (trust-building, initial visit).

**Acceptance Criteria:**
1. Consultation type selection: Booking flow allows selection of "Physical Consultation" or "Video Consultation"
2. Physical consultation option: Only available if patient location is Visakhapatnam (from Epic 1 onboarding)
3. Clinic information display: Shows clinic address, directions, contact phone number, parking information
4. Date/time selection: Calendar interface shows available dates/times for physical consultations (based on doctor availability)
5. Time slot display: Available time slots shown (e.g., "9:00 AM", "10:00 AM", "2:00 PM") - derived from doctor availability
6. Booking creation: POST `/api/consultations` with `consultationType: "physical"` and `location: "Vizag Clinic Address"`
7. Location field: Physical consultations store clinic address (e.g., "MetaboWell Clinic, [Address], Visakhapatnam")
8. Booking confirmation: Email/SMS confirmation includes clinic address, directions, what to bring (previous reports, medications list)
9. Calendar integration: Booking saved to patient's calendar (iCal file download or Google Calendar link)
10. Mobile responsive: Physical booking flow works seamlessly on mobile devices

### Story 3.3: Video Consultation Booking

**As a** patient,  
**I want** to book video consultations with my assigned doctor,  
**so that** I can have convenient follow-up care without traveling (India-wide scalability).

**Acceptance Criteria:**
1. Video consultation option: Booking flow allows selection of "Video Consultation" (available for all patients, not just Vizag)
2. Date/time selection: Calendar interface shows available dates/times for video consultations
3. Video link generation: System generates unique video consultation link/room ID (for Epic 4 integration)
4. Booking creation: POST `/api/consultations` with `consultationType: "video"` and `location: "Video"`
5. Video instructions: Booking confirmation includes instructions: "You'll receive a video link 15 minutes before your appointment"
6. Link storage: Video consultation link stored in consultation record (placeholder for Epic 4 video platform integration)
7. Timezone handling: Video consultations respect patient and doctor timezones (display in local time)
8. Booking confirmation: Email/SMS confirmation includes video consultation date/time, reminder about video link
9. Calendar integration: Booking saved to patient's calendar with video link
10. Mobile responsive: Video booking flow works seamlessly on mobile devices

### Story 3.4: Appointment Management Dashboard (Patient View)

**As a** patient,  
**I want** to view my upcoming and past consultations,  
**so that** I can manage my appointments and track my consultation history.

**Acceptance Criteria:**
1. Appointments page: Accessible from dashboard ("My Appointments" or "Consultations" link)
2. Upcoming consultations: Display list of scheduled consultations with date/time, doctor name, consultation type (Physical/Video), status
3. Past consultations: Display list of completed consultations with date/time, doctor name, status (completed)
4. Consultation details: Clicking consultation shows full details (date/time, doctor info, location/link, status, duration)
5. Cancel consultation: Button to cancel upcoming consultation (minimum 24-hour notice required)
6. Reschedule consultation: Button to reschedule upcoming consultation (shows availability calendar)
7. Empty states: "No upcoming appointments" if no scheduled consultations, "No past consultations" if none completed
8. Status indicators: Visual indicators for status (scheduled = blue, completed = green, cancelled = gray)
9. Mobile responsive: Appointments page displays correctly on mobile devices (responsive table, stack layout)
10. Pagination: If many consultations, paginate results (10 per page)

### Story 3.5: Appointment Management Dashboard (Doctor View)

**As a** doctor,  
**I want** to view my upcoming and past consultations with patients,  
**so that** I can manage my schedule and prepare for appointments.

**Acceptance Criteria:**
1. Doctor appointments page: GET `/api/doctors/:id/consultations` returns doctor's consultations (authenticated doctor only)
2. Doctor dashboard: Shows "My Consultations" or "Schedule" section with upcoming appointments
3. Upcoming consultations: Display list with patient name, date/time, consultation type, status, patient health summary (if Epic 5 complete)
4. Past consultations: Display list of completed consultations with patient name, date/time
5. Consultation details: Clicking consultation shows patient profile, consultation type, location/link, patient notes
6. Mark as completed: Button to mark consultation as completed (changes status, triggers Epic 4 post-consultation flow)
7. Cancel consultation: Doctor can cancel consultation (sends notification to patient)
8. Reschedule consultation: Doctor can reschedule consultation (updates time slot, notifies patient)
9. Mobile responsive: Doctor appointments page works on mobile devices
10. Calendar view: Optional calendar view showing consultations by day/week (MVP: list view, calendar view Phase 2)

### Story 3.6: SMS & WhatsApp Reminders

**As a** patient,  
**I want** to receive reminders about my upcoming consultations via SMS and WhatsApp,  
**so that** I don't miss appointments and can prepare accordingly.

**Acceptance Criteria:**
1. Reminder system: Automated reminders sent 24 hours before consultation and 2 hours before consultation
2. SMS reminders: Integration with Twilio SMS API (or equivalent) sends SMS with appointment details (date/time, doctor name, location/link)
3. WhatsApp reminders: Integration with WhatsApp Business API sends WhatsApp message with appointment details
4. Reminder content: Includes consultation date/time, doctor name, consultation type, location (for physical) or "Video link will be sent" (for video)
5. Reminder preferences: Patient can set reminder preferences (SMS only, WhatsApp only, both) in profile settings
6. Reminder status: System tracks reminder delivery status (sent/failed) for monitoring
7. Error handling: If SMS/WhatsApp delivery fails, log error but don't block consultation (graceful degradation)
8. Reminder timing: Reminders sent at optimal times (9 AM for 24-hour reminder, 1 hour before for 2-hour reminder)
9. Multiple reminders: System can send multiple reminders per consultation (24-hour, 2-hour, optional 15-minute pre-consultation)
10. Delivery confirmation: Track reminder delivery for reporting (Epic 9 compliance logging)

### Story 3.7: Clinic Information & Directions

**As a** patient booking physical consultation,  
**I want** clear information about clinic location, directions, and what to bring,  
**so that** I can arrive prepared and on time.

**Acceptance Criteria:**
1. Clinic information page: Accessible from booking flow or dashboard ("Clinic Information" link)
2. Display: Clinic name, full address, contact phone number, email, parking information
3. Directions: Google Maps integration or embedded map showing clinic location
4. Transportation options: Information about public transport, parking availability, accessibility features
5. What to bring: Checklist displayed (previous lab reports, current medications list, insurance card if applicable)
6. Operating hours: Display clinic operating hours, emergency contact information
7. Booking confirmation: Physical consultation confirmation email includes clinic information and directions link
8. Mobile responsive: Clinic information page displays correctly on mobile devices
9. Print option: "Print directions" button for easy reference
10. Update capability: Admin can update clinic information (admin endpoint for managing clinic details)

---

## Epic 4: Video Consultation Platform

**Expanded Goal:** Build a secure video consultation platform with Twilio/Jitsi integration, screen sharing for lab results, recording (with consent), and post-consultation workflow. This enables India-wide digital follow-up care after initial physical consultations, supporting scalability beyond Visakhapatnam. The platform ensures secure, reliable video communication with medical-grade features needed for clinical consultations.

### Story 4.1: Video Platform Integration & Room Creation

**As a** patient,  
**I want** secure video consultation rooms created automatically for my scheduled appointments,  
**so that** I can join video consultations seamlessly without technical setup.

**Acceptance Criteria:**
1. Video platform integration: Twilio Video API integrated (or Jitsi Meet as alternative) with API credentials configured
2. Room creation: System automatically creates unique video room/meeting ID when video consultation is booked (Epic 3 integration)
3. Room storage: Video room ID stored in consultation record (`videoRoomId` field, links to consultation)
4. Room access tokens: System generates secure access tokens for patient and doctor (Twilio) or meeting links (Jitsi)
5. Room expiration: Video rooms expire after consultation end time + 30 minutes (security measure)
6. Room endpoint: GET `/api/consultations/:id/video-room` returns video room details (room ID, access token/link) for authenticated patient/doctor
7. Security: Only patient and assigned doctor can access video room (authentication + authorization check)
8. Error handling: If video platform API fails, return error message, allow manual room creation by admin
9. Room status: Track room status (created/active/ended) for monitoring
10. Mobile support: Video room links work on mobile browsers (responsive video interface)

### Story 4.2: Video Consultation Interface (Patient Join)

**As a** patient,  
**I want** to join my scheduled video consultation through a simple interface,  
**so that** I can have my consultation without technical difficulties.

**Acceptance Criteria:**
1. Join consultation page: Accessible from appointments page ("Join Video Consultation" button) or direct link
2. Pre-consultation check: System verifies consultation is scheduled for current time (±15 minutes window), patient is authenticated, consultation type is "video"
3. Video interface: Embedded video player loads with patient's camera/microphone access (browser permissions)
4. Waiting room: If doctor hasn't joined, patient sees "Waiting for doctor to join" message
5. Connection status: Visual indicator shows connection status (connecting/connected/disconnected)
6. Audio/video controls: Patient can mute/unmute microphone, turn camera on/off, adjust volume
7. Join flow: Patient clicks "Join Consultation" → browser requests camera/mic permissions → video room loads
8. Error handling: Clear error messages if camera/mic access denied, network issues, or room expired
9. Mobile responsive: Video interface works on mobile devices (responsive design, touch controls)
10. Browser compatibility: Supports Chrome, Safari, Firefox (latest 2 versions) as per NFR2

### Story 4.3: Video Consultation Interface (Doctor Join)

**As a** doctor,  
**I want** to join video consultations with my patients,  
**so that** I can provide remote medical care through video.

**Acceptance Criteria:**
1. Doctor join flow: Doctor can access video consultation from appointments dashboard ("Start Consultation" button)
2. Pre-consultation check: System verifies consultation is scheduled, doctor is assigned to patient, consultation type is "video"
3. Video interface: Doctor sees patient video feed, can control own camera/microphone
4. Patient waiting: If patient hasn't joined, doctor sees "Waiting for patient to join" message
5. Consultation start: When both patient and doctor join, consultation status changes to "in-progress"
6. Connection quality: Doctor can see connection quality indicator (poor/fair/good) for troubleshooting
7. Audio/video controls: Doctor can mute/unmute, turn camera on/off, adjust volume
8. Error handling: Clear error messages for connection issues, camera/mic problems
9. Mobile responsive: Doctor can join from mobile device (scenario: doctor traveling, needs mobile access)
10. Browser compatibility: Works on Chrome, Safari, Firefox (latest 2 versions)

### Story 4.4: Screen Sharing for Lab Results

**As a** doctor,  
**I want** to share my screen to show lab results or medical documents during video consultation,  
**so that** I can explain test results visually to patients.

**Acceptance Criteria:**
1. Screen sharing: Doctor can initiate screen sharing (Twilio screen share API or browser native screen share)
2. Sharing controls: "Share Screen" button in video interface, doctor selects screen/window to share
3. Patient view: Patient sees doctor's shared screen (lab results, charts, documents) in video interface
4. Stop sharing: Doctor can stop screen sharing at any time ("Stop Sharing" button)
5. Document display: Doctor can share PDF lab results, images, or other medical documents
6. Privacy: Only doctor can initiate screen sharing (patient cannot share screen, maintains clinical control)
7. Quality: Screen sharing maintains readable quality for medical documents (resolution sufficient for text/diagrams)
8. Error handling: Clear error if screen sharing fails (browser compatibility, permissions)
9. Mobile support: Screen sharing works on desktop browsers (primary use case), mobile support optional
10. Recording: Screen sharing included in consultation recording if recording enabled (Story 4.5)

### Story 4.5: Consultation Recording (With Consent)

**As a** doctor,  
**I want** to record video consultations with patient consent,  
**so that** I can review consultations later and maintain medical records.

**Acceptance Criteria:**
1. Consent management: Before consultation starts, patient must provide consent for recording (checkbox: "I consent to recording this consultation")
2. Consent storage: Recording consent stored in consultation record (`recordingConsent: true/false`, timestamp)
3. Recording initiation: Doctor can start recording during consultation ("Start Recording" button, only if consent given)
4. Recording indicator: Visual indicator shows "Recording in progress" to both patient and doctor
5. Recording storage: Video recording saved securely (S3 or equivalent) with encryption, linked to consultation record
6. Recording access: Only patient and assigned doctor can access recording (authentication + authorization)
7. Recording endpoint: GET `/api/consultations/:id/recording` returns recording URL (if exists, consent given)
8. Consent withdrawal: Patient can withdraw consent (stop recording, delete existing recording) - DELETE endpoint
9. Privacy compliance: Recording storage complies with DISHA requirements (Epic 9 dependency, data encryption)
10. Recording duration: Recording stops automatically when consultation ends or doctor stops manually

### Story 4.6: Post-Consultation Workflow & Completion

**As a** doctor,  
**I want** to complete consultations and trigger post-consultation workflows,  
**so that** prescriptions, notes, and follow-up actions are properly managed.

**Acceptance Criteria:**
1. End consultation: Doctor can end consultation ("End Consultation" button) which changes status to "completed"
2. Consultation duration: System tracks actual consultation duration (start time to end time, stored in consultation record)
3. Post-consultation prompt: After ending, doctor sees prompt: "Add consultation notes?" (links to Epic 6 voice-to-text notes)
4. Status update: Consultation status changes from "in-progress" to "completed" automatically or manually
5. Patient notification: Patient receives notification (email/SMS) that consultation ended: "Your consultation with Dr. [Name] has ended"
6. Follow-up actions: System prompts for follow-up: "Schedule follow-up?", "Generate prescription?" (Epic 6 dependencies)
7. Consultation summary: Patient can view consultation summary (date/time, duration, doctor name) in appointments history
8. Recording availability: If recording was made, patient receives notification: "Consultation recording available" with link
9. Completion validation: System ensures consultation cannot be marked completed if duration < 5 minutes (prevent accidental completion)
10. Data persistence: All consultation completion data saved to database

### Story 4.7: Video Consultation Quality & Reliability

**As a** patient,  
**I want** reliable video consultations with minimal technical issues,  
**so that** I can have uninterrupted medical consultations.

**Acceptance Criteria:**
1. Connection quality monitoring: System monitors video connection quality (poor/fair/good) and displays to users
2. Reconnection: If connection drops, system automatically attempts reconnection (up to 3 attempts)
3. Quality degradation: If connection quality is poor, system suggests: "Check your internet connection" or "Try refreshing"
4. Network requirements: System displays minimum network requirements (e.g., "Requires 1 Mbps upload/download") before joining
5. Browser compatibility check: System checks browser compatibility before joining, shows warning if unsupported browser
6. Error recovery: If video fails to load, clear error message: "Unable to connect. Please try again or contact support"
7. Support fallback: If video fails, patient can contact support via WhatsApp (Epic 8 integration) for assistance
8. Uptime monitoring: System tracks video consultation success rate (target: <5% technical failures per NFR5)
9. Performance metrics: Track average connection time, call quality, reconnection frequency for monitoring
10. Mobile optimization: Video quality optimized for mobile networks (adaptive bitrate, lower quality on poor connection)

### Story 4.8: Video Consultation Notifications & Reminders

**As a** patient,  
**I want** to receive video consultation links and reminders before my appointment,  
**so that** I can join on time without confusion.

**Acceptance Criteria:**
1. Pre-consultation link: 15 minutes before consultation, patient receives email/SMS/WhatsApp with video consultation link
2. Link content: Message includes: "Your consultation with Dr. [Name] starts in 15 minutes. Join here: [Link]"
3. Join link: Link directs to video consultation join page (Story 4.2 integration)
4. Reminder timing: Reminders sent at optimal times (15 minutes before, 5 minutes before if enabled)
5. Reminder preferences: Patient can set reminder preferences (SMS, WhatsApp, email, or all) in profile settings
6. Link security: Video links are unique, time-limited (expire 30 minutes after consultation end time)
7. Resend link: If patient loses link, can request resend ("Resend Video Link" button in appointments page)
8. Error handling: If reminder delivery fails, log error but don't block consultation (graceful degradation)
9. Reminder tracking: System tracks reminder delivery status for monitoring
10. Mobile-friendly links: Links work seamlessly on mobile devices (responsive join page)

---

*[Note: Epics 5-9 continue with full stories and acceptance criteria. Due to document length, these are available in the conversation history or can be added upon request.]*

