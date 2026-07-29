# PillOverlay

A safe, public-API iOS example that provides:

- A draggable, pill-shaped overlay inside the app.
- Local notification scheduling.
- A Live Activity shown on the Lock Screen and, on supported iPhones, in the Dynamic Island.
- Start, update, and stop controls for the Live Activity.
- A clean starting point for adding app-owned status information.

## Important iOS limitations

A normal App Store or sideloaded iOS app cannot:

- Draw above every other app with a permanent system-wide window.
- imitate or replace the system Dynamic Island for arbitrary content.
- read or intercept notifications belonging to other apps.
- continue unrestricted execution after the user force-quits it.
- use private SpringBoard APIs without jailbreak-level modification.

Live Activities are the supported way to show ongoing app information while the app is backgrounded. After the app is terminated, continuing to update a Live Activity requires ActivityKit push notifications from your server.

## Build

1. Install Xcode 16 or newer.
2. Install XcodeGen:
   `brew install xcodegen`
3. In this directory run:
   `xcodegen generate`
4. Open `PillOverlay.xcodeproj`.
5. Choose your signing team for both targets.
6. Build on a physical device.

## Create an unsigned IPA

Run:

`./Scripts/build-unsigned-ipa.sh`

The script builds with code signing disabled and creates:

`build/PillOverlay-unsigned.ipa`

Unsigned IPAs are not directly installable on stock iOS. They must be signed by a valid development, ad hoc, enterprise, or other permitted signing identity before installation.
