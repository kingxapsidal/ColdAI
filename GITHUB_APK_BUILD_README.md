# COLDMC AI — Build APK from your phone

This project includes a GitHub Actions workflow that builds an installable Android **debug APK**.

## One-time setup

1. Sign in to GitHub and create a **new repository** (Public or Private).
2. On GitHub, choose **Add file → Upload files**.
3. Extract this ZIP on your phone first, then upload the *contents* of the extracted folder to the repository. The `.github` folder must be included.
   - If your ZIP/file manager hides dot-folders, make sure `.github/workflows/android-apk.yml` is uploaded. You can also create that file manually using the same path and contents.
4. Commit the files to the `main` branch.

## Build and download

1. Open the repository on GitHub.
2. Tap **Actions** → **Build COLDMC AI APK**.
3. Tap **Run workflow** → **Run workflow**.
4. Wait until the workflow finishes with a green check mark.
5. Open that completed run and find **Artifacts**.
6. Download **COLDMC-AI-debug-APK**, extract it, and install the `.apk` file on your Android phone.
7. If Android asks, allow your browser/file manager to **Install unknown apps**.

A push to the `main` branch also triggers a build automatically.

## Important

- This workflow builds a **debug APK** signed with Android's standard debug key. It is suitable for testing and direct installation, but it is not a Play Store release.
- Keep your Pterodactyl panel passwords/API tokens private. Do not commit real credentials, `.env` files containing secrets, or keystores to a public repository.
- This workflow compiles the project; it does not guarantee every app feature or server connection works. Test the app after installing it.
- For future updates, install the newly built APK. Android updates generally need the same application ID and signing key; this debug workflow uses GitHub's generated debug key on each clean runner, so update behavior may require uninstalling the previous debug build first (which can erase local app data).
