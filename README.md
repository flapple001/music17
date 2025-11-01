# Music17 — One-Click MP3 Player (Android)

This repository contains a ready-to-upload Android Studio project skeleton for **Music17**,
a minimal, one-click MP3 player. It also includes a GitHub Actions workflow that will
build a debug APK automatically when pushed to GitHub.

**Important:** This package does **not** contain a prebuilt APK (I can't build APKs inside this chat),
but if you upload this repository to GitHub and enable Actions, the workflow will produce an APK artifact
you can download — no coding required.

## Steps to get an APK (3 simple steps)

1. Create a new **private** or **public** repository on GitHub.
2. Upload the contents of this repository (zip upload or push via git).
3. Go to the repository's "Actions" tab; the `android-build.yml` workflow will run and produce an artifact.
   Download the `app-debug.apk` artifact from the workflow run.

If you want a signed release APK, I included instructions in `SIGNING.md`.

