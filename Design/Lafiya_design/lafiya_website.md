# Lafiya AI Website Integration Plan

This document outlines the step-by-step plan for structuring the new Lafiya web page on the existing `c-mindcare-site` Astro codebase, highlighting the Cloud version and offering the Offline Download as a fallback.

## Step 1: Verification of Cloud Deployment
The Cloud version of Lafiya AI is already successfully deployed on Google Cloud. We will simply need the direct URL for this hosted service so we can link it as the primary call-to-action on the new webpage. 

*(Note: The Android APK fallback is also prepared and will be linked as a secondary option.)*

## Step 2: Create the `lafiya.astro` Page
The `c-mindcare-site` is built using [Astro](https://astro.build/) and Tailwind CSS. We will create a dedicated landing page at `src/pages/lafiya.astro`, which will resolve to `https://c-mindcare.com/lafiya`.

### Proposed Layout for the Page:
* **Hero Section**: A strong headline ("Lafiya AI: Clinical Decision Support for Primary Care") with a high-quality split-screen image or graphic showing both the cloud dashboard and the app running on an Android tablet.
* **What is Lafiya?**: A brief, non-technical explanation of the AI engine, emphasizing its dual capability (cloud-first, with offline edge fallback using the knowledge graph).
* **How it Works (The 3 Steps)**:
  1. **Intake**: Gather patient vitals and symptoms fast.
  2. **Diagnose**: The AI suggests evidence-based differentials.
  3. **Treat**: Review Nigerian Standing Orders treatment guidelines contextually.
* **Primary CTA (Cloud URL)**: A large, prominent, distinctly colored button: "Use Lafiya Online Now". This button will link directly to the deployed Google Cloud web service.
* **Secondary CTA (Download Option)**: A smaller or outlined button just below the main CTA: "Download Lafiya for Android Tablet (Offline .apk)". This provides the fallback option for clinics with poor connectivity.
* **Installation Guide (Collapsible or Footnote)**: A short, non-intrusive blurb or collapsible section under the secondary button explaining how to install an APK on Android ("Allow apps from unknown sources").

## Step 3: Update C-Mindcare Navigation
Once the page looks perfect, we will update the global navigation components to ensure visitors can discover it naturally.

1. **Update Header**: We will modify `src/components/Header.astro` and add "Lafiya AI" to the top navigation bar.
2. **Update Footer**: We will modify `src/components/Footer.astro` to include a link to the new `/lafiya` page under the relevant footer section.

### Summary
This approach keeps the primary `c-mindcare-site` website fast and clean while immediately guiding users to the preferred cloud-hosted Lafiya service. By retaining the Google Cloud-hosted offline APK as a secondary fallback, you seamlessly cater to both well-connected and connectivity-restricted clinics.
