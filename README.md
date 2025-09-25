# Android App Similarity Evaluation

This repository provides tools, sample app pairs, and guidelines for **manual verification of app similarity**.  
It is designed for researchers and developers working on application similarity detection.

---

## Repository Structure

```
/samples
  ├── pair_001/
  │   ├── app_A.apk
  │   ├── app_B.apk
  ├── pair_002/
  │   ├── app_A.apk
  │   ├── app_B.apk
  ...
/tools
  └── emulator_setup_guide.md
```

- **/samples/**: Contains detected similar app pairs. Each folder includes two APKs (`app_A.apk`, `app_B.apk`).
- **/tools/**: Provides supporting materials, such as emulator setup guides or helper scripts.

---

##  Environment Setup

1. **Install Android Studio** or use the [Android Emulator](https://developer.android.com/studio/run/emulator).  

   - Recommended Android version: **Android 11 (API 30)** or later.  
   - Ensure Google Play Services are available for apps requiring authentication.  

2. **Set up an emulator**:

   - Create an emulator with at least **2 GB RAM, 2 vCPUs**.

   - Resolution: **1080×1920** (for consistent UI observation).

   - Install apps via:

     ```bash
     adb install path/to/app_A.apk
     adb install path/to/app_B.apk
     ```

3. **(Optional)** Use a physical Android device for more realistic performance and interaction.

---

##  Running the Evaluation

For each pair in `/samples/`:

### Step 1: App Launch

- Observe splash screens, icons, and initial UI layout.  
- Note similarities in color themes, logos, or branding.

### Step 2: Navigation & UI Structure

- Explore major screens (home, menu, settings, etc.).  
- Compare navigation flows (tabs, drawers, bottom navigation).  

### Step 3: Core Features

- Identify the **main functionality** of each app.  
- Run equivalent tasks (e.g., login, search, media playback).  
- Note if flows and results are highly similar.  

### Step 4: Resource Elements

- Check reused icons, images, or text content.  
- Look for identical layouts or widget arrangements.  

### Step 5: Interaction & Behavior

- Interact with buttons, forms, and gestures.  
- Compare response times, error messages, and animations.  

---

##  Verification Questions

After running both apps, please answer the following:

1. Do both apps provide the **same primary functionality**?  
2. Are the **UI layouts** and navigation flows largely identical?  
3. Do the apps reuse **icons, images, or textual resources**?  
4. Are the **interactions and behaviors** (e.g., login flow, search results) similar?  
5. Based on your observation, would you classify the pair as **similar applications**?  
