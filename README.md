# Personal Rclone Drive Sync - OAuth Consent & Pages Portal

This repository hosts the static application home page, privacy policy, and terms of service required by Google Cloud Platform (GCP) when registering a custom OAuth 2.0 Client ID for [Rclone](https://rclone.org/).

## 🌐 Live URLs

Once published on GitHub Pages:

* **Application Home Page:** `https://nanobrad.github.io/rclone-oauth/`
* **Privacy Policy URL:** `https://nanobrad.github.io/rclone-oauth/privacy.html`
* **Terms of Service URL:** `https://nanobrad.github.io/rclone-oauth/terms.html`
* **Authorized Domain:** `github.io`

---

## 🛠️ Google Cloud Console OAuth Setup Guide

### 1. Configure the OAuth Consent Screen
1. Go to the [Google Cloud Console](https://console.cloud.google.com/apis/credentials/consent).
2. Choose **External** user type and click **Create**.
3. Fill in the App Information:
   * **App Name:** `Personal Rclone Drive Sync`
   * **User Support Email:** `nanobrad@gmail.com`
   * **Application Home Page:** `https://nanobrad.github.io/rclone-oauth/`
   * **Application Privacy Policy link:** `https://nanobrad.github.io/rclone-oauth/privacy.html`
   * **Application Terms of Service link:** `https://nanobrad.github.io/rclone-oauth/terms.html`
   * **Authorized Domains:** Add `github.io`
   * **Developer Contact Information:** `nanobrad@gmail.com`
4. Click **Save and Continue**.
5. Under **Scopes**, click **Add or Remove Scopes** and add:
   * `.../auth/drive` (Full access) or `.../auth/drive.file`
6. Under **Test Users**, add your personal Google email address (`nanobrad@gmail.com`).

### 2. Create OAuth Credentials
1. Go to **APIs & Services > Credentials**.
2. Click **Create Credentials > OAuth client ID**.
3. Choose **Desktop app** (or TV and Limited Input devices).
4. Name it (e.g., `Rclone Desktop Client`).
5. Copy the generated **Client ID** and **Client Secret**.

### 3. Use in Rclone
Run `rclone config`:
* Select your Google Drive remote (or create a new one).
* Paste your custom **Client ID** and **Client Secret**.
* Complete the authorization in your browser.
