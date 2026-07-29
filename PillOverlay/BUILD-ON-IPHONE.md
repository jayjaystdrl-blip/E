# Build the IPA using only an iPhone

1. Sign in to GitHub in Safari.
2. Create a new repository.
3. Extract this ZIP in the Files app.
4. Upload the contents of the `PillOverlay` folder to the repository.
5. Open the repository's **Actions** tab.
6. Select **Build Unsigned IPA**.
7. Tap **Run workflow**.
8. Open the completed workflow run.
9. Under **Artifacts**, download **PillOverlay-unsigned-ipa**.
10. Extract the downloaded artifact ZIP to obtain `PillOverlay-unsigned.ipa`.

The IPA is unsigned. Stock iOS will not install it until it is signed using a permitted signing service or an Apple development certificate.
