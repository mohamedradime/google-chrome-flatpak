## Google Chrome Flatpak

An automatically updatable Flatpak package of Google Chrome.
It simply depends on a GitHub Action, configured to run daily, that checks for a new releases and accordingly re-configures the manifest.

### Package Limitations

- Missess support for X11 due to security issues (no --socket=x11)
- Missess support for Gamepads, Joysticks, WebHID (no --device=input)
- Missess legacy support for audio streaming (no --socket=pulseaudio)
- Missess legacy support for video streams (no --device=/dev/video\*)
- Missess integration with the file manager (no --talk-name=org.freedesktop.FileManager1)
- Missess support for Chromecast devices (no --system-talk-name=org.freedesktop.Avahi)
- Missess integration with the Bluetooth service (no --system-talk-name=org.bluez)
- Missess support for FIDO2/U2F hardware security keys (no --socket=pcsc)
- Missess support for Kerberos authentication (no krb5, krb5-config or --filesystem=/run/.heim_org.h5l.kcm-socket)
- Missess support for installing PWAs (no flextop)
- Missess integration with enterprise browser policies

### Todos

[] Write a proper documentation  
[] Test the package for full compatibility with Gnome-based environments  
[] Test the package for full compatibility with KDE-based environments  
[] Provide different configurations for different target segments (permissions model and used dependences)  
[] Provide a stable branch that is tested before each new version
[] Use the package desktop and icons instead
