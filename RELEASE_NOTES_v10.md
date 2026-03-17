# CYOND Worker App - Release Notes v10

Release date: 2026-03-17
Base: v9

## Highlights

- Added Rule-Out Method workflow tab before Inspection Comments in checklist flow.
- Added backend APIs to fetch and update Rule-Out Method data per lead.
- Added persistence for Rule-Out Method data on leads via `rollout_method_data`.
- Added dedicated Rule-Out Method rendering block in checklist PDFs.
- Fixed quotation PDF address layout overlap issues with dynamic flow rendering.
- Improved quotation and checklist visual styling with section-based themes.
- Clarified Rule-Out YES/NO and OPEN/CLOSED question text in checklist PDF.
- Cleaned checklist table labels and removed noisy bracket prefixes.
- Improved contact/feedback table content and made Google Rating conditional on real user input.
- Updated toast notification behavior to display clearly at the top for better visibility.
- Optimized Android release build for smaller artifacts.

## Backend

- Updated `cyond_node-master/controllers/App/appInspectionController.js`
- Updated `cyond_node-master/controllers/App/appUserController.js`
- Updated `cyond_node-master/controllers/App/newPdfController.js`
- Updated duplicate controller tree under `cyond_node-master/controllers/controllers/App/`
- Added migration: `cyond_node-master/migrations/add_rollout_method_data_to_leads.js`
- Updated routes: `cyond_node-master/routes/app/appInspectionRoutes.js`
- Updated model: `cyond_node-master/models/Lead.js`

## Flutter

- Added `lib/screens/inspection_tabs/rollout_method_tab.dart`
- Updated checklist tab ordering and navigation indices.
- Added rollout API constants and service methods.
- Updated toast utility positioning.

## Build / Size Optimization

- Enabled Android release minification and resource shrinking.
- Added `android/app/proguard-rules.pro`.
- Generated split APK and AAB artifacts with obfuscation and split debug info.

## Notes

- Existing S3 PDFs are immutable; regenerate PDFs to reflect v10 formatting changes.
