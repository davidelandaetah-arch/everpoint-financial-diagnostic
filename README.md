# EverPoint Financial Diagnostic MVP

Static bilingual MVP for the **EverPoint Financial Readiness Score™**.

## What it does

- Matches EverPoint's current navy/gold premium financial-services look.
- Spanish / English toggle.
- One-question-at-a-time guided diagnostic.
- Conditional business questions.
- Calculates three educational/internal indicators:
  - Credit Readiness
  - Business Foundation
  - Funding Readiness
- Routes the user toward:
  - Credit evaluation
  - Business funding application
  - Business credit / formation consultation
  - General consultation
- Uses EverPoint's current LeadConnector forms and booking URL.
- Does **not** request SSN, banking credentials or perform a credit pull.

## Files

`index.html` contains the complete MVP and can be deployed as a static site.

## Publish free with GitHub Pages

1. Create a GitHub repository.
2. Upload `index.html`.
3. Go to **Settings → Pages**.
4. Select deployment from the main branch/root.
5. GitHub will provide the public URL.
6. Add that URL as the destination of a button on EverPoint's website.

For a branded domain/subdomain, configure DNS after the initial test.

## Important before production

This MVP intentionally keeps the scoring algorithm simple and transparent for testing. Before using it as a production lead-qualification system:

- validate scoring thresholds against EverPoint's real funding criteria;
- confirm compliance language with EverPoint's legal/compliance advisor;
- connect lead capture to GoHighLevel/LeadConnector through a secure backend/webhook rather than exposing private API credentials in browser code;
- add consent language required for SMS/email follow-up;
- add analytics and conversion tracking;
- verify all links and service names.

## Current CTA links

- Consultation booking:
  `https://api.leadconnectorhq.com/widget/booking/Jo2itL8ZeS6S68rKyyFm`
- Credit repair/application form:
  `https://api.leadconnectorhq.com/widget/form/hXr9MAZMR8AHID3LC5cg`
- Funding application:
  `https://api.leadconnectorhq.com/widget/form/tvJ4AjmdXHVnOmm8DyEk`

## Next recommended version

V1.1 should push the diagnostic result into GoHighLevel automatically with fields/tags such as:

- `diagnostic_score`
- `credit_readiness`
- `business_foundation`
- `funding_readiness`
- `recommended_service`
- `lead_priority`
- `diagnostic_language`

That integration should be done server-side so CRM credentials are never exposed in the browser.
