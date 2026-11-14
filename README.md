# Mission Kerala: get the APK

This folder is a ready Android project. GitHub builds the APK for you in the cloud, so you do not need Android Studio. It takes about 10 minutes and is free.

## Build the APK

1. Sign in at github.com (free account), then click **New repository**. Name it `mission-kerala` and click **Create repository**.
2. On the new repository page, click **uploading an existing file**.
3. Unzip this folder on your computer. Select everything inside it (including the hidden `.github` folder) and drag it into the upload box. Click **Commit changes**.
   - Check that the repository now shows `www`, `assets`, `package.json` and a `.github` folder.
   - If `.github` did not upload: click **Add file > Create new file**, type `.github/workflows/build-apk.yml` as the name, paste the contents of that file from this folder, and commit.
4. Open the **Actions** tab. If asked, click **I understand my workflows, go ahead and enable them**.
5. Click **Build APK** on the left, then **Run workflow > Run workflow**. Wait until the run shows a green tick (5 to 10 minutes).
6. Open the finished run, scroll to **Artifacts**, and download **MissionKerala-APK**. Unzip it to get `app-debug.apk`.

## Install on your phone

1. Send `app-debug.apk` to your phone (WhatsApp to yourself, Google Drive or a USB cable).
2. Tap the file. Android will ask you to allow installing from this source. Allow it for this one time.
3. Tap **Install**, then **Open**.

## Notes

- The APK is a debug build, signed with a test key. It installs normally and is meant for demos and pilot testing. A Play Store release needs a proper signing key.
- Fonts load from Google Fonts. With no internet the app still works but uses your phone's default font.
- Every figure, vehicle, driver and shop in the app is sample data. SOS, reports and alerts are simulated and send nothing.
- To change the app later, edit `www/index.html`, commit, and run **Build APK** again.

## Already built the APK once?

Open your repository on GitHub, replace `www/index.html` and `package.json` with the ones from this folder (Add file > Upload files, same names), and commit. Build APK runs again by itself. Download the new APK from the finished run and install it over the old one.
