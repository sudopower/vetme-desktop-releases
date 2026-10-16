# vetme desktop releases

Release binaries for vetme desktop. Builds are unsigned during alpha and beta.

Runs your interview in your own Claude Code or Codex. vetme is not affiliated with Anthropic or OpenAI.

Downloads are on the Releases page. The macOS builds are for Apple Silicon (M-series) Macs only; there is no Intel Mac build. Alpha and beta builds are marked as pre-releases. This repository holds no source code.

## Installing the alpha

Builds are not signed yet, so your computer warns you the first time you open the app. Running interviews on your own Claude Code or Codex is not in this alpha yet. Only the files attached to a release exist: if a release has no Windows or Linux file, that build is not part of it.

### Install on macOS

macOS on Apple Silicon only (M1 or newer). There is no Intel build.

1. Download `vetme-<version>-mac-arm64.dmg` from the Releases page (for example `vetme-0.2.0-alpha.1-mac-arm64.dmg`).
2. Open the dmg and drag vetme to Applications.
3. Open vetme. macOS blocks the first launch because the app is not signed. Open System Settings > Privacy & Security, scroll to the message about vetme, and choose Open Anyway. Confirm Open.
4. Or, instead of step 3, run this once in Terminal and open the app normally:
   ```
   xattr -dr com.apple.quarantine /Applications/vetme.app
   ```
5. macOS may ask for access to the Keychain item `vetme Safe Storage`. This is where the app keeps your sign-in on this computer. Choose Allow. It can ask again after an update, because each build is signed differently.

### Install on Windows

1. Download `vetme-<version>-win-x64.exe` from the Releases page.
2. Run it. If SmartScreen says "Windows protected your PC", choose More info, then Run anyway.
3. The installer runs in one step and starts vetme when it finishes. Later, open vetme from the Start menu.

### Install on Linux

1. Download the package for your system from the Releases page: `vetme-<version>-linux-amd64.deb` for Debian and Ubuntu, `vetme-<version>-linux-x86_64.rpm` for Fedora and similar.
2. Install it, for example `sudo apt install ./vetme-<version>-linux-amd64.deb` or `sudo dnf install ./vetme-<version>-linux-x86_64.rpm`.
3. Open vetme from your applications menu, or run `/opt/vetme/vetme`.
4. If a game shows a blank or very slow screen, for example in a virtual machine, open Settings > Graphics, turn on Software rendering for WebGL, and restart vetme.

### Sign in

1. Choose Sign in with your browser. Your default browser opens the vetme website.
2. Sign in there with Google, GitHub or email.
3. The browser tab says `Signed in. You can close this tab and return to vetme.` Close it and go back to the vetme window, which updates by itself.

If sign-in does not finish, choose Cancel in the vetme window and try again. If your computer has no secure key store, vetme keeps your sign-in in memory only and the window tells you so; you will sign in again each time you open the app.

### Moving around

- The rail on the left has Dashboard, New assessment, Mock interviews, Sharpen, Arcade, Sessions and Settings. Back and Forward are at the top of the rail.
- The pages are the vetme website, so what you see matches what you see on the web.
- Back and Forward also work from the keyboard: Cmd+[ and Cmd+] on macOS, Alt+Left and Alt+Right on Windows and Linux. Cmd or Ctrl+R reloads the page.
- A link like `vetme://open?path=/sharpen` opens that page in vetme, if vetme is installed. Links that carry sign-in details are refused.
- Settings has your theme, notifications, update status, and devices.

### Updates

vetme checks for updates when it starts and every 6 hours. Settings > Updates shows the version you have, its channel (alpha) and the result of the last check, and Check now runs one on demand.

During the alpha, macOS updates are installed by hand: when Settings > Updates shows a new version, choose Download and replace vetme in Applications. On Windows and Linux, the update downloads in the background and Settings > Updates shows Restart now when it is ready.

If your version is too old to keep working, vetme shows an "Update vetme to continue" screen with a Download the latest version button.

### Signing out

Settings > Sign out. vetme asks you to confirm. It removes your session from this computer and clears what the app stored for vetme pages, including game progress saved on this computer. Your assessments, reports and practice history stay in your account.

### Reporting a problem

Open an issue at https://github.com/sudopower/vetme-desktop-releases/issues. Please include:

- the version (Settings > Updates) and your operating system and version
- what you did, what you expected, and what happened
- a screenshot if it helps

Do not paste tokens, passwords or anything from your Claude Code or Codex setup into an issue.
