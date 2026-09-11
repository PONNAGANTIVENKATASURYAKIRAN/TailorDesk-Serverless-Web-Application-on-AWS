**TailorDesk – Tailoring Studio Management Portal**
---------------------------------------------------
A serverless web application and administrative ledger designed for Lakshmi Devi Ladies Tailors & Boutique (Guntur, AP). It provides a responsive booking catalog for customers and a real-time order intake and worker productivity tracker for shop owners.

**Key Features**
----------------
**Interactive Customer Booking Flow:** 3-step service selection, custom alteration notes, dress previews, and direct WhatsApp order dispatch.

**Smart Customer Memory:** Recognizes returning clients by phone number to eliminate duplicates and streamline repeat bookings.

**Owner Kanban Board:** Real-time customer pipeline categorized by order stage (Reached to Stitching, Selected but Not Now, and Just Browsed).

**Worker Ledger & Payout Settlement:** Tracks daily stitched pieces, calculates shop profit per garment, and handles one-click balance settlements with worker privacy modes.

**Bilingual UI**: Instant switching between English and Telugu across all customer touchpoints.

**Customer Feedback System:** In-app rating and review capture with moderation/deletion support in the admin panel.

**System Architecture**
------------------------

**Tech Stack**
--------------
**Frontend:** Vanilla HTML5, CSS3 (Mobile-first responsive design), JavaScript (ES6 Fetch API)

**Hosting & CDN:** Amazon S3, AWS CloudFront

**API Layer:** Amazon API Gateway (Lambda Proxy Integration)

**Compute:** AWS Lambda (Python 3.12)

**Database:** Amazon DynamoDB (On-Demand Capacity)

**Security & Auth:** Email/PIN administrative authentication, IAM policy enforcement, HTTPS termination via CloudFront
