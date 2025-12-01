# Company-Posture-Assessment-page


The TBO Secure Assessment Platform is an end-to-end business maturity evaluation system combining a fully client-side scoring engine, dynamic PDF generation, and automated report delivery through Supabase Edge Functions and MailerSend.
It provides a modern, branded, privacy-focused assessment experience designed for lead generation, internal visibility, and instant personalized reporting.

Key Features
Interactive Assessment Engine

Category-based questionnaire system.

Progress tracking and step indicators.

Accessible tooltips and responsive layout.

Smooth transitions and animations.

All scoring is processed locally on the user’s device for maximum privacy.

Dynamic PDF Report Generation

Powered by html2pdf, jsPDF, html2canvas, and Chart.js.

Multi-page branded PDF output.

Includes category analysis, weighted scoring, and recommendations.

Fully client-side generation (no backend processing).

Email Gate & Lead Capture

Before generating or downloading the report, users submit:

Company name

Work email

The platform:

Sends the PDF report to the user automatically.

Logs the submission to the Supabase leads table.

Automated Email Delivery

A Supabase Edge Function receives the PDF as Base64.

Sends a branded HTML email to the user via MailerSend.

Stores the lead entry (email, company, timestamp) in the database.

Admin / Tech Team Notification Email

Every submission triggers a second internal email containing:

Company name

Email address

Assessment category

Final assessment score

Timestamp

Internal download link to the PDF report

Designed so the technical team has full visibility into inbound activity.

Modern UI Implementation

The front-end includes:

Animated loaders and modal flows.

Glass-style card components and branded gradients.

Mobile-responsive layouts.

Smooth question transitions.

Accessibility-friendly interactions and ARIA usage.

Dark-Mode Safe Email Templates

Both user and admin emails include anti-dark-mode CSS to prevent Gmail/Outlook color inversion and maintain brand consistency across clients.

Tech Stack
Front-End

HTML, CSS, JavaScript (no frameworks)

Chart.js

html2pdf.js

jsPDF

html2canvas

Backend

Supabase Edge Functions (Deno)

Database

Supabase Postgres (leads table)

Email Delivery

MailerSend API

Optional Storage

Supabase Storage for saving reports or logs

Project Goals

Provide companies with a personalized business maturity assessment and roadmap.

Deliver instant, branded PDF reports directly to users.

Create a reliable lead-generation channel with internal visibility.

Maintain strict privacy by keeping all assessment answers client-side.

Build a polished, modern UI that reflects TBO’s brand identity.
