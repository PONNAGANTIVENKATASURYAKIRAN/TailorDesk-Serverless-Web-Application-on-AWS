Lakshmi Devi Ladies Tailors — Serverless Management Portal
----------------------------------------------------------
A full-stack, responsive web application and workshop ledger built for a bespoke tailoring boutique located in Guntur, Andhra Pradesh. The application features a 3-step customer consultation flow, dynamic catalog browsing, bilingual English/Telugu localization, automated order dispatch via WhatsApp, worker piece-rate payroll calculations, and an owner administration dashboard.
Architecture Overview
---------------------

[ Customer / Owner Browser ]
             │
             │ HTTPS (Encrypted Edge Delivery)
             ▼
    [ Amazon CloudFront ]
             │
             │ Static Hosting (Origin)
             ▼
      [ Amazon S3 ] (index.html, style.css)
             │
             │ REST API Calls (CORS Enabled)
             ▼
   [ Amazon API Gateway ] (/customers, /workers, /catalog, /feedback)
             │
             ├──────────────────────────┬──────────────────────────┐
             ▼                          ▼                          ▼
 [ TailorCustomerCatalogHandler ]  [ TailorWorkerHandler ]  [ Amazon SNS ]
             │                          │                  (Transactional SMS)
             ├──────────────────────────┤
             ▼                          ▼
    [ Amazon DynamoDB ]        [ Amazon DynamoDB ]
   (TailorCustomers,          (TailorWorkerLedger)
    TailorCatalog,
    TailorFeedback)

Componets brakdown
