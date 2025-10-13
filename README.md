# Android App Similarity Evaluation

This repository provides tools, sample app pairs, and guidelines for **manual verification of app similarity**.  
It is designed for researchers and developers working on application similarity detection.

APK samples are **not included in this repository**.  
They are hosted on Hugging Face:

 [Hugging Face — zhuowu / Similar_Apps](https://huggingface.co/datasets/zhuowu/Similar_Apps/tree/main)

After downloading, organize them into cluster folders under `/samples/`:
---

## Repository Structure

```
/samples
  ├── cluster_001/
  │   ├── app_001.apk
  │   ├── app_002.apk
  │   ├── app_003.apk
  ├── cluster_002/
  │   ├── app_001.apk
  │   ├── app_002.apk
  ...
/tools
  └── emulator_setup_guide.md
```

- **/samples/**: Contains clusters of potentially similar applications.  
  Each cluster folder includes **two or more APKs**.  
- **/tools/**: Provides supporting materials, such as emulator setup guides or helper scripts.

---

## Environment Setup

1. **Install an Android Emulator** (choose one of the following options):  
   - [Android Studio Emulator (official)](https://developer.android.com/studio/run/emulator)  
   - [LDPlayer Emulator](https://www.ldmnq.com/)  
   - (Optional) Other third-party emulators such as [BlueStacks](https://www.bluestacks.com/)  

   > Note: For research reproducibility, we recommend using **Android Studio Emulator** first.  
   > Third-party emulators may differ in performance or compatibility.

2. **Set up an emulator**:

   - Create an emulator with at least **2 GB RAM, 2 vCPUs**.

   - Resolution: **1080×1920** (for consistent UI observation).

   - Install apps via:

     ```bash
     adb install path/to/app_001.apk
     adb install path/to/app_002.apk
     ```

3. **(Optional)** Use a physical Android device for more realistic performance and interaction.

---

##  Running the Evaluation

For each cluster in `/samples/`:

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

##  Verification Submission

After running both apps, please submit your evaluation result as a **GitHub Issue**.

### How to Submit

1. Go to the repository's [Issues page](../../issues).
2. Click **New Issue** → choose **App Similarity Verification**.
3. Fill in the form with the following information:
   - Pair ID (e.g., cluster_001)
   - App 001 / App 002 info
   - Answers to the similarity checks (UI, functionality, resources, etc.)
   - Your final decision (e.g., Highly Similar / Weakly Similar / Not Similar)

We provide a standardized issue form in  
`.github/ISSUE_TEMPLATE/verification.yml`  
so all results follow the same structure.


## Example of Similar Apps

The following are sample app pairs from the dataset that exhibit notable similarity in UI design, layout, and functionality.

| App Pair | Screenshots |
|:--:|:--:|
| **Cluster 001** | <img src="docs/examples/cluster_001.png" width="400"/> |
