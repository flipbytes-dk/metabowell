# MetaboWell Product Requirements Document (PRD)

**Document Version:** 1.0  
**Date:** November 2, 2025  
**Prepared By:** John (PM)  
**Status:** Draft for Review  
**Source:** Project Brief (docs/brief.md)

---

## Goals and Background Context

### Goals

- Acquire 1,000 users in Year 1 with blended CAC of ₹4,000
- Achieve ₹60L gross revenue in Year 1 (₹6,000 per user average)
- Maintain 7.5x LTV:CAC ratio (₹30,000 LTV ÷ ₹4,000 CAC)
- Achieve 71% gross margin (platform leverage model)
- Break even at 4,200 users (Year 2-3) with ₹1.5Cr seed funding
- Establish #1 metabolic health platform in Visakhapatnam (50%+ brand awareness by Month 12)
- Deliver 70%+ of patients losing 10%+ body weight within 6 months
- Achieve 50%+ NPS (Net Promoter Score) vs. general telemedicine 30-40
- Maintain <12% monthly churn rate (vs. industry 15-20%)
- Enable endocrinologist-led care continuity (assigned doctor throughout journey)

### Background Context

MetaboWell addresses fragmentation in Indian metabolic healthcare, where patients receive prescriptions but lack ongoing support, coordination, and community—especially critical for GLP-1 medications requiring long-term management, side effect monitoring, and lifestyle integration.

The platform combines in-person endocrinologist consultations in Visakhapatnam with digital follow-up care India-wide, creating India's first doctor-led metabolic health ecosystem. Unlike digital-only competitors (HealthifyRx) or transactional marketplaces (Practo, Apollo), MetaboWell provides assigned doctor relationships, integrated services (doctors + labs + pharmacy + dieticians), and community support—all coordinated through one platform. The timing is critical: GLP-1 medications (Ozempic approved Oct 2024, Mounjaro launched) are revolutionizing treatment, generic semaglutide arrives in 2026 (85-90% cost reduction), and there's a 24-36 month competitive window before well-funded players enter the metabolic health vertical.

### Change Log

| Date | Version | Description | Author |
|------|---------|-------------|--------|
| 2025-11-02 | 1.0 | Initial PRD creation from Project Brief | John (PM) |

---

## Requirements

### Functional Requirements

**FR1:** Patient Onboarding Flow - System shall provide a frictionless, conversational signup experience (not form-heavy) that collects minimal data initially and progressively gathers details as users engage, enabling users to reach value within 5 minutes or less.

**FR2:** Doctor Marketplace - System shall display browseable profiles of available endocrinologists including photos, RMP certification, specializations, experience, and availability, allowing patients to select their preferred doctor (initial launch: 5 endocrinologists).

**FR3:** Physical Consultation Booking - System shall enable patients to book in-person consultations at the Visakhapatnam clinic with calendar integration, SMS/WhatsApp reminders, and clinic address/directions.

**FR4:** Video Consultation Platform - System shall provide secure video calls for follow-up consultations (after initial physical visit) with recording capability (with consent) and screen sharing for lab results, enabling India-wide scalability.

**FR5:** Basic EHR (Electronic Health Records) - System shall maintain unified patient medical history including weight tracking, medication dosage, side effects, and lab results, accessible by all providers (doctors, dieticians) with role-based access and audit logs for DISHA compliance.

**FR6:** Patient Tracking Dashboard - System shall allow patients to log weight, blood sugar, blood pressure, medication adherence, and symptoms, displaying progress over time through charts/graphs.

**FR7:** Doctor Voice-to-Text Notes - System shall enable doctors to dictate clinical observations with auto-transcription (using Google Speech-to-Text API), allowing review/edit before saving to patient records, saving 10-15 minutes per patient.

**FR8:** WhatsApp Support Integration - System shall allow patients to text assigned doctors/nutritionists via WhatsApp Business API with guaranteed <2 hour response time, routing messages to assigned providers and tracking response times.

**FR9:** Digital Prescription System - System shall enable doctors to issue digital prescriptions (if regulations allow) or PDF prescriptions sent via WhatsApp, including prescription template, digital signature, and secure delivery.

**FR10:** Subscription Management - System shall manage recurring billing at ₹3,500/month (standard) or ₹6,000/month (with GLP-1), with payment gateway integration (Razorpay/Stripe), automatic renewals, and payment failure handling.

**FR11:** Transparent Pricing Page - System shall display clear pricing tiers, what's included, and no hidden costs, with comparison table (MetaboWell vs. competitors).

**FR12:** Educational Content Library - System shall provide blog articles and videos on GLP-1 safety, obesity as disease, PCOS management, and diabetes reversal, optimized for SEO and accessible through CMS.

**FR13:** Visual Onboarding Experience - System shall present relatable imagery (obese person walking), empowerment messaging ("Take control of your life"), and "Science-led healthcare" positioning on landing page, with doctor credentials display.

**FR14:** Doctor Credentials Display - System shall show RMP certification, experience, and specializations on doctor profiles, with credential verification and photo uploads.

**FR15:** Diagnostic Lab Partnership Integration - System shall integrate with 1-2 lab partners (Thyrocare, Dr. Lal PathLabs) for home blood test visits, order placement, results delivery, and automatic integration into EHR.

**FR16:** Free Metabolic Health Assessment - System shall enable booking of free 30-minute consultations (₹1,500 value) as lead generation, with landing page and booking system integration.

**FR17:** Compliance Infrastructure - System shall ensure DISHA (Digital Information Security in Healthcare Act) compliance with data encryption, audit logs, consent management frameworks, and Digital Personal Data Protection Act preparation.

**FR18:** Payment Gateway Integration - System shall integrate Razorpay or Stripe India for secure payment processing, including refund handling and invoice generation.

### Non-Functional Requirements

**NFR1:** Performance - System shall achieve page load times <3 seconds, video consultation latency <200ms, and 99.5% uptime availability.

**NFR2:** Platform Support - System shall support web-first (desktop + mobile responsive) for MVP, with browser support for Chrome, Safari, Firefox (latest 2 versions), Android 8+, iOS 12+ (for future mobile app).

**NFR3:** Security - System shall implement end-to-end encryption for patient data, role-based access control (RBAC) for providers, and audit logs for all data access per DISHA compliance requirements.

**NFR4:** Scalability - System shall support auto-scaling infrastructure (AWS or GCP) with CDN (CloudFront/Cloudflare) to handle growth from 200 users (Phase 1) to 1,000 users (Phase 2) to 5,000+ users (Phase 3).

**NFR5:** Video Platform Reliability - System shall achieve <5% technical failure rate for video consultations using Twilio Video or Jitsi Meet integration.

**NFR6:** WhatsApp Response Time - System shall guarantee <2 hour average response time for WhatsApp support queries with 95%+ satisfaction tracking.

**NFR7:** Voice-to-Text Accuracy - System shall achieve 90%+ accuracy for medical terminology using Google Speech-to-Text API with review/edit capability before saving.

**NFR8:** Payment Transaction Success - System shall achieve 100% transaction success rate (excluding user payment failures) with reliable payment gateway integration.

**NFR9:** Data Interoperability - System shall prepare for India Stack/ABDM integration for EHR interoperability (Phase 2+ consideration).

**NFR10:** Multi-language Support - System shall support English + Hindi for MVP (V1), with architecture allowing expansion to regional languages (Telugu) in Phase 2.

**NFR11:** Compliance Certifications - System shall prepare for ISO 27001 certification (Phase 2) while achieving DISHA compliance from MVP launch.

**NFR12:** Onboarding Completion Rate - System shall achieve 80%+ onboarding completion rate (frictionless signup validation).

---

## User Interface Design Goals

### Overall UX Vision

MetaboWell's UX centers on trust and relationship-building. The first 30 seconds are critical to overcome skepticism and shame barriers through relatable imagery, empowerment messaging, and visible medical credibility. The experience should feel like a partnership with a healthcare team, not a transactional app.

Design emphasizes:
- Trust through transparency: doctor credentials, clear pricing, visible medical expertise
- Accessibility: WhatsApp-native users, conversational onboarding, simple interactions
- Empowerment: progress visualization, educational content, community connection
- Professional yet warm: medical credibility balanced with human support

The visual style combines scientific authority with approachable warmth—avoiding clinical coldness or overly casual health apps.

### Key Interaction Paradigms

**Conversational Onboarding:** WhatsApp-style progressive disclosure where patients answer questions conversationally rather than filling long forms. Data collection happens progressively as users engage.

**Assigned Relationship Model:** UI emphasizes continuity—patients see "Your Doctor: Dr. [Name]" prominently, not a marketplace of random providers. The relationship is front and center.

**Just-in-Time Support:** WhatsApp integration accessible from any screen. Side effects or questions can be addressed immediately without complex navigation.

**Progress Visualization:** Weight, lab results, and health metrics displayed as clear charts/graphs showing improvement over time. Celebrating small wins builds motivation.

**Educational Content Integration:** Content woven into the journey contextually (e.g., GLP-1 safety articles when starting medication), not buried in a separate library.

**Hybrid Model Transparency:** UI clearly indicates whether a consultation is physical (Vizag clinic) or digital (video), with clear instructions for each.

### Core Screens and Views

1. **Landing Page** - Trust-building entry point with visual onboarding experience, doctor credentials, transparent pricing, and free assessment CTA
2. **Onboarding Flow** - Conversational multi-step wizard collecting minimal required data initially, progressive data collection
3. **Doctor Selection/Marketplace** - Browseable doctor profiles with photos, credentials, specializations, availability (initial: 5 endocrinologists)
4. **Consultation Booking** - Calendar interface for physical (Vizag) or video consultations, with reminders and instructions
5. **Patient Dashboard** - Central hub showing assigned doctor, upcoming appointments, tracking dashboard (weight, vitals, medications), recent lab results, quick access to WhatsApp support
6. **Tracking Dashboard** - Input forms and charts/graphs for weight, blood sugar, blood pressure, medication adherence, symptoms over time
7. **Video Consultation Room** - Secure video call interface with screen sharing for lab results, recording consent, and post-consultation notes
8. **EHR/Medical Records View** - Patient-facing view of medical history, prescriptions, lab results, doctor notes (read-only for patients, editable for providers)
9. **Educational Content Library** - Browseable articles and videos on GLP-1 safety, obesity as disease, PCOS management, diabetes reversal (SEO-optimized)
10. **Subscription Management** - Current plan, billing history, payment methods, upgrade/downgrade options, transparent pricing display
11. **Settings/Profile** - Personal information, notification preferences, consent management, account settings
12. **WhatsApp Support Interface** - In-app interface or direct WhatsApp Business API integration showing conversation history and response time guarantees

### Accessibility: WCAG AA

Target WCAG AA compliance to ensure accessibility for users with disabilities, support older devices common in Tier-2 cities, and meet healthcare accessibility standards. This includes keyboard navigation, screen reader support, color contrast, and clear labeling.

### Branding

**Visual Identity:**
- Science-led healthcare positioning: medical credibility balanced with approachable warmth
- Empowering imagery: relatable photos (e.g., person walking), not stock photos
- Color palette: professional healthcare colors (blues, greens) with warmth, avoiding clinical coldness
- Typography: clean, readable fonts prioritizing clarity over decoration

**Messaging Tone:**
- "Your metabolic health partner for life—not just an app, not just a consultation, but a relationship"
- Empowerment-focused: "Take control of your life"
- Trust-building: Visible credentials, transparent pricing, no hidden costs
- Supportive: Community and belonging, not isolation

### Target Device and Platforms: Web Responsive

MVP focuses on Web Responsive (desktop + mobile responsive) for fastest time-to-market and broadest reach. This supports both desktop users (Tier-1) and mobile-first users (Tier-2, WhatsApp-native). Mobile app (Flutter, Android first, iOS later) planned for Phase 2 (Months 7-18) after validating the web experience.

Browser support: Chrome, Safari, Firefox (latest 2 versions)  
Mobile: Android 8+, iOS 12+ (for future mobile app planning)

---

## Technical Assumptions

### Repository Structure: Monorepo

Use a monorepo for MVP to centralize code, simplify development coordination with outsourced teams, enable shared components (EHR, payment, video), and streamline deployment. The brief indicates outsourced MVP development, so a single repository reduces coordination overhead. Consider splitting into polyrepo if the team scales post-seed.

### Service Architecture

Start with a modular monolith, then split into microservices as needed.

**Initial Architecture (MVP):**
- Modular monolith with clear domain boundaries
- Services logically separated but deployed together
- Domain modules: User Service, Consultation Service, EHR Service, Payment Service, Content Service, Notification Service

**Post-MVP Evolution (Phase 2-3):**
- Split into microservices when scaling needs or team size demands it
- API gateway pattern for service orchestration
- Event-driven architecture for async operations (notifications, lab integrations)

### Testing Requirements

Unit + Integration testing (not full pyramid for MVP).

**MVP Testing Strategy:**
- Unit tests: Core business logic (EHR data validation, subscription calculations, prescription generation)
- Integration tests: API endpoints, database operations, payment gateway integration, video platform integration
- Manual testing: UI/UX flows, WhatsApp integration, complex user journeys
- No E2E automation for MVP (add in Phase 2)

### Additional Technical Assumptions

**Frontend:** React (web-first MVP) with TypeScript, Next.js recommended for SSR/SEO, Tailwind CSS or styled-components, React Hook Form for forms.

**Backend:** Node.js with Express (recommended for MVP speed) or Python Django/FastAPI (if team has Python expertise). Recommendation: Node.js for MVP.

**Database:** PostgreSQL (primary) for structured data, Redis for caching/sessions, MongoDB optional for unstructured data.

**Hosting:** AWS or GCP with healthcare compliance, auto-scaling, CDN (CloudFront/Cloudflare).

**Third-Party Integrations:**
- Video: Twilio Video (recommended) or Jitsi Meet
- WhatsApp: WhatsApp Business API
- Payment: Razorpay (India-focused) or Stripe India
- Voice-to-Text: Google Speech-to-Text API
- Email/SMS: SendGrid, Twilio SMS
- Lab: Lab APIs (Thyrocare, Dr. Lal PathLabs)

**Security:** TLS 1.3, AES-256 encryption, DISHA compliance, DPDP Act preparation, ISO 27001 preparation (Phase 2).

**DevOps:** GitHub Actions/GitLab CI, Docker, environment management (dev/staging/prod), automated deployments.

**Monitoring:** Sentry/DataDog, CloudWatch/StackDriver, uptime monitoring, Web Vitals tracking.

---

## Epic List

1. **Epic 1: Foundation & User Onboarding** - Establish project infrastructure and deliver frictionless patient onboarding flow
2. **Epic 2: Doctor Management & Marketplace** - Enable doctor onboarding, credential management, and browseable marketplace
3. **Epic 3: Consultation Booking & Scheduling** - Deliver booking system for physical and video consultations
4. **Epic 4: Video Consultation Platform** - Build secure video consultation platform with Twilio/Jitsi integration
5. **Epic 5: EHR & Patient Tracking** - Create unified EHR system with role-based access and patient tracking dashboard
6. **Epic 6: Prescriptions & Provider Tools** - Enable digital prescriptions and doctor voice-to-text notes
7. **Epic 7: Payment & Subscription Management** - Implement subscription billing and payment gateway integration
8. **Epic 8: Content & Support Integration** - Deliver educational content library, WhatsApp support, and lab integration
9. **Epic 9: Compliance & Security Hardening** - Complete DISHA compliance infrastructure and security hardening

---

## Epic Details

### Epic 1: Foundation & User Onboarding

**Expanded Goal:** Establish foundational infrastructure (project setup, Git, CI/CD, authentication, database schema) and deliver a frictionless patient onboarding flow with conversational signup. This enables users to register, complete initial profile setup, and access the platform, setting the foundation for all subsequent features. The onboarding flow collects minimal required data initially and progressively gathers details as users engage, achieving the "5 minutes to value" target and reducing drop-off rates.

#### Story 1.1: Project Foundation & Infrastructure Setup

**As a** development team,  
**I want** project infrastructure (repository, CI/CD, environment configuration, Docker setup) established,  
**so that** all subsequent development can proceed with proper version control, automated testing, and deployment pipelines.

**Acceptance Criteria:**
1. Git repository initialized with proper .gitignore (excluding node_modules, .env files, build artifacts)
2. CI/CD pipeline configured (GitHub Actions or GitLab CI) with automated testing on pull requests
3. Docker configuration files (Dockerfile, docker-compose.yml) for local development environment
4. Environment configuration management (.env.example template, separate dev/staging/prod configs)
5. Health check endpoint (`/health`) returns 200 OK with basic system status (verifies app is running)
6. Project documentation (README.md) includes setup instructions, tech stack overview, and development workflow
7. Code quality tools configured (ESLint, Prettier for TypeScript/JavaScript) or equivalent for chosen stack
8. Database connection established (PostgreSQL) with initial schema migration framework ready

#### Story 1.2: Authentication & User Management Foundation

**As a** patient,  
**I want** secure authentication (registration, login, password reset) and basic user profile management,  
**so that** I can create an account and securely access the platform with my personal information protected.

**Acceptance Criteria:**
1. User registration endpoint accepts email, password, basic profile data (name, phone number, age, gender)
2. Password hashing using bcrypt or equivalent secure algorithm (never store plaintext passwords)
3. JWT token generation for authenticated sessions with configurable expiration (default 24 hours)
4. Login endpoint validates credentials and returns JWT token
5. Password reset flow: "Forgot password" link sends reset email with secure token, allows password update
6. User profile retrieval endpoint (authenticated) returns current user's profile data
7. User profile update endpoint allows authenticated users to modify their profile information
8. Role-based access control foundation: User model includes role field (patient, doctor, admin) for future RBAC
9. Email verification flow: Registration sends verification email, account activation required before full access
10. Rate limiting on authentication endpoints (prevent brute force attacks)

#### Story 1.3: Conversational Onboarding Flow - Step 1 (Basic Registration)

**As a** new patient,  
**I want** a simple, conversational first step to create my account with minimal required information,  
**so that** I can start using the platform quickly without form fatigue.

**Acceptance Criteria:**
1. Landing page displays clear value proposition ("Your metabolic health partner for life") with visual onboarding elements (relatable imagery, empowerment messaging)
2. "Get Started" or "Book Free Assessment" CTA button prominently displayed
3. Onboarding Step 1: Collect only email and password (or phone number + OTP for Indian market preference)
4. Conversational UI: Questions presented one at a time (not long form), WhatsApp-style progressive disclosure
5. Visual feedback: Progress indicator shows "Step 1 of X" (total steps will expand in future stories)
6. Validation: Email format validation, password strength requirements (min 8 characters, complexity)
7. Success: After Step 1 completion, user account created, logged in, redirected to Step 2
8. Error handling: Clear error messages for validation failures (email already exists, weak password)
9. Mobile responsive: Onboarding flow works seamlessly on mobile devices (primary use case)

#### Story 1.4: Conversational Onboarding Flow - Step 2 (Health Profile Basics)

**As a** new patient,  
**I want** to provide basic health information (BMI, conditions, goals) conversationally,  
**so that** the platform can understand my needs and match me with appropriate care.

**Acceptance Criteria:**
1. Onboarding Step 2 automatically loads after Step 1 completion (no manual navigation needed)
2. Collect: Current weight, height (calculate BMI automatically), age, gender
3. Collect: Primary health concern (multi-select: Obesity, Type-2 Diabetes, PCOS, Metabolic disorders, Other)
4. Collect: Weight loss goal (target weight or "lose X kg") - optional field, can skip
5. Conversational format: Questions presented sequentially with clear, simple language
6. Skip option: Non-critical fields can be skipped with "Skip for now" option (progressive data collection)
7. Data validation: Weight/height numeric validation, reasonable ranges (e.g., weight 30-200 kg)
8. Save progress: All entered data saved to user profile, can return later to complete
9. Progress indicator: Shows "Step 2 of X" with visual progress bar
10. Success: After Step 2, data saved, user sees confirmation message, ready for Step 3

#### Story 1.5: Conversational Onboarding Flow - Step 3 (Location & Preferences)

**As a** new patient,  
**I want** to specify my location and consultation preferences,  
**so that** the platform can show me relevant doctors and consultation options (physical vs. digital).

**Acceptance Criteria:**
1. Onboarding Step 3 loads after Step 2 completion
2. Collect: Location (city selection dropdown: Visakhapatnam, Tier-1 cities, Other) or manual entry
3. Collect: Consultation preference (radio: "I prefer in-person consultations", "I prefer video consultations", "I'm open to both")
4. Collect: Preferred language (English, Hindi) - MVP scope, expandable to Telugu in Phase 2
5. Collect: How did you hear about us? (referral source: Doctor referral, Friend, Google, Social media, Other)
6. Conversational UI: Clear questions, simple choices (no complex forms)
7. Location-based logic: If Visakhapatnam selected, show physical consultation option prominently
8. Skip option: Non-critical preferences can be skipped
9. Data saved: All preferences stored in user profile
10. Completion: After Step 3, onboarding complete, user redirected to dashboard (or doctor selection if Epic 2 ready)

#### Story 1.6: Patient Dashboard Foundation

**As a** patient,  
**I want** a central dashboard showing my profile, upcoming appointments, and quick access to key features,  
**so that** I can easily navigate the platform and see my progress at a glance.

**Acceptance Criteria:**
1. Dashboard route `/dashboard` accessible to authenticated patients only (redirect to login if not authenticated)
2. Display: User's name and profile photo (if uploaded) prominently at top
3. Display: Assigned doctor section (shows "No doctor assigned yet" if Epic 2 not complete, placeholder for future)
4. Display: Upcoming appointments section (empty state: "No upcoming appointments" if Epic 3 not complete)
5. Display: Quick action buttons: "Book Consultation", "View Health Records", "Contact Support" (placeholders, link to future epics)
6. Display: Onboarding completion status (if incomplete, show "Complete your profile" CTA)
7. Navigation: Sidebar or top navigation with links to Dashboard, Profile, Settings (basic structure)
8. Mobile responsive: Dashboard layout adapts to mobile screens (stack layout, touch-friendly buttons)
9. Loading states: Show loading indicators while fetching data
10. Error handling: Graceful error messages if data fetch fails

#### Story 1.7: User Profile Management

**As a** patient,  
**I want** to view and edit my profile information,  
**so that** I can keep my information up to date and manage my account settings.

**Acceptance Criteria:**
1. Profile page accessible from dashboard navigation ("Profile" or "My Account" link)
2. Display: All user profile data (name, email, phone, age, gender, location, health profile from onboarding)
3. Edit capability: Editable fields have "Edit" button or inline editing
4. Update endpoint: Save changes to profile with validation (email format, phone number format)
5. Password change: Separate section for changing password (requires current password verification)
6. Profile photo: Upload profile photo functionality (image upload, validation, storage in S3 or equivalent)
7. Data persistence: All changes saved to database, success confirmation message displayed
8. Validation: Form validation prevents invalid data entry (e.g., invalid email, future birth date)
9. Security: Only authenticated user can view/edit their own profile (no access to other users' profiles)
10. Mobile responsive: Profile page works on mobile devices

---

### Epic 2: Doctor Management & Marketplace

**Expanded Goal:** Enable endocrinologist onboarding, credential management, and a browseable marketplace where patients can view doctor profiles with credentials, specializations, and availability. This supports the "doctor-led" differentiator and trust-building through visible medical expertise, differentiating MetaboWell from anonymous marketplace platforms. The system manages doctor profiles, verifies credentials (RMP certification), and displays them prominently so patients can make informed choices about their care provider.

#### Story 2.1: Doctor Model & Admin Management Interface

**As an** admin user,  
**I want** to create and manage doctor profiles in the system,  
**so that** doctors can be onboarded and their information stored securely for patient viewing.

**Acceptance Criteria:**
1. Doctor model/schema includes: name, email, phone, RMP registration number, specialization, years of experience, bio, profile photo, status (active/inactive)
2. Admin-only endpoint to create doctor profile (POST `/api/admin/doctors`) with all required fields
3. Admin-only endpoint to update doctor profile (PUT `/api/admin/doctors/:id`)
4. Admin-only endpoint to list all doctors (GET `/api/admin/doctors`) with filtering by status
5. Admin-only endpoint to activate/deactivate doctors (PATCH `/api/admin/doctors/:id/status`)
6. RMP registration number validation: Format validation and uniqueness check (no duplicate RMP numbers)
7. Profile photo upload: Admin can upload doctor photo (image validation, storage in S3 or equivalent)
8. Admin authentication: Only users with admin role can access admin endpoints (RBAC check)
9. Data persistence: All doctor data saved to database with proper relationships to user model
10. Error handling: Validation errors returned for invalid data (missing required fields, invalid RMP format)

#### Story 2.2: Doctor Credential Verification & Display

**As a** patient,  
**I want** to see verified doctor credentials (RMP certification, experience, specializations) prominently displayed,  
**so that** I can trust the medical expertise of the doctors on the platform.

**Acceptance Criteria:**
1. Doctor profile page displays: Doctor name, profile photo, RMP registration number (formatted display)
2. Credentials section shows: Years of experience, specializations (formatted list), RMP certification badge/icon
3. Credential verification status: Display "Verified" badge if RMP number validated (visual trust indicator)
4. Bio section: Doctor's professional bio/background displayed (formatted text)
5. Public endpoint: GET `/api/doctors/:id` returns doctor profile (no authentication required for viewing)
6. Credential formatting: RMP number displayed in readable format (e.g., "RMP-12345/AP/2020")
7. Specialization display: Specializations shown as tags or badges (e.g., "Endocrinology", "Diabetes Management", "PCOS")
8. Mobile responsive: Doctor profile page displays correctly on mobile devices
9. Loading states: Show loading indicator while fetching doctor data
10. Error handling: Graceful 404 page if doctor not found

#### Story 2.3: Doctor Marketplace - Browse & Search

**As a** patient,  
**I want** to browse available doctors with filters and search functionality,  
**so that** I can find the right doctor for my metabolic health needs.

**Acceptance Criteria:**
1. Doctor marketplace page accessible from dashboard ("Find a Doctor" or "Browse Doctors" link)
2. Display: Grid or list view of all active doctors with profile photos, names, specializations
3. Search functionality: Search bar allows filtering by doctor name or specialization
4. Filter options: Filter by specialization (Endocrinology, Diabetes, PCOS, Obesity Management), years of experience (dropdown ranges)
5. Sort options: Sort by experience (most experienced first), alphabetical (A-Z), or recently added
6. Doctor cards: Each doctor card shows thumbnail photo, name, specializations, years of experience, "View Profile" button
7. Pagination: If more than 12 doctors, paginate results (12 per page) or infinite scroll
8. Empty states: "No doctors found" message if search/filter returns no results
9. Public endpoint: GET `/api/doctors` returns list of active doctors with pagination, search, filter support
10. Mobile responsive: Marketplace displays in mobile-friendly grid (2 columns) or list layout

#### Story 2.4: Doctor Availability Management

**As a** doctor,  
**I want** to set my availability schedule (working hours, days),  
**so that** patients can see when I'm available for consultations.

**Acceptance Criteria:**
1. Doctor availability model: Stores working days (Monday-Sunday), time slots (e.g., 9 AM - 5 PM), timezone
2. Doctor endpoint: PUT `/api/doctors/:id/availability` allows doctors to update their availability (authenticated, own profile only)
3. Availability display: Doctor profile page shows "Available for consultations" with general availability info
4. Time slot management: Doctors can set weekly schedule (which days, which hours) - MVP: simple weekly pattern
5. Timezone handling: Availability stored with timezone (default: IST), display adjusted for user location
6. Availability status: Display "Available Now" if current time falls within doctor's working hours
7. Future enhancement placeholder: Availability can be expanded to specific time slots in Epic 3 (consultation booking)
8. Admin override: Admin can set/modify doctor availability if needed
9. Data validation: Time slots validated (start time < end time, no overlapping ranges)
10. Mobile responsive: Availability display works on mobile devices

#### Story 2.5: Doctor Selection & Assignment

**As a** patient,  
**I want** to select a doctor from the marketplace and have them assigned as my primary doctor,  
**so that** I can establish a continuous care relationship.

**Acceptance Criteria:**
1. Doctor selection: On doctor profile page, "Select This Doctor" or "Book Consultation" button prominently displayed
2. Selection endpoint: POST `/api/patients/:id/assign-doctor` assigns doctor to patient (authenticated patient only)
3. One doctor assignment: Patient can only have one assigned doctor at a time (reassigning updates assignment)
4. Assignment confirmation: After selection, confirmation message displayed ("Dr. [Name] is now your assigned doctor")
5. Dashboard update: Patient dashboard shows assigned doctor name and photo immediately after selection
6. Doctor relationship: Patient model includes `assignedDoctorId` foreign key linking to doctor
7. Unassignment: Patient can unassign doctor (via settings or selecting new doctor) - endpoint POST `/api/patients/:id/unassign-doctor`
8. Assignment history: System tracks assignment changes (audit log for Epic 9 compliance)
9. Validation: Cannot assign inactive doctors, error message if doctor unavailable
10. Mobile responsive: Doctor selection flow works seamlessly on mobile

#### Story 2.6: Doctor Reviews & Ratings (Post-Launch Foundation)

**As a** patient,  
**I want** to see patient reviews and ratings for doctors (after consultations),  
**so that** I can make informed decisions based on other patients' experiences.

**Acceptance Criteria:**
1. Review model: Stores rating (1-5 stars), review text, patient ID, doctor ID, consultation ID, timestamp
2. Review endpoint: POST `/api/reviews` allows authenticated patients to submit reviews (only after completed consultation - Epic 4 dependency)
3. Review display: Doctor profile page shows average rating (e.g., "4.5 stars") and review count
4. Review list: Doctor profile page displays recent reviews (last 5) with patient names anonymized (e.g., "Patient P.") or initials
5. Review validation: Patient can only review doctors they've consulted with (Epic 4 integration)
6. One review per consultation: Patient can submit one review per completed consultation (prevent duplicates)
7. Review moderation: Admin can flag/hide inappropriate reviews (admin endpoint for moderation)
8. Empty state: If no reviews, show "No reviews yet" message
9. Public endpoint: GET `/api/doctors/:id/reviews` returns reviews for doctor (no authentication required)
10. Mobile responsive: Reviews display correctly on mobile devices

**Note:** Review submission requires Epic 4 (consultations) to be complete. This story establishes the foundation, but full functionality depends on consultation completion flow.

---

### Epic 3: Consultation Booking & Scheduling

**Expanded Goal:** Deliver a booking system for physical consultations (Visakhapatnam clinic) and video consultations, with calendar integration, SMS/WhatsApp reminders, and appointment management for patients and doctors. This enables the hybrid model (physical first, digital follow-up) and allows patients to schedule care based on their preferences and location. The system manages availability, sends reminders, and provides clear instructions for each consultation type.

#### Story 3.1: Consultation Model & Appointment Scheduling Foundation

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

#### Story 3.2: Physical Consultation Booking (Vizag Clinic)

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

#### Story 3.3: Video Consultation Booking

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

#### Story 3.4: Appointment Management Dashboard (Patient View)

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

#### Story 3.5: Appointment Management Dashboard (Doctor View)

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

#### Story 3.6: SMS & WhatsApp Reminders

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

#### Story 3.7: Clinic Information & Directions

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

### Epic 4: Video Consultation Platform

**Expanded Goal:** Build a secure video consultation platform with Twilio/Jitsi integration, screen sharing for lab results, recording (with consent), and post-consultation workflow. This enables India-wide digital follow-up care after initial physical consultations, supporting scalability beyond Visakhapatnam. The platform ensures secure, reliable video communication with medical-grade features needed for clinical consultations.

#### Story 4.1: Video Platform Integration & Room Creation

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

#### Story 4.2: Video Consultation Interface (Patient Join)

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

#### Story 4.3: Video Consultation Interface (Doctor Join)

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

#### Story 4.4: Screen Sharing for Lab Results

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

#### Story 4.5: Consultation Recording (With Consent)

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

#### Story 4.6: Post-Consultation Workflow & Completion

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

#### Story 4.7: Video Consultation Quality & Reliability

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

#### Story 4.8: Video Consultation Notifications & Reminders

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

### Epic 5: EHR & Patient Tracking

**Expanded Goal:** Create a unified Electronic Health Records system with role-based access, patient tracking dashboard for logging vitals/medications/symptoms, progress visualization, and medical history management. This enables continuity of care—all providers (doctors, dieticians) access the same unified record, eliminating "explain your problem again" friction. The system provides data-driven care through progress tracking and pattern recognition, helping doctors make informed decisions and patients see their improvement over time.

#### Story 5.1: EHR Data Model & Core Infrastructure

**As a** developer,  
**I want** a comprehensive EHR data model and core infrastructure established,  
**so that** all medical data can be stored securely with proper relationships and access controls.

**Acceptance Criteria:**
1. EHR core models: Patient profile (extended from Epic 1), medical history, lab results, prescriptions, vitals, medications, consultation notes
2. Database schema: PostgreSQL tables with proper relationships (patient → consultations → notes → prescriptions → vitals)
3. Data encryption: All sensitive medical data encrypted at rest (AES-256) and in transit (TLS 1.3) per DISHA requirements
4. Audit logging: All EHR access logged (who accessed, when, what data viewed) for DISHA compliance
5. Role-based access: Foundation for RBAC (patient can view own records, doctor can view assigned patients, admin can view all)
6. Data retention: Policy for data retention (minimum 7 years per Indian medical records regulations)
7. Backup strategy: Automated daily backups of EHR data with 30-day retention
8. Data migration: Framework for migrating existing patient data (if any) into EHR system
9. Indexing: Database indexes on critical fields (patient ID, consultation ID, date) for query performance
10. Validation: Data validation rules (e.g., weight must be positive number, dates cannot be future)

#### Story 5.2: Patient Medical History Management

**As a** doctor,  
**I want** to view and update patient medical history (conditions, medications, allergies, family history),  
**so that** I can provide informed care based on complete patient context.

**Acceptance Criteria:**
1. Medical history model: Stores conditions (diabetes, PCOS, hypertension), current medications, allergies, family history, surgical history
2. Doctor endpoint: GET `/api/patients/:id/medical-history` returns patient medical history (authenticated doctor, assigned patients only)
3. Doctor update: PUT `/api/patients/:id/medical-history` allows doctor to update medical history (authenticated, assigned patients only)
4. Patient view: Patient can view own medical history (read-only) from dashboard ("My Medical History" section)
5. History display: Medical history displayed in organized sections (Current Conditions, Medications, Allergies, Family History)
6. Update tracking: System tracks who updated medical history and when (audit log)
7. Data validation: Validates medical data (e.g., medication names, condition codes using standard medical terminology)
8. History timeline: Medical history changes displayed chronologically (shows when conditions added/removed)
9. Export capability: Patient can export medical history as PDF (for sharing with other doctors)
10. Mobile responsive: Medical history page displays correctly on mobile devices

#### Story 5.3: Patient Vitals Logging (Weight, Blood Sugar, Blood Pressure)

**As a** patient,  
**I want** to log my daily vitals (weight, blood sugar, blood pressure) easily,  
**so that** I can track my progress and doctors can see patterns in my health data.

**Acceptance Criteria:**
1. Vitals logging: Patient can log weight, blood sugar (fasting/post-meal), blood pressure (systolic/diastolic), date/time
2. Logging interface: Simple form on dashboard ("Log Vitals" button) with input fields for each vital
3. Logging endpoint: POST `/api/patients/:id/vitals` saves vitals data (authenticated patient, own data only)
4. Data validation: Validates vitals ranges (weight: 30-200 kg, blood sugar: 50-500 mg/dL, blood pressure: reasonable ranges)
5. Date/time: Vitals stored with timestamp (patient can log historical data if needed)
6. Quick logging: Mobile-friendly quick entry form (takes <30 seconds to log)
7. Multiple entries: Patient can log multiple vitals per day (e.g., morning weight, evening blood sugar)
8. Data persistence: All vitals saved to database with patient ID, timestamp, source (patient-entered)
9. Doctor access: Doctor can view patient vitals in EHR (assigned patients only, Epic 5.6)
10. Empty state: If no vitals logged, show "Start tracking your vitals" prompt with logging form

#### Story 5.4: Progress Visualization Dashboard

**As a** patient,  
**I want** to see charts and graphs showing my health progress over time,  
**so that** I can visualize improvements and stay motivated.

**Acceptance Criteria:**
1. Progress dashboard: Patient dashboard includes "My Progress" section with charts/graphs
2. Weight chart: Line graph showing weight over time (days/weeks/months), with goal weight line if set
3. Blood sugar chart: Line graph showing blood sugar readings over time (different colors for fasting/post-meal)
4. Blood pressure chart: Line graph showing systolic/diastolic over time
5. Time range selector: Patient can view progress for different periods (Last 7 days, Last 30 days, Last 3 months, All time)
6. Chart library: Uses charting library (Chart.js, Recharts, or equivalent) for responsive, interactive charts
7. Trend indicators: Shows trend arrows (↑ improving, ↓ declining, → stable) for quick visual feedback
8. Goal visualization: If patient has weight loss goal, chart shows progress toward goal (percentage, remaining kg)
9. Data points: Charts show individual data points (hover to see exact values, date)
10. Mobile responsive: Charts display correctly on mobile devices (responsive chart sizing, touch-friendly interactions)
11. Export: Patient can export progress charts as image/PDF for sharing with family or other doctors
12. Empty state: If insufficient data (<3 data points), show "Log more vitals to see your progress" message

#### Story 5.5: Medication Tracking & Adherence

**As a** patient,  
**I want** to log my medications and track adherence,  
**so that** I can ensure I'm taking medications correctly and doctors can monitor compliance.

**Acceptance Criteria:**
1. Medication list: Patient can view current medications (name, dosage, frequency, start date) from dashboard
2. Medication logging: Patient can add medications (prescribed by doctor or self-reported)
3. Adherence tracking: Patient can mark medications as "Taken" or "Missed" for each day
4. Medication endpoint: POST `/api/patients/:id/medications` saves medication data (authenticated patient)
5. Adherence endpoint: POST `/api/patients/:id/medications/:id/adherence` logs daily adherence (taken/missed, date)
6. Adherence display: Calendar view or list showing medication adherence (green = taken, red = missed)
7. Adherence rate: Dashboard shows "Medication Adherence: X%" (calculated from logged data)
8. Reminders: System can send medication reminders (Epic 8 integration, optional for MVP)
9. Doctor access: Doctor can view patient medication list and adherence in EHR (assigned patients only)
10. Data validation: Validates medication data (dosage format, frequency, dates)
11. Medication history: Shows when medications started/stopped (timeline view)
12. Mobile responsive: Medication tracking works seamlessly on mobile devices

#### Story 5.6: Doctor EHR Access & Patient Overview

**As a** doctor,  
**I want** to access comprehensive patient EHR data (medical history, vitals, medications, consultations) in one view,  
**so that** I can make informed medical decisions without asking patients to repeat information.

**Acceptance Criteria:**
1. Patient overview page: Doctor can access patient overview from appointments dashboard ("View Patient Profile")
2. Unified view: Displays patient medical history, vitals trends, current medications, consultation history, lab results (if Epic 8 complete)
3. EHR endpoint: GET `/api/doctors/:id/patients/:patientId/ehr` returns comprehensive EHR data (authenticated doctor, assigned patients only)
4. Access control: Only assigned doctor can access patient EHR (authorization check prevents unauthorized access)
5. Data sections: EHR organized in tabs/sections: Overview, Medical History, Vitals, Medications, Consultations, Lab Results
6. Quick summary: Overview tab shows key metrics (current weight, latest blood sugar, medication adherence %, last consultation date)
7. Vitals trends: Doctor sees vitals charts (same as patient view, Story 5.4) with annotations if needed
8. Consultation history: Doctor sees list of past consultations with dates, consultation notes (if Epic 6 complete)
9. Recent changes: Highlights recent changes (e.g., "Patient logged weight: 2 days ago", "New medication added: 1 week ago")
10. Mobile responsive: Doctor EHR view works on mobile devices (responsive layout, touch-friendly)
11. Export: Doctor can export patient EHR summary as PDF (for medical records, referrals)
12. Audit logging: All EHR access logged (doctor ID, patient ID, timestamp, data viewed) for DISHA compliance

#### Story 5.7: Lab Results Integration & Display

**As a** patient,  
**I want** to view my lab results (blood tests, diagnostic reports) in my EHR,  
**so that** I can track diagnostic metrics and share results with doctors.

**Acceptance Criteria:**
1. Lab results model: Stores lab test name, date, results (key-value pairs: e.g., HbA1c: 7.2%), reference ranges, lab name
2. Lab results upload: Patient can upload lab result PDF/image (file upload, stored in S3)
3. Lab results endpoint: POST `/api/patients/:id/lab-results` saves lab results (authenticated patient, file upload + metadata)
4. Lab results display: Patient dashboard shows "Lab Results" section with list of recent tests
5. Results detail: Clicking lab result shows full details (test name, date, values, reference ranges, interpretation)
6. Results visualization: Key metrics (HbA1c, cholesterol, etc.) displayed as charts over time (if multiple tests)
7. Doctor access: Doctor can view patient lab results in EHR (assigned patients only, Story 5.6 integration)
8. Lab integration: If Epic 8 lab partnership complete, lab results automatically imported (API integration)
9. Results comparison: System can compare current results to previous results (shows improvement/decline)
10. Data validation: Validates lab result data (date cannot be future, values within reasonable ranges)
11. Mobile responsive: Lab results display correctly on mobile devices
12. Export: Patient can export lab results as PDF (for sharing with other doctors)

**Note:** Full lab integration (automatic import from lab partners) depends on Epic 8. This story establishes manual upload and display; automatic import can be added later.

#### Story 5.8: Symptom Logging & Tracking

**As a** patient,  
**I want** to log symptoms (nausea, fatigue, side effects) easily,  
**so that** doctors can monitor side effects and adjust treatment accordingly.

**Acceptance Criteria:**
1. Symptom logging: Patient can log symptoms (nausea, constipation, fatigue, headaches, etc.) with severity (1-10 scale) and date/time
2. Logging interface: Simple form on dashboard ("Log Symptom" button) with symptom dropdown/autocomplete and severity slider
3. Symptom endpoint: POST `/api/patients/:id/symptoms` saves symptom data (authenticated patient)
4. Symptom list: Patient dashboard shows "My Symptoms" section with recent symptoms (last 7 days)
5. Symptom trends: Shows symptom frequency over time (e.g., "Nausea: 3 times this week")
6. Doctor access: Doctor can view patient symptoms in EHR (assigned patients only, helps identify side effects)
7. Symptom alerts: If severe symptoms logged (severity 8+), system can flag for doctor review (Epic 8 notification)
8. Symptom history: Patient can view symptom history (calendar view or list) showing patterns
9. Data validation: Validates symptom data (severity 1-10, date cannot be future)
10. Mobile responsive: Symptom logging works seamlessly on mobile devices
11. Quick logging: Pre-filled common symptoms (GLP-1 side effects: nausea, constipation, fatigue) for quick entry
12. Symptom patterns: System can identify patterns (e.g., "Nausea more common after medication increase")

#### Story 5.9: EHR Data Export & Portability

**As a** patient,  
**I want** to export my complete EHR data,  
**so that** I can share it with other doctors or maintain backup copies.

**Acceptance Criteria:**
1. Export endpoint: GET `/api/patients/:id/ehr/export` generates complete EHR export (authenticated patient, own data only)
2. Export format: Exports as PDF document or JSON file (patient choice)
3. Export content: Includes medical history, vitals (last 2 years), medications, consultation history, lab results, symptoms
4. Data formatting: PDF export formatted as readable medical report (sections, tables, charts)
5. Export security: Export link is time-limited (expires in 24 hours), requires authentication
6. Export tracking: System logs when patient exports EHR (audit log for compliance)
7. Data portability: Patient can request complete data deletion (GDPR/DPDP Act compliance, Epic 9)
8. Export download: Patient can download export file directly or receive via email
9. Partial export: Patient can select specific data types to export (e.g., only lab results, only vitals)
10. Mobile support: Export functionality works on mobile devices (download or email delivery)

---

### Epic 6: Prescriptions & Provider Tools

**Expanded Goal:** Enable digital prescription generation, doctor voice-to-text notes for clinical observations, and provider workflow tools to improve efficiency and reduce administrative burden. This addresses a major pain point for doctors—spending 10-15 minutes per patient on documentation—by enabling voice-to-text transcription. The prescription system provides convenience for patients (digital prescriptions via WhatsApp) while supporting regulatory compliance. Provider tools streamline workflows so doctors can focus on patient care rather than administrative tasks.

#### Story 6.1: Digital Prescription Model & Generation

**As a** doctor,  
**I want** to generate digital prescriptions for my patients,  
**so that** I can prescribe medications electronically and patients receive prescriptions conveniently.

**Acceptance Criteria:**
1. Prescription model: Stores patient ID, doctor ID, consultation ID, medications (name, dosage, frequency, duration), instructions, date, digital signature
2. Prescription generation: Doctor can create prescription during or after consultation (POST `/api/prescriptions`, authenticated doctor, assigned patients only)
3. Medication entry: Doctor can add multiple medications to prescription (name, dosage, frequency, duration, instructions)
4. Prescription template: System generates formatted prescription (PDF or HTML) with doctor details, patient details, medications, instructions, date
5. Digital signature: Doctor's digital signature included on prescription (stored signature or system-generated)
6. Prescription storage: Prescriptions saved to database and linked to consultation record
7. Regulatory compliance: Prescription format complies with Indian medical prescription regulations (if applicable)
8. Prescription endpoint: GET `/api/prescriptions/:id` returns prescription (authenticated patient/doctor, authorization check)
9. Prescription list: Patient can view all prescriptions from dashboard ("My Prescriptions" section)
10. Data validation: Validates prescription data (medication names, dosages, dates)

#### Story 6.2: Prescription Delivery via WhatsApp/Email

**As a** patient,  
**I want** to receive my prescription via WhatsApp or email immediately after consultation,  
**so that** I can access it conveniently without needing to collect paper prescriptions.

**Acceptance Criteria:**
1. Prescription delivery: After prescription generation, system automatically sends prescription to patient via WhatsApp and email
2. WhatsApp delivery: Integration with WhatsApp Business API sends prescription PDF or link to patient's WhatsApp number
3. Email delivery: Prescription PDF attached to email sent to patient's registered email address
4. Delivery content: Message includes: "Your prescription from Dr. [Name] is ready. Download here: [Link]" or PDF attachment
5. Delivery tracking: System tracks prescription delivery status (sent/failed) for monitoring
6. Delivery preferences: Patient can set delivery preferences (WhatsApp only, email only, or both) in profile settings
7. Resend prescription: Patient can request resend if not received ("Resend Prescription" button in prescriptions page)
8. Prescription link: Prescription link is secure, time-limited (expires in 30 days), requires authentication
9. Error handling: If delivery fails, log error, allow manual resend by doctor
10. Mobile-friendly: Prescription PDF is mobile-readable (responsive PDF format, clear text)

#### Story 6.3: Prescription Display & Download

**As a** patient,  
**I want** to view and download my prescriptions,  
**so that** I can access them anytime and share with pharmacies.

**Acceptance Criteria:**
1. Prescription list: Patient dashboard shows "My Prescriptions" section with list of all prescriptions (date, doctor name, medications summary)
2. Prescription detail: Clicking prescription shows full prescription details (doctor info, patient info, medications, instructions, date)
3. Prescription display: Prescription displayed in readable format (formatted text, clear medication list)
4. Download PDF: Patient can download prescription as PDF ("Download PDF" button)
5. Print prescription: Patient can print prescription directly ("Print" button, browser print dialog)
6. Prescription endpoint: GET `/api/prescriptions/:id` returns prescription data (authenticated patient, own prescriptions only)
7. Prescription history: Patient can view prescription history (all prescriptions, sorted by date, newest first)
8. Prescription search: Patient can search prescriptions by medication name or date
9. Mobile responsive: Prescription display works correctly on mobile devices (readable format, download/print options)
10. Pharmacy sharing: Patient can share prescription with pharmacy (via WhatsApp or email, "Share with Pharmacy" button)

#### Story 6.4: Voice-to-Text Notes Foundation & Integration

**As a** doctor,  
**I want** voice-to-text transcription capability integrated into the platform,  
**so that** I can dictate clinical notes instead of typing them manually.

**Acceptance Criteria:**
1. Voice-to-text integration: Google Speech-to-Text API integrated with API credentials configured
2. Audio capture: Doctor can record audio (microphone access) during or after consultation ("Start Recording" button)
3. Transcription endpoint: POST `/api/consultations/:id/transcribe` accepts audio file, returns transcribed text
4. Transcription accuracy: System achieves 90%+ accuracy for medical terminology (NFR7 requirement)
5. Language support: Transcription supports English (MVP), Hindi (Phase 2 expansion)
6. Audio format: Accepts common audio formats (WAV, MP3, M4A) for maximum compatibility
7. Transcription storage: Transcribed text stored in consultation notes (linked to consultation record)
8. Error handling: If transcription fails, clear error message, allow manual text entry fallback
9. Transcription review: Doctor can review transcribed text before saving (edit, correct errors)
10. Mobile support: Voice recording works on mobile devices (browser microphone access or mobile app)

#### Story 6.5: Doctor Voice-to-Text Notes Workflow

**As a** doctor,  
**I want** to dictate consultation notes using voice-to-text, review, and save them to patient records,  
**so that** I can save 10-15 minutes per patient on documentation.

**Acceptance Criteria:**
1. Notes interface: Doctor sees "Add Consultation Notes" prompt after consultation ends (Epic 4 integration)
2. Voice recording: Doctor clicks "Record Notes" button, speaks consultation observations, clicks "Stop Recording"
3. Auto-transcription: System automatically transcribes audio to text using Google Speech-to-Text API (Story 6.4)
4. Transcription display: Transcribed text displayed in text editor for doctor review
5. Edit capability: Doctor can edit transcribed text (correct errors, add details, format text)
6. Medical terminology: System handles medical terminology correctly (proper capitalization, spelling)
7. Notes saving: Doctor clicks "Save Notes" to save to consultation record (POST `/api/consultations/:id/notes`)
8. Notes storage: Consultation notes stored in database, linked to consultation, accessible in EHR (Epic 5)
9. Notes format: Notes formatted with timestamp, doctor name, structured content (chief complaint, examination, plan)
10. Time savings: Voice-to-text reduces note-taking time from 10-15 minutes to 2-3 minutes (validation through user testing)

#### Story 6.6: Consultation Notes Management & Display

**As a** doctor,  
**I want** to view and manage consultation notes for all my patients,  
**so that** I can review previous consultations and maintain continuity of care.

**Acceptance Criteria:**
1. Notes list: Doctor dashboard shows "Consultation Notes" section with list of notes (patient name, date, preview)
2. Notes detail: Clicking note shows full consultation notes (transcribed text, formatted display)
3. Notes editing: Doctor can edit notes after saving (PUT `/api/consultations/:id/notes`, authenticated doctor, own notes only)
4. Notes search: Doctor can search notes by patient name, date, or keywords (full-text search)
5. Notes export: Doctor can export notes as PDF or text file (for medical records, referrals)
6. Notes access: Only assigned doctor can view/edit patient notes (authorization check)
7. Notes history: System maintains notes history (shows edits, timestamps, who edited)
8. Patient access: Patient can view consultation notes (read-only) from dashboard ("Consultation History" section)
9. Notes formatting: Notes displayed in readable format (paragraphs, sections, proper spacing)
10. Mobile responsive: Notes display and editing work on mobile devices

#### Story 6.7: Provider Dashboard & Workflow Tools

**As a** doctor,  
**I want** a provider dashboard with workflow tools (patient queue, quick actions, notifications),  
**so that** I can efficiently manage my patient load and prioritize tasks.

**Acceptance Criteria:**
1. Provider dashboard: Doctor sees customized dashboard with patient queue, upcoming consultations, pending tasks
2. Patient queue: Shows list of patients needing attention (upcoming consultations, pending notes, follow-ups)
3. Quick actions: Dashboard includes quick action buttons: "Start Consultation", "Add Notes", "Generate Prescription", "View Patient EHR"
4. Notifications: Doctor sees notifications (new consultation requests, patient messages, lab results available)
5. Dashboard endpoint: GET `/api/doctors/:id/dashboard` returns dashboard data (authenticated doctor)
6. Task management: System tracks pending tasks (incomplete notes, pending prescriptions, follow-up reminders)
7. Efficiency metrics: Dashboard shows efficiency metrics (consultations today, average consultation duration, notes completion rate)
8. Mobile responsive: Provider dashboard works on mobile devices (responsive layout, touch-friendly)
9. Customization: Doctor can customize dashboard layout (hide/show sections, reorder widgets)
10. Integration: Dashboard integrates with all provider tools (consultations, notes, prescriptions, EHR)

#### Story 6.8: Prescription Refill & Renewal Management

**As a** patient,  
**I want** to request prescription refills and renewals,  
**so that** I can continue medications without scheduling unnecessary consultations.

**Acceptance Criteria:**
1. Refill request: Patient can request prescription refill from prescriptions page ("Request Refill" button)
2. Refill endpoint: POST `/api/prescriptions/:id/refill-request` creates refill request (authenticated patient)
3. Refill validation: System checks if prescription is eligible for refill (within validity period, not expired)
4. Doctor notification: Doctor receives notification of refill request (email/SMS/WhatsApp, Epic 8 integration)
5. Doctor approval: Doctor can approve/deny refill request from provider dashboard ("Approve Refill" button)
6. Auto-refill: If approved, system generates new prescription automatically (same medications, updated date)
7. Refill history: Patient can view refill history (when requested, when approved, refill count)
8. Refill limits: System enforces refill limits (e.g., maximum 3 refills per prescription, requires new consultation)
9. Refill delivery: Approved refills delivered via WhatsApp/email (same as new prescriptions, Story 6.2)
10. Mobile responsive: Refill request flow works seamlessly on mobile devices

---

### Epic 7: Payment & Subscription Management

**Expanded Goal:** Implement subscription billing (₹3,500/month standard, ₹6,000/month with GLP-1), payment gateway integration (Razorpay/Stripe), transparent pricing display, and subscription lifecycle management. This enables the business model with predictable recurring revenue, reduces churn through subscription stickiness, and provides transparent pricing as a competitive advantage. The system handles payment processing, subscription renewals, payment failures, and provides clear pricing information to build trust.

#### Story 7.1: Payment Gateway Integration & Configuration

**As a** developer,  
**I want** payment gateway (Razorpay or Stripe India) integrated and configured,  
**so that** secure payment processing can handle subscription payments and one-time transactions.

**Acceptance Criteria:**
1. Payment gateway integration: Razorpay API integrated (recommended for India market) or Stripe India as alternative
2. API credentials: Payment gateway API keys configured securely (stored in environment variables, not in code)
3. Payment gateway endpoint: Payment gateway webhook endpoint configured to receive payment status updates
4. Webhook security: Webhook requests verified using payment gateway signature validation (prevent fraud)
5. Payment model: Database model stores payment transactions (amount, status, payment gateway transaction ID, timestamp)
6. Test mode: System supports test mode for development (test API keys, sandbox environment)
7. Production mode: System switches to production mode with live API keys (environment-based configuration)
8. Error handling: Payment gateway API failures handled gracefully (retry logic, error logging, user-friendly messages)
9. Transaction logging: All payment transactions logged for audit (Epic 9 compliance)
10. Payment status tracking: System tracks payment status (pending/success/failed/refunded) for each transaction

#### Story 7.2: Subscription Plans & Pricing Model

**As a** product manager,  
**I want** subscription plans (Standard ₹3,500/month, GLP-1 ₹6,000/month) configured in the system,  
**so that** patients can subscribe to appropriate plans based on their needs.

**Acceptance Criteria:**
1. Subscription plan model: Database stores subscription plans (plan ID, name, price, features, duration)
2. Standard plan: ₹3,500/month plan configured (basic consultations, tracking, support)
3. GLP-1 plan: ₹6,000/month plan configured (includes GLP-1 therapy management, priority support)
4. Plan features: Each plan includes feature list (what's included: consultations, tracking, WhatsApp support, etc.)
5. Plan endpoint: GET `/api/subscription-plans` returns available plans (public endpoint, no authentication)
6. Plan display: Plans displayed in pricing page (Story 7.8) with clear feature comparison
7. Plan pricing: Pricing stored in database (allows future price changes without code changes)
8. Plan duration: Plans support monthly billing (future: annual plans, 6-month plans)
9. Plan activation: Plans can be activated/deactivated by admin (control which plans are available)
10. Plan validation: System validates plan exists and is active before allowing subscription

#### Story 7.3: Subscription Creation & Initial Payment

**As a** patient,  
**I want** to subscribe to a plan and complete initial payment,  
**so that** I can access platform features and start my metabolic health journey.

**Acceptance Criteria:**
1. Subscription creation: Patient can select subscription plan from pricing page ("Subscribe" button)
2. Subscription endpoint: POST `/api/subscriptions` creates subscription (authenticated patient, plan ID, payment method)
3. Payment method: Patient enters payment details (card number, expiry, CVV) or UPI/Wallet (Razorpay supports Indian payment methods)
4. Payment processing: System processes payment through payment gateway (Razorpay API call)
5. Payment success: If payment succeeds, subscription activated, patient gains access to platform features
6. Payment failure: If payment fails, clear error message displayed, subscription not created, patient can retry
7. Subscription status: Subscription status tracked (active/trial/cancelled/past_due)
8. Subscription start date: Subscription start date set to payment date, renewal date calculated (start date + 1 month)
9. Email confirmation: Patient receives email confirmation with subscription details (plan, price, renewal date)
10. Mobile responsive: Subscription creation and payment flow works seamlessly on mobile devices

#### Story 7.4: Subscription Renewal & Recurring Billing

**As a** system,  
**I want** to automatically renew subscriptions and process recurring payments,  
**so that** subscriptions continue seamlessly without manual intervention.

**Acceptance Criteria:**
1. Renewal scheduler: System has scheduled job (cron job or background worker) that runs daily to check subscriptions due for renewal
2. Renewal detection: System identifies subscriptions due for renewal (renewal date = today or within 3 days)
3. Automatic payment: System automatically charges payment method on file (payment gateway recurring payment API)
4. Renewal success: If payment succeeds, subscription renewed, renewal date updated (current date + 1 month), patient notified
5. Renewal failure: If payment fails, subscription status changed to "past_due", renewal retry scheduled (3 retry attempts over 7 days)
6. Payment retry: System retries failed payments (Day 1, Day 3, Day 7) before marking subscription as cancelled
7. Renewal notification: Patient receives email/SMS before renewal (3 days before) and after successful renewal
8. Renewal endpoint: Manual renewal endpoint available (POST `/api/subscriptions/:id/renew`) for admin use
9. Renewal history: System tracks renewal history (renewal date, payment status, amount charged)
10. Grace period: Subscription remains active during grace period (7 days) even if payment fails, access revoked after grace period

#### Story 7.5: Payment Failure Handling & Dunning Management

**As a** patient,  
**I want** clear notifications and opportunities to update payment methods when payments fail,  
**so that** I can resolve payment issues and maintain my subscription.

**Acceptance Criteria:**
1. Payment failure notification: Patient receives email/SMS immediately when payment fails ("Payment failed, update payment method")
2. Payment failure page: Patient dashboard shows "Payment Failed" banner with "Update Payment Method" button
3. Payment method update: Patient can update payment method (POST `/api/subscriptions/:id/payment-method`, new card/UPI details)
4. Retry payment: Patient can manually retry failed payment ("Retry Payment" button)
5. Grace period: Patient retains access during grace period (7 days) to resolve payment issues
6. Access revocation: After grace period, if payment still fails, subscription cancelled, access revoked, patient notified
7. Dunning emails: System sends dunning emails (Day 1, Day 3, Day 6) reminding patient to update payment method
8. Payment failure tracking: System tracks payment failure reasons (insufficient funds, card expired, declined) for analysis
9. Admin override: Admin can manually process payment or extend grace period if needed (admin endpoint)
10. Reactivation: Patient can reactivate cancelled subscription by updating payment method and paying outstanding amount

#### Story 7.6: Subscription Cancellation & Refunds

**As a** patient,  
**I want** to cancel my subscription and request refunds if applicable,  
**so that** I have control over my subscription and can discontinue service when needed.

**Acceptance Criteria:**
1. Cancellation request: Patient can cancel subscription from dashboard ("Cancel Subscription" button)
2. Cancellation endpoint: POST `/api/subscriptions/:id/cancel` cancels subscription (authenticated patient, own subscription only)
3. Cancellation options: Patient can choose immediate cancellation or cancel at end of billing period (pro-rated refund option)
4. Cancellation confirmation: Patient receives confirmation email/SMS with cancellation details (end date, refund status)
5. Access retention: If cancel at end of period, patient retains access until end of billing period
6. Immediate cancellation: If immediate cancellation, access revoked immediately, pro-rated refund processed
7. Refund processing: System processes refunds through payment gateway (Razorpay refund API) for pro-rated amounts
8. Refund tracking: Refund status tracked (pending/processed/failed), patient notified when refund processed
9. Cancellation reason: System collects cancellation reason (optional survey: "Why are you cancelling?") for insights
10. Reactivation: Patient can reactivate cancelled subscription within 30 days (same plan, new payment required)

#### Story 7.7: Subscription Management Dashboard (Patient View)

**As a** patient,  
**I want** to view my subscription details, billing history, and manage my subscription,  
**so that** I can track my payments and control my account.

**Acceptance Criteria:**
1. Subscription dashboard: Patient dashboard includes "My Subscription" section showing current plan, status, renewal date
2. Subscription details: Displays plan name, price, billing cycle (monthly), next renewal date, payment method (masked)
3. Billing history: Shows list of past payments (date, amount, status, invoice download)
4. Invoice download: Patient can download invoices as PDF (GET `/api/subscriptions/:id/invoices/:invoiceId`)
5. Payment method management: Patient can view/update payment method ("Update Payment Method" button)
6. Subscription actions: Quick actions: "Upgrade Plan", "Cancel Subscription", "Update Payment Method"
7. Subscription endpoint: GET `/api/subscriptions/:id` returns subscription details (authenticated patient, own subscription)
8. Invoice generation: System generates invoices automatically for each payment (PDF format, stored in S3)
9. Mobile responsive: Subscription dashboard displays correctly on mobile devices
10. Empty state: If no active subscription, shows "Subscribe Now" CTA linking to pricing page

#### Story 7.8: Transparent Pricing Page

**As a** potential patient,  
**I want** to see clear, transparent pricing with no hidden costs,  
**so that** I can make informed decisions and trust the platform.

**Acceptance Criteria:**
1. Pricing page: Public pricing page accessible from landing page ("Pricing" link in navigation)
2. Plan display: All subscription plans displayed with clear pricing (₹3,500/month Standard, ₹6,000/month GLP-1)
3. Feature comparison: Each plan shows included features (consultations, tracking, WhatsApp support, etc.) in comparison table
4. Pricing transparency: Clear statement: "No hidden costs, transparent pricing, cancel anytime"
5. Competitive comparison: Optional comparison table (MetaboWell vs. competitors: HealthifyRx, Veera) highlighting advantages
6. FAQ section: Pricing page includes FAQ addressing common questions (billing, cancellation, refunds)
7. CTA buttons: Each plan has "Subscribe Now" button linking to subscription creation flow
8. Mobile responsive: Pricing page displays correctly on mobile devices (responsive table, stack layout)
9. Trust indicators: Pricing page includes trust elements (doctor credentials, patient testimonials after launch)
10. Currency display: Pricing displayed in Indian Rupees (₹) with clear formatting

#### Story 7.9: Subscription Upgrade & Downgrade

**As a** patient,  
**I want** to upgrade or downgrade my subscription plan,  
**so that** I can adjust my plan based on changing needs (e.g., starting GLP-1 therapy).

**Acceptance Criteria:**
1. Upgrade option: Patient can upgrade from Standard to GLP-1 plan ("Upgrade Plan" button in subscription dashboard)
2. Upgrade endpoint: POST `/api/subscriptions/:id/upgrade` upgrades subscription (authenticated patient, plan ID)
3. Pro-rated billing: Upgrade charges pro-rated amount (difference between plans for remaining days in billing period)
4. Immediate upgrade: Upgrade takes effect immediately, patient gains access to upgraded plan features
5. Downgrade option: Patient can downgrade from GLP-1 to Standard plan ("Downgrade Plan" button)
6. Downgrade endpoint: POST `/api/subscriptions/:id/downgrade` downgrades subscription
7. Downgrade timing: Downgrade takes effect at end of current billing period (patient retains GLP-1 features until period ends)
8. Pro-rated refund: Downgrade refunds pro-rated amount (difference for remaining days) to payment method
9. Upgrade/downgrade confirmation: Patient receives email confirmation with new plan details, billing changes
10. Plan change history: System tracks plan changes (upgrade/downgrade history) for audit and analysis

---

### Epic 8: Content & Support Integration

**Expanded Goal:** Deliver educational content library (blogs, videos), WhatsApp Business API integration for patient support (<2 hour response guarantee), and diagnostic lab partnership integration for home blood tests and results delivery. This supports the "education-first" approach that builds trust and reduces CAC through SEO value, provides critical support for GLP-1 side effects, and integrates lab services for a complete care ecosystem. The content library educates patients about metabolic health, while WhatsApp support addresses urgent needs, and lab integration eliminates friction in diagnostic testing.

#### Story 8.1: Educational Content Library Foundation

**As a** content manager,  
**I want** a content management system for educational articles and videos,  
**so that** patients can access reliable metabolic health information and we can build SEO value.

**Acceptance Criteria:**
1. Content model: Database stores content articles (title, body, author, publish date, category, tags, SEO metadata)
2. Content categories: Content organized by categories (GLP-1 Safety, Obesity as Disease, PCOS Management, Diabetes Reversal, Nutrition, Exercise)
3. Content creation: Admin endpoint to create/edit content (POST `/api/admin/content`, authenticated admin only)
4. Content display: Public content library page accessible from navigation ("Learn" or "Resources" link)
5. Content listing: Content displayed as cards (title, excerpt, category, read time, publish date)
6. Content search: Search functionality allows filtering by category, tags, or keyword search
7. Content pagination: Content paginated (10 articles per page) or infinite scroll
8. SEO optimization: Content includes SEO metadata (meta title, meta description, keywords) for search engine optimization
9. Content status: Content can be draft/published (admin controls visibility)
10. Mobile responsive: Content library displays correctly on mobile devices

#### Story 8.2: Educational Article Display & Reading Experience

**As a** patient,  
**I want** to read educational articles with clear formatting and navigation,  
**so that** I can learn about metabolic health topics at my own pace.

**Acceptance Criteria:**
1. Article page: Individual article page displays full article content (title, author, publish date, body, category)
2. Article formatting: Articles formatted with headings, paragraphs, lists, images (readable, scannable format)
3. Article navigation: Article page includes "Back to Library" link, related articles section, category navigation
4. Reading time: Article displays estimated reading time (calculated from word count)
5. Share functionality: Patient can share article via WhatsApp, email, or social media ("Share" button)
6. Article endpoint: GET `/api/content/:id` returns article content (public endpoint, no authentication required)
7. Related articles: Article page shows related articles (same category, similar tags) for discovery
8. Table of contents: Long articles include table of contents for easy navigation (if >1000 words)
9. Mobile responsive: Article page displays correctly on mobile devices (readable font, proper spacing)
10. Print-friendly: Article page is print-friendly (clean layout, no ads, proper page breaks)

#### Story 8.3: Video Content Integration & Display

**As a** patient,  
**I want** to watch educational videos about metabolic health,  
**so that** I can learn through visual content that's easier to understand than text.

**Acceptance Criteria:**
1. Video model: Database stores video content (title, description, video URL, thumbnail, duration, category, publish date)
2. Video hosting: Videos hosted on YouTube or Vimeo (external hosting, embed in platform)
3. Video display: Video content page displays embedded video player with title, description, category
4. Video listing: Video library page shows video thumbnails, titles, durations, categories
5. Video search: Videos searchable by category, keyword, or tags
6. Video endpoint: GET `/api/content/videos` returns video list (public endpoint)
7. Video metadata: Videos include metadata (duration, view count if available, publish date)
8. Video categories: Videos organized by categories (same as articles: GLP-1 Safety, PCOS, Diabetes, etc.)
9. Mobile responsive: Video player works on mobile devices (responsive embed, touch controls)
10. Video analytics: System tracks video views (if possible) for content performance analysis

#### Story 8.4: WhatsApp Business API Integration & Configuration

**As a** developer,  
**I want** WhatsApp Business API integrated and configured,  
**so that** patients can receive support via WhatsApp with guaranteed <2 hour response time.

**Acceptance Criteria:**
1. WhatsApp API integration: WhatsApp Business API integrated with API credentials configured
2. API configuration: WhatsApp API webhook configured to receive incoming messages
3. Message model: Database stores WhatsApp messages (patient ID, doctor ID, message text, timestamp, direction: inbound/outbound, status)
4. Webhook security: Webhook requests verified using WhatsApp signature validation (prevent fraud)
5. Message routing: Incoming messages routed to assigned doctor or support team based on patient assignment
6. Message status tracking: System tracks message status (sent/delivered/read/failed) for monitoring
7. Test mode: System supports test mode for development (test API credentials, sandbox)
8. Production mode: System switches to production mode with live API credentials
9. Error handling: WhatsApp API failures handled gracefully (retry logic, error logging, fallback to email)
10. Rate limiting: System respects WhatsApp API rate limits (prevent API blocking)

#### Story 8.5: WhatsApp Support Interface & Message Handling

**As a** patient,  
**I want** to send WhatsApp messages to my assigned doctor and receive responses,  
**so that** I can get quick support for side effects or questions without scheduling consultations.

**Acceptance Criteria:**
1. WhatsApp initiation: Patient can initiate WhatsApp conversation from dashboard ("Contact Support via WhatsApp" button)
2. WhatsApp link: Button opens WhatsApp Business chat (phone number pre-filled) or in-app WhatsApp interface
3. Message sending: Patient can send messages via WhatsApp (through WhatsApp Business API or direct WhatsApp link)
4. Message receiving: Patient receives WhatsApp messages from doctor/support team
5. Message display: If in-app interface, messages displayed in chat interface (inbound/outbound, timestamps)
6. Response time tracking: System tracks response times (time from patient message to doctor response)
7. Response time guarantee: System monitors <2 hour response time (NFR6 requirement), alerts if exceeded
8. Message history: Patient can view WhatsApp message history from dashboard ("Support Messages" section)
9. Message notifications: Patient receives WhatsApp notifications for new messages (if enabled)
10. Mobile-friendly: WhatsApp integration works seamlessly on mobile devices (native WhatsApp app preferred)

#### Story 8.6: Doctor WhatsApp Support Dashboard

**As a** doctor,  
**I want** to receive and respond to patient WhatsApp messages from a dashboard,  
**so that** I can provide timely support and meet the <2 hour response guarantee.

**Acceptance Criteria:**
1. Doctor WhatsApp dashboard: Doctor sees "Support Messages" section in provider dashboard with list of patient messages
2. Message queue: Messages displayed in queue (newest first, unread messages highlighted)
3. Message display: Doctor sees patient name, message text, timestamp, response status (pending/responded)
4. Message response: Doctor can respond to messages directly from dashboard (text input, send button)
5. Response endpoint: POST `/api/doctors/:id/whatsapp-messages/:messageId/respond` sends response (authenticated doctor)
6. Response time indicator: Dashboard shows response time (e.g., "2 hours remaining" for <2 hour guarantee)
7. Message filtering: Doctor can filter messages by patient, status (unread/read), date
8. Quick responses: Doctor can use quick response templates (e.g., "Thanks for reaching out, I'll review and respond shortly")
9. Message assignment: Messages automatically assigned to patient's assigned doctor (Epic 2 dependency)
10. Mobile responsive: Doctor WhatsApp dashboard works on mobile devices (critical for on-the-go support)

#### Story 8.7: Diagnostic Lab Partnership Integration Foundation

**As a** developer,  
**I want** lab partnership integration foundation established,  
**so that** patients can order home blood tests and receive results automatically in EHR.

**Acceptance Criteria:**
1. Lab model: Database stores lab partners (lab name, API endpoint, credentials, test catalog)
2. Lab API integration: Integration with lab partner API (Thyrocare, Dr. Lal PathLabs, or equivalent) configured
3. Test catalog: System stores available lab tests (test name, code, price, description, fasting requirements)
4. Lab API credentials: Lab API credentials configured securely (environment variables)
5. Test ordering: Foundation for ordering lab tests (POST `/api/lab-tests/order`, authenticated patient)
6. Order tracking: System tracks lab test orders (order ID, patient ID, test name, status: ordered/completed/failed)
7. Results integration: Foundation for receiving lab results via API (webhook or polling)
8. Error handling: Lab API failures handled gracefully (manual workflow fallback if API unavailable)
9. Test mode: System supports test mode for development (sandbox API or mock responses)
10. Lab partner management: Admin can add/manage lab partners (admin endpoint for lab partner configuration)

#### Story 8.8: Home Blood Test Ordering & Management

**As a** patient,  
**I want** to order home blood tests through the platform,  
**so that** I can get diagnostic tests without visiting labs.

**Acceptance Criteria:**
1. Lab test catalog: Patient can browse available lab tests from dashboard ("Order Lab Test" link)
2. Test selection: Patient can select tests (HbA1c, Lipid Profile, Thyroid Function, etc.) with test descriptions and prices
3. Test ordering: Patient can order tests (POST `/api/lab-tests/order`, authenticated patient, test selection, address)
4. Home visit scheduling: System schedules home visit for sample collection (date/time selection, address confirmation)
5. Order confirmation: Patient receives confirmation email/SMS/WhatsApp with order details, scheduled visit date/time
6. Order tracking: Patient can track order status (ordered → sample collected → processing → results ready)
7. Order history: Patient dashboard shows lab test order history (date, test name, status, results link if available)
8. Payment integration: Lab test orders processed through payment gateway (Story 7.1 integration, one-time payment)
9. Address management: Patient can save addresses for home visits (multiple addresses supported)
10. Mobile responsive: Lab test ordering flow works seamlessly on mobile devices

#### Story 8.9: Lab Results Integration & EHR Import

**As a** patient,  
**I want** lab results automatically imported into my EHR,  
**so that** I don't need to manually upload results and doctors can see them immediately.

**Acceptance Criteria:**
1. Results webhook: Lab partner sends results via webhook (or system polls for results) when tests complete
2. Results parsing: System parses lab results (test name, values, reference ranges, date) from lab API response
3. Results storage: Lab results automatically saved to patient EHR (Epic 5.7 integration, linked to patient ID)
4. Results notification: Patient receives notification (email/SMS/WhatsApp) when results ready ("Your lab results are ready")
5. Results display: Patient can view results in EHR dashboard (Epic 5.7, automatic import vs. manual upload)
6. Results comparison: System compares new results to previous results (shows trends, improvement/decline)
7. Doctor notification: Assigned doctor receives notification when patient's lab results available
8. Results accuracy: System validates results data (date, values, reference ranges) before importing
9. Manual fallback: If automatic import fails, patient can manually upload results (Epic 5.7 fallback)
10. Results security: Lab results encrypted and access-controlled (only patient and assigned doctor can view)

**Note:** This story depends on Epic 8.7 (lab integration foundation) and Epic 5.7 (lab results display). Automatic import is ideal, but manual upload fallback ensures functionality even if lab API unavailable.

#### Story 8.10: Content SEO Optimization & Discovery

**As a** content manager,  
**I want** content optimized for search engines,  
**so that** patients can discover MetaboWell through organic search and reduce CAC.

**Acceptance Criteria:**
1. SEO metadata: All content includes SEO metadata (meta title, meta description, keywords, OG tags for social sharing)
2. Content URLs: Content URLs are SEO-friendly (e.g., `/learn/glp-1-safety-guide` not `/content/123`)
3. Sitemap generation: System generates XML sitemap for search engines (includes all published content)
4. Robots.txt: Proper robots.txt configured (allows search engine crawling, blocks admin pages)
5. Internal linking: Content includes internal links to related articles (improves SEO, user engagement)
6. Content structure: Content structured with proper headings (H1, H2, H3) for SEO and readability
7. Image optimization: Content images optimized (alt text, file size, lazy loading) for SEO and performance
8. Mobile SEO: Content is mobile-friendly (responsive design, fast loading) for mobile search rankings
9. Analytics integration: Content analytics tracked (page views, time on page, bounce rate) for SEO insights
10. Keyword optimization: Content optimized for target keywords ("GLP-1 India", "diabetes reversal", "PCOS treatment")

---

### Epic 9: Compliance & Security Hardening

**Expanded Goal:** Complete DISHA compliance infrastructure (data encryption, audit logs, consent management), security hardening, performance optimization, and prepare for Digital Personal Data Protection Act compliance. This ensures legal compliance, builds trust through security, and creates a competitive moat (compliance overhead for new entrants). The system protects patient data, maintains audit trails for regulatory requirements, and optimizes performance to meet NFR requirements. This epic hardens the platform for production launch and ongoing operations.

#### Story 9.1: Data Encryption & Security Infrastructure

**As a** security engineer,  
**I want** all sensitive data encrypted at rest and in transit,  
**so that** patient medical data is protected from unauthorized access and breaches.

**Acceptance Criteria:**
1. Encryption at rest: All database data encrypted using AES-256 encryption (PostgreSQL encryption or application-level encryption)
2. Encryption in transit: All API communications use TLS 1.3 (HTTPS) with valid SSL certificates
3. Encryption keys: Encryption keys stored securely (AWS KMS, HashiCorp Vault, or equivalent key management service)
4. Key rotation: System supports encryption key rotation (can rotate keys without data loss)
5. Encrypted fields: Sensitive fields encrypted (patient medical history, lab results, prescriptions, consultation notes)
6. Password security: Passwords hashed using bcrypt (minimum 10 rounds) or equivalent secure algorithm
7. API security: API endpoints require authentication (JWT tokens) and authorization (RBAC checks)
8. Security headers: Application includes security headers (HSTS, CSP, X-Frame-Options) to prevent attacks
9. Security audit: Security audit performed (vulnerability scanning, penetration testing) before production launch
10. Compliance validation: Encryption implementation validated against DISHA requirements (documentation, testing)

#### Story 9.2: Audit Logging & Access Tracking

**As a** compliance officer,  
**I want** comprehensive audit logs for all data access and modifications,  
**so that** we can demonstrate DISHA compliance and track security incidents.

**Acceptance Criteria:**
1. Audit log model: Database stores audit logs (user ID, action, resource, timestamp, IP address, user agent, result: success/failure)
2. Logging scope: System logs all EHR access (who accessed, when, what data viewed), data modifications (who changed, what changed, when)
3. Logging endpoints: System logs API access (endpoint, method, parameters, response status, execution time)
4. Logging persistence: Audit logs stored in separate database/table (prevent tampering, long-term retention)
5. Log retention: Audit logs retained for minimum 7 years (per Indian medical records regulations)
6. Log search: Admin can search audit logs (by user, date, action, resource) for compliance audits
7. Log export: System can export audit logs for regulatory submissions (CSV, JSON format)
8. Real-time monitoring: System monitors audit logs for suspicious activity (multiple failed logins, unauthorized access attempts)
9. Log integrity: Audit logs are tamper-proof (immutable logs, cryptographic hashing) to prevent manipulation
10. Compliance reporting: System generates compliance reports (access logs, data modifications, security incidents) for DISHA audits

#### Story 9.3: Role-Based Access Control (RBAC) Implementation

**As a** security engineer,  
**I want** comprehensive RBAC system implemented,  
**so that** users can only access data and features appropriate to their role.

**Acceptance Criteria:**
1. Role model: System defines roles (patient, doctor, admin, support_staff) with permissions
2. Permission model: Permissions defined for each role (view own EHR, view assigned patients' EHR, view all EHR, manage users, etc.)
3. RBAC middleware: API endpoints protected by RBAC middleware (checks user role, verifies permissions)
4. Patient access: Patients can only access own data (EHR, prescriptions, consultations, own profile)
5. Doctor access: Doctors can only access assigned patients' data (EHR, consultations, notes, prescriptions)
6. Admin access: Admins can access all data (for platform management, support, compliance)
7. Permission checks: All sensitive endpoints verify permissions before allowing access (no unauthorized data leaks)
8. Role assignment: Users assigned roles during registration or by admin (Epic 1 integration)
9. Permission updates: Admin can update role permissions (future flexibility, audit log of permission changes)
10. RBAC testing: RBAC tested thoroughly (unauthorized access attempts fail, authorized access succeeds)

#### Story 9.4: Consent Management Framework

**As a** compliance officer,  
**I want** a consent management system for patient data usage,  
**so that** we comply with DISHA and prepare for Digital Personal Data Protection Act (DPDP Act).

**Acceptance Criteria:**
1. Consent model: Database stores consent records (patient ID, consent type, consent status: granted/withdrawn, timestamp, version)
2. Consent types: System manages consent types (data collection, data sharing, marketing communications, consultation recording)
3. Consent collection: Patients provide consent during onboarding (checkbox: "I consent to data collection and usage")
4. Consent display: Patients can view all consents from dashboard ("Privacy & Consent" section)
5. Consent withdrawal: Patients can withdraw consent (consent status updated, system respects withdrawal)
6. Consent versioning: System tracks consent versions (when consent changed, what changed) for audit trail
7. Consent validation: System validates consent before data operations (check consent status before accessing data)
8. Consent reminders: System sends consent renewal reminders (if consent expires or regulations require renewal)
9. Consent export: Patients can export consent history (for personal records, compliance)
10. DPDP Act preparation: Consent framework flexible enough to adapt to upcoming DPDP Act requirements

#### Story 9.5: Data Privacy & Patient Rights

**As a** patient,  
**I want** control over my data (access, export, deletion),  
**so that** I can exercise my privacy rights under DISHA and DPDP Act.

**Acceptance Criteria:**
1. Data access: Patients can access all their data (EHR export, Story 5.9 integration, comprehensive data export)
2. Data export: Patients can export complete data (GET `/api/patients/:id/data-export`) including EHR, consultations, prescriptions, messages
3. Data portability: Export format supports data portability (JSON, PDF) for sharing with other healthcare providers
4. Data deletion: Patients can request data deletion (DELETE `/api/patients/:id/data`) with proper authorization
5. Deletion workflow: Data deletion requires confirmation (prevents accidental deletion, audit log of deletion requests)
6. Deletion scope: Deletion includes all patient data (EHR, consultations, prescriptions, messages, account) or partial deletion (specific data types)
7. Deletion compliance: Deletion complies with regulations (medical records retention requirements, audit log retention)
8. Right to rectification: Patients can request data correction (PUT `/api/patients/:id/data-correction`) for inaccurate data
9. Privacy policy: Platform includes clear privacy policy (what data collected, how used, patient rights)
10. Privacy dashboard: Patients have privacy dashboard (view data, manage consent, request export/deletion) in settings

#### Story 9.6: Performance Optimization & Caching

**As a** system administrator,  
**I want** performance optimization and caching implemented,  
**so that** the platform meets NFR requirements (page load <3 seconds, 99.5% uptime).

**Acceptance Criteria:**
1. Database optimization: Database queries optimized (indexes on critical fields, query optimization, connection pooling)
2. Caching layer: Redis caching implemented for frequently accessed data (doctor profiles, pricing, content, session data)
3. API response caching: API responses cached where appropriate (GET endpoints, static data, reduce database load)
4. CDN integration: Static assets (images, videos, CSS, JS) served via CDN (CloudFront/Cloudflare) for faster delivery
5. Image optimization: Images optimized (compression, WebP format, lazy loading) for faster page loads
6. Code optimization: Frontend code optimized (minification, bundling, code splitting) for faster initial load
7. Performance monitoring: Performance monitoring implemented (page load times, API response times, database query times)
8. Performance targets: System meets NFR targets (page load <3 seconds, API response <500ms for most endpoints)
9. Load testing: Load testing performed (simulate 200+ concurrent users) to validate performance under load
10. Performance reporting: System generates performance reports (slow queries, high response times) for optimization

#### Story 9.7: Security Monitoring & Incident Response

**As a** security engineer,  
**I want** security monitoring and incident response procedures,  
**so that** security threats are detected and responded to quickly.

**Acceptance Criteria:**
1. Security monitoring: System monitors security events (failed logins, unauthorized access attempts, suspicious API calls)
2. Alert system: Security alerts configured (email/SMS notifications for critical security events)
3. Intrusion detection: System detects intrusion attempts (brute force attacks, SQL injection attempts, XSS attempts)
4. Rate limiting: API rate limiting implemented (prevent abuse, DDoS protection)
5. Incident response plan: Incident response plan documented (what to do if breach detected, who to notify, how to respond)
6. Security logging: Security events logged (failed logins, access denials, suspicious activity) for investigation
7. Security dashboard: Admin security dashboard shows security metrics (failed logins, blocked IPs, security alerts)
8. IP blocking: System can block malicious IPs (manual or automatic blocking after multiple failed attempts)
9. Security updates: System supports security updates (patch management, dependency updates, vulnerability fixes)
10. Security audit: Regular security audits performed (quarterly vulnerability scans, annual penetration testing)

#### Story 9.8: Backup & Disaster Recovery

**As a** system administrator,  
**I want** comprehensive backup and disaster recovery procedures,  
**so that** data is protected and can be restored in case of failures.

**Acceptance Criteria:**
1. Automated backups: Database backups automated (daily full backups, hourly incremental backups)
2. Backup storage: Backups stored securely (encrypted, off-site storage, AWS S3 or equivalent)
3. Backup retention: Backups retained for 30 days (configurable, supports longer retention if needed)
4. Backup testing: Backup restoration tested regularly (monthly restoration tests to verify backup integrity)
5. Disaster recovery plan: Disaster recovery plan documented (RTO: Recovery Time Objective, RPO: Recovery Point Objective)
6. Multi-AZ deployment: Production system deployed across multiple availability zones (high availability)
7. Database replication: Database read replicas configured (improve performance, backup for failover)
8. Failover procedures: Automated failover procedures configured (database failover, application failover)
9. Data redundancy: Critical data replicated across multiple regions (protect against regional failures)
10. Recovery testing: Disaster recovery tested annually (full disaster recovery drill, validate procedures)

#### Story 9.9: Compliance Documentation & Reporting

**As a** compliance officer,  
**I want** compliance documentation and reporting capabilities,  
**so that** we can demonstrate DISHA compliance and pass regulatory audits.

**Acceptance Criteria:**
1. Compliance documentation: DISHA compliance documentation created (data security policies, access control policies, incident response procedures)
2. Compliance checklist: DISHA compliance checklist maintained (track compliance requirements, verify implementation)
3. Compliance reports: System generates compliance reports (access logs, data modifications, security incidents, consent records)
4. Audit trail: Complete audit trail available (who accessed what, when, why) for regulatory audits
5. Data retention policy: Data retention policy documented (how long data retained, when data deleted, compliance with regulations)
6. Privacy policy: Privacy policy published (what data collected, how used, patient rights, contact information)
7. Terms of service: Terms of service published (platform usage terms, liability, dispute resolution)
8. Compliance training: Compliance training materials created (for staff, doctors, support team)
9. Regulatory updates: System tracks regulatory updates (DISHA amendments, DPDP Act progress) for compliance adjustments
10. Compliance audit: External compliance audit performed (third-party audit of DISHA compliance) before production launch

#### Story 9.10: ISO 27001 Preparation (Phase 2 Foundation)

**As a** security engineer,  
**I want** security infrastructure prepared for ISO 27001 certification,  
**so that** we can achieve ISO 27001 certification in Phase 2 as planned.

**Acceptance Criteria:**
1. Security policies: Security policies documented (information security policy, access control policy, incident response policy)
2. Security controls: ISO 27001 security controls implemented (access control, cryptography, physical security, operations security)
3. Risk assessment: Security risk assessment performed (identify risks, assess impact, mitigation strategies)
4. Security awareness: Security awareness program established (training, phishing simulations, security best practices)
5. Incident management: Incident management procedures documented (incident detection, response, recovery, lessons learned)
6. Change management: Change management procedures documented (code changes, infrastructure changes, security reviews)
7. Vendor management: Vendor security assessments performed (third-party vendors, API providers, security reviews)
8. Business continuity: Business continuity plan documented (backup procedures, disaster recovery, service continuity)
9. Security metrics: Security metrics tracked (incidents, vulnerabilities, compliance, training completion)
10. ISO 27001 gap analysis: ISO 27001 gap analysis performed (identify gaps, create roadmap for certification)

**Note:** ISO 27001 certification is Phase 2 target (Months 7-18). This story establishes foundation and prepares infrastructure. Full certification requires additional documentation, processes, and external audit.

---

**Total Stories:** 67 stories across 9 epics

---

## User Journey Flow Diagrams

### Journey 1: New Patient Onboarding & First Consultation

```
┌─────────────────────────────────────────────────────────────────┐
│                    NEW PATIENT ONBOARDING FLOW                  │
└─────────────────────────────────────────────────────────────────┘

START: Landing Page
  │
  ├─> [Views Value Proposition]
  │   "Your metabolic health partner for life"
  │   Visual: Relatable imagery, empowerment messaging
  │
  ├─> [Clicks "Get Started" or "Book Free Assessment"]
  │
  ├─> STEP 1: Basic Registration
  │   ├─> Conversational UI: "What's your email?"
  │   ├─> Enter email + password (or phone + OTP)
  │   ├─> Validation & account creation
  │   └─> Auto-login, redirect to Step 2
  │
  ├─> STEP 2: Health Profile Basics
  │   ├─> "What's your current weight?" (conversational)
  │   ├─> "What's your height?" → Auto-calculate BMI
  │   ├─> "What's your primary health concern?"
  │   │   └─> Multi-select: Obesity, Diabetes, PCOS, etc.
  │   ├─> "What's your weight loss goal?" (optional, can skip)
  │   └─> Save progress, redirect to Step 3
  │
  ├─> STEP 3: Location & Preferences
  │   ├─> "Where are you located?" (dropdown: Vizag, Tier-1, Other)
  │   ├─> "What's your consultation preference?"
  │   │   └─> Radio: In-person / Video / Both
  │   ├─> "Preferred language?" (English / Hindi)
  │   └─> Onboarding complete! → Redirect to Dashboard
  │
  ├─> Dashboard (First Time)
  │   ├─> Shows: "No doctor assigned yet"
  │   ├─> CTA: "Find a Doctor" or "Browse Doctors"
  │   └─> Quick actions: Book Consultation, View Health Records
  │
  ├─> Doctor Marketplace
  │   ├─> Browse doctor profiles (photos, credentials, specializations)
  │   ├─> Filter by specialization, experience
  │   ├─> View doctor profile (RMP certification, bio, availability)
  │   └─> Click "Select This Doctor" or "Book Consultation"
  │
  ├─> Doctor Assignment
  │   ├─> Confirmation: "Dr. [Name] is now your assigned doctor"
  │   └─> Dashboard updates: Shows assigned doctor
  │
  ├─> Consultation Booking
  │   ├─> Select consultation type: Physical (if Vizag) or Video
  │   ├─> Select date/time from calendar (based on doctor availability)
  │   ├─> If Physical: See clinic address, directions, what to bring
  │   ├─> If Video: See "Video link will be sent 15 min before"
  │   └─> Confirm booking
  │
  ├─> Booking Confirmation
  │   ├─> Email/SMS/WhatsApp confirmation with details
  │   ├─> Calendar integration (iCal download or Google Calendar)
  │   └─> Reminders scheduled (24 hours before, 2 hours before)
  │
  └─> END: Patient ready for first consultation

DECISION POINTS:
  - Location (Vizag) → Physical consultation available
  - Location (Other) → Video consultation only
  - Consultation preference → Affects available options
```

### Journey 2: Physical Consultation (Vizag Patients)

```
┌─────────────────────────────────────────────────────────────────┐
│              PHYSICAL CONSULTATION JOURNEY (VIZAG)              │
└─────────────────────────────────────────────────────────────────┘

START: Consultation Scheduled
  │
  ├─> [24 Hours Before]
  │   └─> Reminder: SMS/WhatsApp with clinic address, directions
  │
  ├─> [2 Hours Before]
  │   └─> Reminder: "Your consultation is in 2 hours"
  │
  ├─> Day of Consultation
  │   ├─> Patient arrives at clinic (Vizag)
  │   ├─> Check-in at reception
  │   └─> Wait for doctor
  │
  ├─> Consultation Begins
  │   ├─> Doctor calls patient
  │   ├─> In-person consultation (30 minutes)
  │   ├─> Doctor reviews patient history (EHR access)
  │   ├─> Physical examination
  │   ├─> Discussion of symptoms, goals, treatment plan
  │   └─> Doctor may generate prescription (Epic 6)
  │
  ├─> Consultation Ends
  │   ├─> Doctor marks consultation as completed
  │   ├─> Patient receives notification: "Consultation completed"
  │   ├─> Prompt for doctor: "Add consultation notes?"
  │   └─> Prompt: "Generate prescription?" (if needed)
  │
  ├─> Post-Consultation
  │   ├─> Patient receives prescription (via WhatsApp/Email)
  │   ├─> Patient can view consultation summary in dashboard
  │   ├─> Follow-up booking suggested (if needed)
  │   └─> Review request (optional, after consultation)
  │
  └─> END: Consultation complete, prescription received

INTEGRATION POINTS:
  - EHR: Doctor accesses patient medical history
  - Prescriptions: Digital prescription generated
  - Follow-up: Video consultation can be booked for next visit
```

### Journey 3: Video Consultation (Follow-up Care)

```
┌─────────────────────────────────────────────────────────────────┐
│                  VIDEO CONSULTATION JOURNEY                     │
└─────────────────────────────────────────────────────────────────┘

START: Video Consultation Scheduled
  │
  ├─> [15 Minutes Before]
  │   └─> Video link sent via Email/SMS/WhatsApp
  │       "Your consultation starts in 15 minutes. Join here: [Link]"
  │
  ├─> [5 Minutes Before] (Optional)
  │   └─> Final reminder with video link
  │
  ├─> Consultation Time
  │   ├─> Patient clicks "Join Video Consultation" or link
  │   ├─> Pre-consultation check:
  │   │   ├─> Verify consultation time (±15 min window)
  │   │   ├─> Verify authentication
  │   │   └─> Verify consultation type is "video"
  │   │
  │   ├─> Browser requests camera/microphone permissions
  │   ├─> Video room loads
  │   │
  │   ├─> IF Doctor hasn't joined:
  │   │   └─> Patient sees "Waiting for doctor to join"
  │   │
  │   ├─> IF Both joined:
  │   │   ├─> Consultation status → "in-progress"
  │   │   ├─> Video interface: See doctor, see self, controls
  │   │   ├─> Audio/video controls (mute, camera on/off)
  │   │   │
  │   │   ├─> Consultation Flow:
  │   │   │   ├─> Doctor reviews patient EHR
  │   │   │   ├─> Discussion of symptoms, progress, vitals
  │   │   │   ├─> Doctor may share screen (lab results, charts)
  │   │   │   ├─> Treatment plan discussion
  │   │   │   └─> Prescription (if needed)
  │   │   │
  │   │   ├─> Recording (if consent given):
  │   │   │   ├─> "Recording in progress" indicator
  │   │   │   └─> Recording saved securely after consultation
  │   │   │
  │   │   └─> Connection quality monitoring
  │   │       └─> If poor: "Check your internet connection"
  │   │
  │   └─> Doctor ends consultation
  │       └─> Status → "completed"
  │
  ├─> Post-Consultation
  │   ├─> Patient notification: "Consultation ended"
  │   ├─> Doctor prompt: "Add consultation notes?" (voice-to-text)
  │   ├─> Patient can view consultation summary
  │   ├─> Prescription sent (if generated)
  │   ├─> Recording available (if recorded)
  │   └─> Follow-up booking suggested
  │
  └─> END: Video consultation complete

ERROR HANDLING:
  - Camera/mic denied → Clear error message, support contact
  - Connection drops → Auto-reconnect (up to 3 attempts)
  - Video fails → Contact support via WhatsApp
```

### Journey 4: Health Tracking & Progress Monitoring

```
┌─────────────────────────────────────────────────────────────────┐
│            HEALTH TRACKING & PROGRESS MONITORING                 │
└─────────────────────────────────────────────────────────────────┘

START: Patient Dashboard
  │
  ├─> Daily Tracking Routine
  │   ├─> Patient logs vitals (weight, blood sugar, BP)
  │   │   ├─> "Log Vitals" button on dashboard
  │   │   ├─> Simple form (<30 seconds to log)
  │   │   ├─> Input: Weight, Blood Sugar (fasting/post-meal), BP
  │   │   └─> Save → Data stored in EHR
  │   │
  │   ├─> Medication Tracking
  │   │   ├─> View current medications
  │   │   ├─> Mark "Taken" or "Missed" for each day
  │   │   └─> Adherence rate calculated automatically
  │   │
  │   └─> Symptom Logging (if needed)
  │       ├─> "Log Symptom" button
  │       ├─> Select symptom (nausea, fatigue, etc.)
  │       ├─> Rate severity (1-10 scale)
  │       └─> Save → Available for doctor review
  │
  ├─> Progress Visualization
  │   ├─> "My Progress" section on dashboard
  │   ├─> Charts showing:
  │   │   ├─> Weight over time (line graph)
  │   │   ├─> Blood sugar trends
  │   │   ├─> Blood pressure trends
  │   │   └─> Medication adherence calendar
  │   │
  │   ├─> Time range selector:
  │   │   └─> Last 7 days / 30 days / 3 months / All time
  │   │
  │   ├─> Trend indicators:
  │   │   └─> ↑ Improving / ↓ Declining / → Stable
  │   │
  │   └─> Goal visualization:
  │       └─> Progress toward weight loss goal (% complete, remaining kg)
  │
  ├─> Doctor Access
  │   ├─> Doctor views patient EHR from provider dashboard
  │   ├─> Sees:
  │   │   ├─> Vitals trends (same charts as patient)
  │   │   ├─> Medication adherence %
  │   │   ├─> Symptom patterns
  │   │   └─> Recent changes (highlighted)
  │   │
  │   └─> Doctor can make informed decisions:
  │       ├─> Adjust medication dosage
  │       ├─> Schedule follow-up consultation
  │       └─> Address side effects
  │
  └─> END: Continuous tracking, progress visible

DATA FLOW:
  Patient logs → EHR storage → Charts update → Doctor views → Decisions made
```

### Journey 5: Support & Communication

```
┌─────────────────────────────────────────────────────────────────┐
│              SUPPORT & COMMUNICATION JOURNEY                     │
└─────────────────────────────────────────────────────────────────┘

START: Patient needs support
  │
  ├─> Support Options Available:
  │   │
  │   ├─> OPTION 1: WhatsApp Support (<2 hour response guarantee)
  │   │   ├─> Patient clicks "Contact Support via WhatsApp"
  │   │   ├─> Opens WhatsApp Business chat (or in-app interface)
  │   │   ├─> Patient sends message:
  │   │   │   └─> "I'm experiencing nausea after starting medication"
  │   │   │
  │   │   ├─> Message routed to assigned doctor
  │   │   ├─> Doctor receives notification
  │   │   ├─> Doctor views message in provider dashboard
  │   │   ├─> Doctor responds (<2 hour target):
  │   │   │   └─> "Hi, nausea is common. Try taking medication with food..."
  │   │   │
  │   │   ├─> Patient receives WhatsApp response
  │   │   └─> Issue resolved or follow-up scheduled
  │   │
  │   ├─> OPTION 2: Educational Content
  │   │   ├─> Patient browses content library
  │   │   ├─> Finds relevant article:
  │   │   │   └─> "GLP-1 Side Effects: What to Expect"
  │   │   ├─> Reads article (contextual, educational)
  │   │   └─> Patient better informed
  │   │
  │   └─> OPTION 3: Schedule Consultation
  │       ├─> If issue urgent or complex
  │       ├─> Patient books consultation (physical or video)
  │       └─> Full consultation with doctor
  │
  ├─> Support Scenarios:
  │   │
  │   ├─> Side Effect Management (Common)
  │   │   ├─> Patient logs symptom via dashboard
  │   │   ├─> If severe (8+ severity):
  │   │   │   └─> System flags for doctor review
  │   │   ├─> Doctor receives notification
  │   │   ├─> Doctor responds via WhatsApp or schedules call
  │   │   └─> Issue addressed promptly
  │   │
  │   ├─> Medication Questions
  │   │   ├─> Patient asks via WhatsApp
  │   │   ├─> Doctor responds with guidance
  │   │   └─> Or directs to educational content
  │   │
  │   └─> Technical Issues (Video Consultation)
  │       ├─> Patient contacts support via WhatsApp
  │       ├─> Support team assists
  │       └─> Consultation rescheduled if needed
  │
  └─> END: Support provided, patient satisfied

RESPONSE TIME TRACKING:
  Message sent → System tracks time → Doctor responds → <2 hour target verified
```

### Journey 6: Subscription & Payment

```
┌─────────────────────────────────────────────────────────────────┐
│              SUBSCRIPTION & PAYMENT JOURNEY                     │
└─────────────────────────────────────────────────────────────────┘

START: Patient wants to subscribe
  │
  ├─> Pricing Page
  │   ├─> Views transparent pricing:
  │   │   ├─> Standard Plan: ₹3,500/month
  │   │   │   └─> Includes: Consultations, tracking, WhatsApp support
  │   │   └─> GLP-1 Plan: ₹6,000/month
  │   │       └─> Includes: Everything + GLP-1 therapy management
  │   │
  │   ├─> Feature comparison table
  │   ├─> Competitive comparison (vs. HealthifyRx, Veera)
  │   └─> CTA: "Subscribe Now"
  │
  ├─> Subscription Selection
  │   ├─> Patient selects plan (Standard or GLP-1)
  │   ├─> Payment method entry:
  │   │   ├─> Card details (card number, expiry, CVV)
  │   │   └─> Or UPI/Wallet (Razorpay supports Indian payment methods)
  │   │
  │   └─> Payment processing
  │       ├─> Razorpay API processes payment
  │       ├─> IF Success:
  │       │   ├─> Subscription activated
  │       │   ├─> Patient gains access to platform features
  │       │   ├─> Email confirmation sent
  │       │   └─> Renewal date set (start date + 1 month)
  │       │
  │       └─> IF Failure:
  │           ├─> Clear error message displayed
  │           └─> Patient can retry
  │
  ├─> Active Subscription
  │   ├─> Patient dashboard shows:
  │   │   ├─> Current plan (Standard/GLP-1)
  │   │   ├─> Next renewal date
  │   │   └─> Billing history
  │   │
  │   └─> Monthly Renewal (Automatic)
  │       ├─> System charges payment method on file
  │       ├─> IF Success:
  │       │   ├─> Subscription renewed
  │       │   ├─> Renewal date updated
  │       │   └─> Patient notified
  │       │
  │       └─> IF Failure:
  │           ├─> Subscription status → "past_due"
  │           ├─> Patient notified: "Payment failed, update payment method"
  │           ├─> Grace period (7 days) - patient retains access
  │           ├─> Retry attempts (Day 1, Day 3, Day 7)
  │           └─> IF Still fails: Subscription cancelled, access revoked
  │
  ├─> Plan Changes
  │   ├─> Upgrade (Standard → GLP-1):
  │   │   ├─> Takes effect immediately
  │   │   ├─> Pro-rated charge (difference for remaining days)
  │   │   └─> Patient gains GLP-1 features
  │   │
  │   └─> Downgrade (GLP-1 → Standard):
  │       ├─> Takes effect at end of billing period
  │       ├─> Pro-rated refund (difference for remaining days)
  │       └─> Patient retains GLP-1 features until period ends
  │
  ├─> Cancellation
  │   ├─> Patient clicks "Cancel Subscription"
  │   ├─> Options:
  │   │   ├─> Cancel immediately (pro-rated refund)
  │   │   └─> Cancel at end of period (retain access until end)
  │   │
  │   ├─> Confirmation email sent
  │   └─> Reactivation available within 30 days
  │
  └─> END: Subscription managed, payments processed

INTEGRATION POINTS:
  - Payment Gateway: Razorpay/Stripe India
  - Email/SMS: Confirmation and reminder notifications
  - Subscription Dashboard: Patient views subscription details
```

### Journey 7: Doctor Onboarding & Platform Setup

```
┌─────────────────────────────────────────────────────────────────┐
│              DOCTOR ONBOARDING & PLATFORM SETUP                  │
└─────────────────────────────────────────────────────────────────┘

START: Doctor interested in joining platform
  │
  ├─> Initial Contact
  │   ├─> Doctor contacts MetaboWell (email, phone, referral)
  │   ├─> Admin schedules onboarding call
  │   └─> Admin explains platform model, compensation, expectations
  │
  ├─> Application & Verification
  │   ├─> Doctor submits application:
  │   │   ├─> Personal information (name, email, phone)
  │   │   ├─> RMP registration number
  │   │   ├─> Specializations
  │   │   ├─> Years of experience
  │   │   ├─> Professional bio
  │   │   └─> Profile photo
  │   │
  │   ├─> Credential Verification
  │   │   ├─> Admin verifies RMP registration number
  │   │   ├─> Checks medical council database
  │   │   ├─> Validates specialization claims
  │   │   └─> Background check (if needed)
  │   │
  │   └─> IF Verified:
  │       └─> Doctor account created, credentials saved
  │
  ├─> Profile Setup
  │   ├─> Doctor logs in with credentials (sent via email)
  │   ├─> Completes profile:
  │   │   ├─> Uploads profile photo
  │   │   ├─> Reviews/edits bio
  │   │   ├─> Sets availability schedule (working hours, days)
  │   │   └─> Uploads digital signature (for prescriptions)
  │   │
  │   └─> Profile goes live → Visible in doctor marketplace
  │
  ├─> Platform Training
  │   ├─> Admin provides training:
  │   │   ├─> How to use video consultation platform
  │   │   ├─> How to access patient EHR
  │   │   ├─> How to generate prescriptions
  │   │   ├─> How to use voice-to-text notes
  │   │   ├─> How to respond to WhatsApp messages
  │   │   └─> Best practices for telemedicine
  │   │
  │   └─> Doctor completes training, ready for patients
  │
  ├─> First Patient Assignment
  │   ├─> Patient selects doctor from marketplace
  │   ├─> Doctor receives notification: "New patient assigned"
  │   ├─> Doctor can view patient profile (basic info)
  │   └─> Doctor ready for first consultation
  │
  └─> END: Doctor onboarded, active on platform

COMPENSATION MODEL:
  - Consultation fee: ₹1,000-₹1,500 per consultation (varies by location)
  - Commission: 30% goes to platform, 70% to doctor
  - Performance-based: Quality metrics tracked (patient satisfaction, response times)
```

### Journey 8: Lab Test Ordering & Results Journey

```
┌─────────────────────────────────────────────────────────────────┐
│          LAB TEST ORDERING & RESULTS JOURNEY                     │
└─────────────────────────────────────────────────────────────────┘

START: Patient needs lab test
  │
  ├─> Test Selection
  │   ├─> Patient navigates to "Order Lab Test" from dashboard
  │   ├─> Views lab test catalog:
  │   │   ├─> HbA1c Test
  │   │   ├─> Lipid Profile
  │   │   ├─> Thyroid Function Test
  │   │   ├─> Complete Blood Count (CBC)
  │   │   └─> Other metabolic tests
  │   │
  │   ├─> Each test shows:
  │   │   ├─> Test name and description
  │   │   ├─> Price
  │   │   ├─> Fasting requirements (if applicable)
  │   │   └─> Estimated results time
  │   │
  │   └─> Patient selects test(s) to order
  │
  ├─> Order Placement
  │   ├─> Address Selection
  │   │   ├─> Patient selects address for home visit
  │   │   ├─> Or adds new address
  │   │   └─> Confirms address details
  │   │
  │   ├─> Date/Time Selection
  │   │   ├─> Patient selects preferred date for sample collection
  │   │   ├─> Selects time slot (morning/afternoon)
  │   │   └─> System confirms availability
  │   │
  │   ├─> Payment
  │   │   ├─> System calculates total (test price + home visit charge if applicable)
  │   │   ├─> Patient enters payment details
  │   │   ├─> Payment processed (one-time payment, not subscription)
  │   │   └─> Payment confirmation received
  │   │
  │   └─> Order Confirmation
  │       ├─> Email/SMS/WhatsApp confirmation sent
  │       ├─> Order details: Test name, date, time, address
  │       ├─> Instructions: Fasting requirements, what to prepare
  │       └─> Order ID for tracking
  │
  ├─> Sample Collection Day
  │   ├─> [Day Before]
  │   │   └─> Reminder: "Your lab test is tomorrow. Remember to fast if required."
  │   │
  │   ├─> [Day Of]
  │   │   ├─> Lab technician arrives at patient's address
  │   │   ├─> Verifies patient identity
  │   │   ├─> Collects blood sample
  │   │   └─> Marks order status: "Sample collected"
  │   │
  │   └─> Order status updated: "Processing"
  │
  ├─> Results Processing
  │   ├─> Lab processes sample (1-3 days typically)
  │   ├─> IF Lab API Integration Available:
  │   │   ├─> Lab sends results via API/webhook
  │   │   ├─> System automatically parses results
  │   │   ├─> Results imported into patient EHR
  │   │   └─> Patient and doctor notified automatically
  │   │
  │   └─> IF Manual Upload (Fallback):
  │       ├─> Lab sends results PDF to patient (email/WhatsApp)
  │       ├─> Patient uploads PDF to platform
  │       ├─> System extracts data (or manual entry)
  │       └─> Results saved to EHR
  │
  ├─> Results Available
  │   ├─> Patient Notification
  │   │   ├─> Email/SMS/WhatsApp: "Your lab results are ready"
  │   │   └─> Link to view results in dashboard
  │   │
  │   ├─> Doctor Notification
  │   │   ├─> Assigned doctor receives notification
  │   │   └─> "Patient [Name]'s lab results available"
  │   │
  │   ├─> Results Display
  │   │   ├─> Patient views results in EHR dashboard
  │   │   ├─> Shows test values, reference ranges, interpretation
  │   │   ├─> Charts showing trends (if previous tests available)
  │   │   └─> Comparison to previous results (improvement/decline)
  │   │
  │   └─> Doctor Review
  │       ├─> Doctor views results in patient EHR
  │       ├─> Analyzes values, identifies concerns
  │       ├─> May schedule follow-up consultation
  │       └─> May adjust treatment plan based on results
  │
  └─> END: Lab test complete, results in EHR, doctor reviewed

INTEGRATION POINTS:
  - Lab Partner API: Automatic results import (preferred)
  - Manual Upload: Fallback if API unavailable
  - EHR Integration: Results automatically linked to patient record
```

### Journey 9: Prescription Refill Request & Approval

```
┌─────────────────────────────────────────────────────────────────┐
│         PRESCRIPTION REFILL REQUEST & APPROVAL                   │
└─────────────────────────────────────────────────────────────────┘

START: Patient needs prescription refill
  │
  ├─> Refill Request Initiation
  │   ├─> Patient views prescriptions from dashboard
  │   ├─> Finds prescription that needs refill
  │   ├─> Clicks "Request Refill" button
  │   │
  │   ├─> System Validation
  │   │   ├─> Checks if prescription is eligible for refill:
  │   │   │   ├─> Within validity period (not expired)
  │   │   │   ├─> Not exceeded refill limit (max 3 refills)
  │   │   │   └─> Prescription still active
  │   │   │
  │   │   ├─> IF Eligible:
  │   │   │   └─> Refill request created
  │   │   │
  │   │   └─> IF Not Eligible:
  │   │       ├─> Error message: "Prescription expired" or "Refill limit reached"
  │   │       └─> Suggestion: "Schedule consultation for new prescription"
  │   │
  │   └─> Confirmation: "Refill request submitted. Doctor will review shortly."
  │
  ├─> Doctor Notification
  │   ├─> Doctor receives notification:
  │   │   ├─> Email/SMS/WhatsApp: "Patient [Name] requested prescription refill"
  │   │   └─> Notification in provider dashboard
  │   │
  │   ├─> Doctor views refill request:
  │   │   ├─> Patient name
  │   │   ├─> Original prescription details (medications, dosage, date)
  │   │   ├─> Number of previous refills
  │   │   └─> Request date/time
  │   │
  │   └─> Doctor can access patient EHR:
  │       └─> Reviews patient progress, vitals, adherence before deciding
  │
  ├─> Doctor Decision
  │   │
  │   ├─> OPTION 1: Approve Refill
  │   │   ├─> Doctor clicks "Approve Refill" in provider dashboard
  │   │   ├─> System generates new prescription:
  │   │   │   ├─> Same medications and dosage as original
  │   │   │   ├─> Updated date (current date)
  │   │   │   └─> Linked to original prescription
  │   │   │
  │   │   ├─> Prescription delivered to patient:
  │   │   │   ├─> Via WhatsApp (PDF or link)
  │   │   │   ├─> Via Email (PDF attachment)
  │   │   │   └─> Available in dashboard
  │   │   │
  │   │   ├─> Patient Notification:
  │   │   │   └─> "Your prescription refill has been approved. View prescription here."
  │   │   │
  │   │   └─> Refill history updated
  │   │
  │   └─> OPTION 2: Deny Refill (Requires Consultation)
  │       ├─> Doctor clicks "Deny - Requires Consultation"
  │       ├─> Doctor may add note: "Please schedule consultation for review"
  │       ├─> Patient Notification:
  │       │   └─> "Doctor recommends consultation before refill. Book consultation here."
  │       │
  │       └─> Patient can book consultation to discuss refill
  │
  ├─> Refill History
  │   ├─> Patient can view refill history:
  │   │   ├─> Original prescription date
  │   │   ├─> Refill 1: Date approved
  │   │   ├─> Refill 2: Date approved
  │   │   └─> Refill 3: Date approved (limit reached)
  │   │
  │   └─> After limit reached:
  │       └─> "Refill limit reached. Schedule consultation for new prescription."
  │
  └─> END: Refill approved or consultation scheduled

AUTOMATION OPPORTUNITIES:
  - Auto-approve refills if patient adherence >90% and no concerns
  - Flag for doctor review if patient adherence <80% or symptoms reported
```

### Journey 10: Content Discovery & Learning Journey

```
┌─────────────────────────────────────────────────────────────────┐
│           CONTENT DISCOVERY & LEARNING JOURNEY                   │
└─────────────────────────────────────────────────────────────────┘

START: Patient wants to learn about metabolic health
  │
  ├─> Content Discovery Entry Points
  │   │
  │   ├─> OPTION 1: Navigation Bar
  │   │   ├─> Patient clicks "Learn" or "Resources" in navigation
  │   │   └─> Redirects to content library
  │   │
  │   ├─> OPTION 2: Dashboard Recommendations
  │   │   ├─> Dashboard shows "Recommended for you" section
  │   │   ├─> Based on patient's health profile (PCOS, diabetes, etc.)
  │   │   └─> "Read: PCOS and Weight Loss - What You Need to Know"
  │   │
  │   ├─> OPTION 3: Contextual Suggestions
  │   │   ├─> After consultation: "Learn more about GLP-1 therapy"
  │   │   ├─> When logging symptoms: "Read about managing side effects"
  │   │   └─> After lab results: "Understand your HbA1c results"
  │   │
  │   └─> OPTION 4: Search Engine (SEO)
  │       ├─> Patient searches Google: "GLP-1 India" or "diabetes reversal"
  │       ├─> MetaboWell article appears in search results
  │       └─> Patient clicks through to article
  │
  ├─> Content Library Browsing
  │   ├─> Content Library Page
  │   │   ├─> Shows articles and videos organized by category:
  │   │   │   ├─> GLP-1 Safety
  │   │   │   ├─> Obesity as Disease
  │   │   │   ├─> PCOS Management
  │   │   │   ├─> Diabetes Reversal
  │   │   │   ├─> Nutrition
  │   │   │   └─> Exercise
  │   │   │
  │   │   ├─> Search Bar: Patient can search by keyword
  │   │   ├─> Filter Options: Filter by category, content type (article/video)
  │   │   └─> Sort Options: Newest first, Most popular, Most relevant
  │   │
  │   └─> Content Cards Display:
  │       ├─> Thumbnail image
  │       ├─> Title
  │       ├─> Excerpt/preview
  │       ├─> Category tags
  │       ├─> Read time (for articles) or Duration (for videos)
  │       └─> Publish date
  │
  ├─> Content Consumption
  │   │
  │   ├─> Article Reading Experience
  │   │   ├─> Patient clicks article
  │   │   ├─> Article page loads:
  │   │   │   ├─> Title, author, publish date
  │   │   │   ├─> Table of contents (if long article)
  │   │   │   ├─> Article body (formatted, readable)
  │   │   │   ├─> Images, charts, diagrams
  │   │   │   └─> Estimated reading time
  │   │   │
  │   │   ├─> Reading Features:
  │   │   │   ├─> Share button (WhatsApp, email, social media)
  │   │   │   ├─> Print-friendly format
  │   │   │   └─> "Back to Library" navigation
  │   │   │
  │   │   └─> Related Articles:
  │   │       └─> "You might also like: [Related article titles]"
  │   │
  │   └─> Video Watching Experience
  │       ├─> Patient clicks video
  │       ├─> Video page loads:
  │       │   ├─> Embedded video player (YouTube/Vimeo)
  │       │   ├─> Title, description, category
  │       │   └─> Duration, view count
  │       │
  │       └─> Video Features:
  │           ├─> Playback controls
  │           ├─> Share functionality
  │           └─> Related videos section
  │
  ├─> Content Engagement
  │   ├─> Patient reads/watches content
  │   ├─> Learns about metabolic health topics
  │   ├─> May bookmark for later (future feature)
  │   ├─> May share with family/friends
  │   └─> Content analytics tracked (views, time spent, shares)
  │
  ├─> Action from Content
  │   ├─> Content may include CTAs:
  │   │   ├─> "Book a consultation to discuss this with your doctor"
  │   │   ├─> "Track your progress in your dashboard"
  │   │   └─> "Read related article: [Link]"
  │   │
  │   └─> Patient may take action:
  │       ├─> Schedule consultation based on learnings
  │       ├─> Start tracking vitals
  │       └─> Ask doctor questions via WhatsApp
  │
  └─> END: Patient educated, better informed about metabolic health

CONTENT TYPES:
  - Educational Articles: GLP-1 safety, obesity as disease, PCOS management
  - Video Content: Doctor explanations, patient testimonials, educational videos
  - Infographics: Visual guides for medication, diet, exercise
  - FAQs: Common questions answered
```

### Journey 11: Account Recovery & Password Reset

```
┌─────────────────────────────────────────────────────────────────┐
│          ACCOUNT RECOVERY & PASSWORD RESET JOURNEY               │
└─────────────────────────────────────────────────────────────────┘

START: Patient forgot password or locked out
  │
  ├─> Login Page
  │   ├─> Patient attempts to login
  │   ├─> Enters email/phone
  │   ├─> Enters incorrect password (or forgot password)
  │   └─> Clicks "Forgot Password?" link
  │
  ├─> Password Reset Request
  │   ├─> Password Reset Page
  │   │   ├─> Patient enters email or phone number
  │   │   ├─> Clicks "Send Reset Link"
  │   │   │
  │   │   ├─> System Validation:
  │   │   │   ├─> Checks if email/phone exists in system
  │   │   │   ├─> IF Found:
  │   │   │   │   ├─> Generates secure reset token
  │   │   │   │   ├─> Stores token with expiration (24 hours)
  │   │   │   │   ├─> Sends reset email/SMS with link
  │   │   │   │   └─> Confirmation: "Reset link sent to your email/phone"
  │   │   │   │
  │   │   │   └─> IF Not Found:
  │   │   │       └─> Generic message: "If account exists, reset link sent" (security)
  │   │   │
  │   │   └─> Rate Limiting:
  │   │       └─> Prevents abuse (max 3 reset requests per hour)
  │   │
  │   └─> Email/SMS Sent
  │       ├─> Reset email includes:
  │       │   ├─> Secure reset link (with token)
  │       │   ├─> Expiration notice (24 hours)
  │       │   └─> Security warning: "If you didn't request this, ignore this email"
  │       │
  │       └─> SMS includes:
  │           └─> Reset link or OTP code
  │
  ├─> Password Reset Process
  │   ├─> Patient clicks reset link from email/SMS
  │   ├─> Reset Page Loads
  │   │   ├─> System validates token:
  │   │   │   ├─> Checks token exists and not expired
  │   │   │   ├─> IF Valid:
  │   │   │   │   └─> Shows password reset form
  │   │   │   │
  │   │   │   └─> IF Invalid/Expired:
  │   │   │       ├─> Error: "Reset link expired or invalid"
  │   │   │       └─> Option to request new reset link
  │   │   │
  │   │   ├─> Password Reset Form:
  │   │   │   ├─> Enter new password
  │   │   │   ├─> Confirm new password
  │   │   │   ├─> Password strength indicator
  │   │   │   └─> "Reset Password" button
  │   │   │
  │   │   └─> Password Validation:
  │   │       ├─> Minimum 8 characters
  │   │       ├─> Complexity requirements (letters, numbers, special chars)
  │   │       └─> Cannot be same as previous password
  │   │
  │   └─> Password Updated
  │       ├─> System hashes new password (bcrypt)
  │       ├─> Updates password in database
  │       ├─> Invalidates reset token (one-time use)
  │       ├─> Invalidates all existing sessions (security measure)
  │       ├─> Success message: "Password reset successfully"
  │       └─> Redirects to login page
  │
  ├─> Account Recovery (Locked Account)
  │   ├─> IF Account Locked (too many failed login attempts):
  │   │   ├─> Patient sees: "Account temporarily locked. Try again in 30 minutes"
  │   │   ├─> OR: "Account locked. Please reset password or contact support"
  │   │   │
  │   │   ├─> Support Contact:
  │   │   │   ├─> "Contact Support" button
  │   │   │   ├─> Opens WhatsApp support or email form
  │   │   │   └─> Patient can request account unlock
  │   │   │
  │   │   └─> Admin can unlock account:
  │   │       └─> After verifying identity (security questions or ID verification)
  │   │
  │   └─> Account Unlocked
  │       ├─> Patient receives notification
  │       └─> Can login with password reset or existing password
  │
  └─> END: Password reset, account accessible

SECURITY MEASURES:
  - Reset tokens expire in 24 hours
  - Tokens are one-time use only
  - Rate limiting prevents abuse
  - All sessions invalidated after password reset
  - Audit log tracks password reset attempts
```

### Journey 12: Free Metabolic Health Assessment (Lead Generation)

```
┌─────────────────────────────────────────────────────────────────┐
│       FREE METABOLIC HEALTH ASSESSMENT JOURNEY                   │
└─────────────────────────────────────────────────────────────────┘

START: Potential patient discovers MetaboWell
  │
  ├─> Landing Page Entry
  │   ├─> Patient visits MetaboWell website
  │   ├─> Sees value proposition:
  │   │   ├─> "Your metabolic health partner for life"
  │   │   ├─> "Doctor-led care, not just an app"
  │   │   └─> Trust-building elements (doctor credentials, testimonials)
  │   │
  │   └─> Prominent CTA: "Book Free Assessment" (₹1,500 value)
  │
  ├─> Free Assessment Booking
  │   ├─> Patient clicks "Book Free Assessment"
  │   ├─> Quick Registration (Lightweight)
  │   │   ├─> Collects minimal data:
  │   │   │   ├─> Name
  │   │   │   ├─> Email or phone
  │   │   │   ├─> Age
  │   │   │   └─> Primary health concern (quick dropdown)
  │   │   │
  │   │   └─> NOT full onboarding (deferred until after assessment)
  │   │
  │   ├─> Assessment Scheduling
  │   │   ├─> Shows available assessment slots (next 7 days)
  │   │   ├─> Patient selects date/time
  │   │   ├─> Selects consultation type:
  │   │   │   ├─> Physical (if Vizag) - builds trust
  │   │   │   └─> Video (if other location) - convenience
  │   │   │
  │   │   └─> Confirms booking (no payment required)
  │   │
  │   └─> Booking Confirmation
  │       ├─> Email/SMS/WhatsApp confirmation:
  │       │   ├─> "Your free assessment is scheduled"
  │       │   ├─> Date, time, doctor name
  │       │   ├─> Location (clinic address) or video link
  │       │   └─> What to bring (previous reports, medications list)
  │       │
  │       └─> Calendar integration (add to calendar)
  │
  ├─> Pre-Assessment Preparation
  │   ├─> [24 Hours Before]
  │   │   └─> Reminder: "Your free assessment is tomorrow. Prepare your medical history."
  │   │
  │   └─> [Day Of]
  │       └─> Final reminder: "Your assessment is in 2 hours"
  │
  ├─> Assessment Consultation
  │   ├─> Consultation Begins
  │   │   ├─> Doctor conducts 30-minute assessment:
  │   │   │   ├─> Reviews patient's health history
  │   │   │   ├─> Discusses goals and concerns
  │   │   │   ├─> Explains metabolic health approach
  │   │   │   ├─> Answers questions about GLP-1, treatment options
  │   │   │   └─> Provides initial recommendations
  │   │   │
  │   │   └─> Doctor documents assessment notes
  │   │
  │   └─> Assessment Ends
  │       ├─> Doctor provides summary
  │       └─> Next steps discussed
  │
  ├─> Post-Assessment Conversion
  │   ├─> Assessment Summary
  │   │   ├─> Patient receives assessment summary:
  │   │   │   ├─> Health assessment findings
  │   │   │   ├─> Recommended treatment approach
  │   │   │   ├─> Next steps
  │   │   │   └─> Pricing information (transparent)
  │   │   │
  │   │   └─> Available in dashboard
  │   │
  │   ├─> Conversion Prompt
  │   │   ├─> Dashboard shows:
  │   │   │   ├─> "Complete your profile to continue your journey"
  │   │   │   ├─> "Subscribe to start your metabolic health program"
  │   │   │   └─> "Your assessment doctor: Dr. [Name]"
  │   │   │
  │   │   └─> Clear CTA: "Start Your Journey" or "Subscribe Now"
  │   │
  │   ├─> Conversion Flow
  │   │   ├─> IF Patient converts:
  │   │   │   ├─> Completes full onboarding (Epic 1)
  │   │   │   ├─> Doctor assigned (assessment doctor becomes assigned doctor)
  │   │   │   ├─> Subscribes to plan
  │   │   │   └─> Begins regular consultations
  │   │   │
  │   │   └─> IF Patient doesn't convert:
  │   │       ├─> Assessment data saved
  │   │       ├─> Follow-up email/SMS in 3 days, 7 days
  │   │       └─> "Ready to start? Complete your profile here"
  │   │
  │   └─> Conversion Tracking
  │       ├─> System tracks conversion rate
  │       ├─> Target: 30-40% conversion (free assessment → paid subscription)
  │       └─> Analytics: Which doctors have higher conversion rates
  │
  └─> END: Patient converted or in follow-up sequence

CONVERSION OPTIMIZATION:
  - Assessment doctor becomes assigned doctor (continuity)
  - Assessment summary reinforces value
  - Transparent pricing reduces friction
  - Follow-up sequence for non-converters
```

---

## Checklist Results Report

### Executive Summary

**Overall PRD Completeness:** ~90%  
**MVP Scope Appropriateness:** Just Right  
**Readiness for Architecture Phase:** Nearly Ready  
**Most Critical Gaps:** PRD needs to be written to file; user journey flows could be more explicitly mapped

### Category Analysis Table

| Category                         | Status | Critical Issues |
| -------------------------------- | ------ | --------------- |
| 1. Problem Definition & Context  | PASS   | Well documented in brief.md and referenced in PRD |
| 2. MVP Scope Definition          | PASS   | Clear MVP scope with 18 core features |
| 3. User Experience Requirements  | PARTIAL| User journeys could be more explicitly mapped |
| 4. Functional Requirements       | PASS   | Comprehensive with clear acceptance criteria |
| 5. Non-Functional Requirements   | PASS   | Comprehensive NFRs covering all aspects |
| 6. Epic & Story Structure        | PASS   | Well-structured epics and stories |
| 7. Technical Guidance            | PASS   | Comprehensive technical assumptions |
| 8. Cross-Functional Requirements | PASS   | Data, integration, operational requirements covered |
| 9. Clarity & Communication       | PARTIAL| Content well-structured but needs file output |

### Top Issues by Priority

**BLOCKERS (Must fix before architect can proceed):**
- None major, but PRD needs to be written to file for architect access

**HIGH PRIORITY (Should fix for quality):**
1. User journey flows could be more explicitly mapped (Section 3.1)
2. Some integration details need clarification (lab API availability, WhatsApp exact workflow)
3. Data schema changes should be tied more explicitly to stories requiring them

**MEDIUM PRIORITY (Would improve clarity):**
1. Edge cases in user flows could be documented
2. Error handling approaches could be more detailed per feature
3. Timeline estimates per epic would help planning

**LOW PRIORITY (Nice to have):**
1. More detailed diagrams/visuals
2. More competitive feature comparison details

### MVP Scope Assessment

- **Scope is appropriate:** 18 core features, clear out-of-scope items
- **Epic breakdown supports 6-month MVP timeline**
- **Stories are appropriately sized** for development (2-4 hour execution)
- **Some complexity concerns:** Video platform integration, WhatsApp API, Lab integrations may need technical spikes

### Technical Readiness

- **Clear technical constraints documented**
- **Technical risks identified** (regulatory compliance, integrations)
- **Areas needing investigation:** Lab API availability, WhatsApp Business API setup, video platform reliability

### Recommendations

1. **Write PRD to file (docs/prd.md)** for architect access - CRITICAL
2. Create explicit user journey flow diagrams/maps for primary flows (onboarding, consultation booking, EHR access)
3. Clarify integration assumptions (lab API availability, WhatsApp exact workflow)
4. Add timeline estimates per epic for planning (optional but helpful)
5. Document edge cases for critical flows (payment failures, consultation cancellations, etc.)

### Final Decision

**NEARLY READY** - The PRD is comprehensive and well-structured. Main gap is that it needs to be written to file. Once written and minor clarifications added, it will be **READY FOR ARCHITECT**.

---

## Next Steps

### UX Expert Prompt

Create the UX design architecture for MetaboWell based on this PRD. Focus on:
- User journey flows for primary use cases (onboarding, doctor selection, consultation booking, EHR access)
- Detailed wireframes for core screens (12 screens identified)
- Design system aligned with branding guidelines (science-led healthcare positioning)
- Accessibility compliance (WCAG AA)
- Mobile-responsive design patterns

Use this PRD as the source of truth for requirements and user needs.

### Architect Prompt

Create the technical architecture for MetaboWell based on this PRD. Focus on:
- System architecture (modular monolith → microservices evolution)
- Database schema design (EHR, users, consultations, subscriptions)
- API design (RESTful, authentication, authorization)
- Third-party integrations (payment, video, WhatsApp, lab APIs)
- Security architecture (DISHA compliance, encryption, audit logs)
- Deployment architecture (AWS/GCP, scaling, monitoring)

Use this PRD as the source of truth for technical requirements and constraints.

---

**Document Status:** Ready for Architecture Phase  
**Owner:** John (PM)  
**Next Review:** After architecture phase completion

