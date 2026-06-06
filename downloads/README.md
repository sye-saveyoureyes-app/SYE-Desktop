# SYE Desktop downloads

## Mac (v1.0.0)

- **File:** `SYE-mac-1.0.0.zip` (~99 MB)
- **URL:** `/downloads/SYE-mac-1.0.0.zip`
- **Install guide:** `/desktop/mac-install.html` or `MAC-INSTALL.md` in this folder

### Install (short)

1. Unzip the download
2. Drag **SYE.app** to Applications
3. **Right-click → Open** on first launch (do not double-click the first time)

### “Damaged and can’t be opened”

The app is **not damaged**. macOS quarantine blocks unsigned apps from the web.

- Right-click SYE.app → Open → Open
- Or: System Settings → Privacy & Security → Open Anyway
- Or Terminal: `xattr -cr /Applications/SYE.app`

See **MAC-INSTALL.md** for the full user guide.

### Developer: stop Gatekeeper warnings permanently

1. Apple Developer Program ($99/year)
2. Sign with **Developer ID Application**
3. Notarize with `notarytool`
4. Staple ticket before distributing the ZIP

## Windows

Coming soon.
