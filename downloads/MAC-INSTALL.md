# Installing SYE on Mac

SYE is **not damaged**. macOS shows *“SYE is damaged and can’t be opened”* for apps downloaded from the web that are not yet **signed and notarized** by Apple. That message is misleading — it is Apple’s **Gatekeeper / quarantine** system, not a corrupt file.

**Do not delete the app.** Follow the steps below.

---

## Install (recommended)

1. **Download** `SYE-mac-1.0.0.zip` from the website.
2. **Double-click the ZIP** in Finder to unzip. You should see **`SYE.app`**.
3. **Drag `SYE.app` to Applications** (or run it from Downloads).
4. **First launch — use Right-click → Open** (important):
   - Do **not** double-click the first time.
   - **Right-click** (or Control-click) **`SYE.app`** → **Open**.
   - Click **Open** in the dialog. macOS remembers your choice; later you can double-click normally.

---

## If you still see “damaged and can’t be opened”

### Option A — System Settings

1. Try to open SYE once (you may get the damaged message).
2. Open **System Settings → Privacy & Security**.
3. Scroll down. You may see **“SYE was blocked”** → click **Open Anyway**.
4. Confirm **Open Anyway** again.

### Option B — Remove quarantine (Terminal)

This clears Apple’s download quarantine flag. It is safe for apps you trust from this site.

After unzipping, run **one** of these in **Terminal** (replace the path if needed):

```bash
xattr -cr ~/Downloads/SYE.app
```

If you already moved SYE to Applications:

```bash
xattr -cr /Applications/SYE.app
```

Then open SYE normally (double-click or Right-click → Open).

---

## What each message means

| What you see | What it usually means |
|--------------|------------------------|
| *“damaged and can’t be opened”* | Quarantine + unsigned app — **not** a broken download |
| *“cannot be opened because the developer cannot be verified”* | Same — use **Right-click → Open** or **Open Anyway** |
| *“Move to Trash”* | Gatekeeper block — use the steps above, **don’t** move to Trash |

---

## For developers (fixing this permanently)

To stop macOS from showing these warnings for users:

1. Enrol in the [Apple Developer Program](https://developer.apple.com/programs/) ($99/year).
2. **Code sign** the app with a **Developer ID Application** certificate.
3. **Notarize** the build with Apple (`notarytool`).
4. **Staple** the notarization ticket to the app before zipping/DMG.

Until then, the install steps above are the standard way users open indie Mac apps distributed outside the App Store.

---

**Support:** syecontact.app@gmail.com
